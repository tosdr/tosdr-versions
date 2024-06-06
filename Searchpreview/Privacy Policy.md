[![SearchPreview](sp_logo.png)](https://searchpreview.de/)

SearchPreview - Privacy Policy
------------------------------

SearchPreview does not process or hold personal user data. SearchPreview only handles non-personal user data required for its features. Each feature can be individually disabled/enabled in the SearchPreview preferences area. If you turn off a feature, user data related to that feature is neither transmitted nor held.

### Feature: Site Preview Images (Thumbnails)

The preview images that are inserted into the search results page are standard html images. Your browser requests the images from a SearchPreview image server (depending on your location eu1. or jp. or nyc. or sfo.searchpreview.de/preview or /x2 for retina preview images) via the HTTPS protocol, this request contains the following information:

* The request for the preview image
* The referrer site (the site the image was embedded in, for example https://www.google.de/)
* The user agent (a string identifying the browser you are using, for example Mozilla/5.0 (Macintosh; Intel Mac OS X 10\_11\_5) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/51.0.2704.103 Safari/537.36

Every HTTPS request contains the above data, see the RFC 2616 (http://www.w3.org/Protocols/rfc2616/rfc2616.html) for a detailed description of the protocol details. The request for the preview image (for example https://eu1.searchpreview.de/preview?s=http://www.mozilla.com&ua=Chrome&ver=833) contains the site of the image that is requested, a user agent flag stating which Browser is used and the version number of the SearchPreview engine.

Your IP address is required for the transmission of above data between your Browser and the SearchPreview image server, however the SearchPreview server software does not read, process or hold your IP Address.

The SearchPreview image server will log every request in a log file on disk, in addition to above data the following data is logged per request: Time, bytes transferred, duration of request, http code. These log files are not sold or given to third parties and are automatically deleted after 10 days. The only purpose of the log files is to monitor performance and traffic usage.

You can disable the Site Preview Images feature in the SearchPreview options area, in this case no data is sent to / requested from the SearchPreview Preview Image servers.