[Back to index](https://tootfinder.ch/index.php)

Tootfinder privacy statement
============================

  

#### Principles

The application does only record data as far as it is needed for the purpose of the application. It does only index data that is public. Data that is obsolete will be deleted within two weeks.

#### Purpose

The purpose of the application is to make recent posts of consenting Mastodon users searchable.

#### Visitor data

The application does not record visits. The underlying webserver does create logfiles of metada that include IP number, a timestamnp and the URI. The logfiles are deleted by the webserver after a month.

#### Query data

For each query that does give results, the query, the timestamp and the number of results are recorded in the database. The data is used for statistical purposes and deleted after 3 months.

#### Consenting user data

Users that opt in are only recorded if they manifest their consent with a magic word ("tootfinder","tfr" or "searchable") on their Mastodon profile. For each verified user host, username, label and id are recorded and the public feed is indexed. A priority field is calculated for each user to optimise the frequency of the crawler.

#### Feed data

The application indexes the feeds of the consenting users. Posts that are public and that are neither replies nor boosts are indexed. For each post, the link, the content, the links and the descriptions of the attachments (media, card) and a timestamp are indexed as while the users name, its avatar and its current follower count.

#### Mentions

Mentions in posts are removed before indexing. It might me possible that a post cites names thet are not mentions.

#### Data sources

The application uses the public API of Mastodon to get the profile of the user and the feed. If the API is not available, it may use the HTML source of the user page and the RSS feed.

#### Reuse of results

Users might share the URL of the result page. The application may provide a REST API to provide the search functionality to third party applications, eg. Mastodon clients.

#### Revoking consent

The user can revoke the consent at any time by removing the magic word on the Mastodon profile. The application checks the profile on a daily base. If the magic word is missing, the user becomes inactive and the posts of the user will not be searchable any more.

#### Deleting data

Post and query data will be deleted after 3 months. User data will be deleted when the user has revoked consent and there are no posts from the user.

#### Cookies

The application does not use cookies, neither own cookies not third party cookies.

#### Source code

The source code of the application is available on [GitHub](https://github.com/bellenuit/Tootfinder). The production environment of the application may have hot fixes which are ahead of the source code.

#### Liabilty

The result page depends on the user posts and the visitor query. The application has no influence on both factors which are entirely user-driven and may not be hold liable for the content of the page.

#### Contact

If you have a privacy issue, you can contact [@buercher@tooting.ch](https://tooting.ch/@buercher) with a direct message.

Version 2.0 2023-04-23