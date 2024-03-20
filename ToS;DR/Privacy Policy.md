tosdr.org Privacy Policy
========================

We only use cookies to store your language, theme preferences or sessions and not any tracking technology.

We anonymize all IP addresses in our nginx logs, but store them for up to 1 day in our Redis Ratelimiting server.

Your IP address will temporarily be visible in to Netcup who provide infrastructure.

We employ anonymized IP logging, this means nginx collects web requests but anonymizes IPs in the process.

(Private IP used in the example below)

    192.115.194.0 - - [01/May/2021:08:21:12 +0200] "GET /api/1/all.json HTTP/2.0" 200 753375 "-" "Mozilla/5.0 (Windows NT 6.1; Win64; x64; rv:88.0) Gecko/20100101 Firefox/88.0" "-"

CODE

Your IP may be stored temporarily in our Redis Cache in order to enforce rate limits.

The only time your IP Address is stored in logs without any path or user agent is to block malicious IPs using fail2ban:

    log_format fail2ban '$remote_addr [$time_local] $status';

CODE

For our assets such as logos, branding images we use a selfhosted S3: Minio.

Our forum software is self hosted using Discourse

### Nginx IP logging configuration

    map $remote_addr $ip_anonym1 {
        default 0.0.0;
        "~(?P<ip>(\d+)\.(\d+)\.(\d+))\.\d+" $ip;
        "~(?P<ip>[^:]+:[^:]+):" $ip;
    }
    
    map $remote_addr $ip_anonym2 {
        default .0;
        "~(?P<ip>(\d+)\.(\d+)\.(\d+))\.\d+" .0;
        "~(?P<ip>[^:]+:[^:]+):" ::;
    }
    
    map $ip_anonym1$ip_anonym2 $ip_anonymized {
        default 0.0.0.0;
        "~(?P<ip>.*)" $ip;
    }
    
    log_format anonymized '$ip_anonymized - $remote_user [$time_local] ' 
                          '"$request" $status $body_bytes_sent ' 
                          '"$http_referer" "$http_user_agent"';
    log_format fail2ban '$remote_addr [$time_local] $status';
    access_log  /var/log/nginx/access.log  anonymized;
    access_log  /var/log/nginx/access-f2b.log  fail2ban;

CODE

×