[back](#) [menu](#nav)

[Log in](https://thesession.org/login?redirect=%2Fapi) or [Sign up](https://thesession.org/signup)

[The Session](https://thesession.org/)

API
===

The Session has a read-only API. Information that is available through the website as HTML is also available in other formats. To request a URL in another format, add `?format=` to the URL with one of the these formats specified:

Formats
-------

|     |     |
| --- | --- |
| JSON | ?format=json |
| XML | ?format=xml |
| RSS | ?format=rss |

Endpoints
---------

The following lists are available in multiple formats e.g. [/tunes/new?format=json](https://thesession.org/tunes/new?format=json) or [/recordings/search?q=altan&format=rss](https://thesession.org/recordings/search?q=altan&format=rss)

By default, 10 items will be returned in a list. You can request up to 50 items by appending &perpage= e.g. [/tunes/new?format=json&perpage=35](https://thesession.org/tunes/new?format=json&perpage=35)

If you request an individual item, e.g. [/tunes/27?format=xml](https://thesession.org/tunes/27?format=xml), you will get back the details for that item and any comments that have been posted to it.

### Tunes

|     |     |     |
| --- | --- | --- |
| New tune settings | [/tunes/new](https://thesession.org/tunes/new) |
| Popular tunes | [/tunes/popular](https://thesession.org/tunes/popular) |
| Recordings of tunes | [/tunes/recordings](https://thesession.org/tunes/recordings) |
| Sets of tunes | [/tunes/sets](https://thesession.org/tunes/sets) |     |
| Tune search results | [/tunes/search?q=searchterm](https://thesession.org/tunes/search?q=humours) |
| Individual tune | [/tunes/ID](https://thesession.org/tunes/2) |
| Comments on tunes | [/tunes/comments](https://thesession.org/tunes/comments) |

### Discography

|     |     |
| --- | --- |
| New recordings | [/recordings/new](https://thesession.org/recordings/new) |
| Recordings search results | [/recordings/search?q=searchterm](https://thesession.org/recordings/search?q=altan) |
| Individual recording | [/recordings/ID](https://thesession.org/recordings/324) |
| Comments on recordings | [/recordings/comments](https://thesession.org/recordings/comments) |

### Trips

|     |     |
| --- | --- |
| Upcoming trips | [/trips/upcoming](https://thesession.org/trips/upcoming) |
| New trips | [/trips/new](https://thesession.org/trips/new) |
| Trips search results | [/trips/search?q=searchterm](https://thesession.org/trips/search?q=dublin) |
| Nearby trips | [/trips/nearby?latlon=latitude,longitude&radius=75](https://thesession.org/trips/nearby?latlon=42.34891891,-71.15130615&radius=75) |
| Individual trip | [/trips/ID](https://thesession.org/trips/187) |
| Comments on trips | [/trips/comments](https://thesession.org/trips/comments) |

### Sessions

|     |     |
| --- | --- |
| New sessions | [/sessions/new](https://thesession.org/sessions/new) |
| Sessions search results | [/sessions/search?q=searchterm](https://thesession.org/sessions/search?q=california) |
| Nearby sessions | [/sessions/nearby?latlon=latitude,longitude&radius=75](https://thesession.org/sessions/nearby?latlon=42.34891891,-71.15130615&radius=75) |
| Individual session | [/sessions/ID](https://thesession.org/sessions/35) |
| Comments on sessions | [/sessions/comments](https://thesession.org/sessions/comments) |

### Events

|     |     |
| --- | --- |
| Upcoming events | [/events/upcoming](https://thesession.org/events/upcoming) |
| New events | [/events/new](https://thesession.org/events/new) |
| Events search results | [/events/search?q=searchterm](https://thesession.org/events/search?q=london) |
| Nearby events | [/events/nearby?latlon=latitude,longitude&radius=75](https://thesession.org/events/nearby?latlon=51.54412079,-0.13344830&radius=75) |
| Individual event | [/events/ID](https://thesession.org/events/2958) |
| Comments on events | [/events/comments](https://thesession.org/events/comments) |

### Discussions

|     |     |
| --- | --- |
| New discussions | [/discussions/new](https://thesession.org/discussions/new) |
| Discussions search results | [/discussions/search?q=searchterm](https://thesession.org/discussions/search?q=whistle) |
| Individual discussion | [/discussions/ID](https://thesession.org/discussions/10525) |
| Comments on discussions | [/discussions/comments](https://thesession.org/discussions/comments) |

### Member contributions

|     |     |
| --- | --- |
| Tune settings | [/members/ID/tunes](https://thesession.org/members/1/tunes) |
| Recordings | [/members/ID/recordings](https://thesession.org/members/1/recordings) |
| Trips | [/members/ID/trips](https://thesession.org/members/1/trips) |
| Sessions | [/members/ID/sessions](https://thesession.org/members/1/sessions) |
| Events | [/members/ID/events](https://thesession.org/members/1/events) |
| Discussions | [/members/ID/discussions](https://thesession.org/members/1/discussions) |

### Member data

|     |     |
| --- | --- |
| Tunebook | [/members/ID/tunebook](https://thesession.org/members/1/tunebook) |
| Bookmarks | [/members/ID/bookmarks](https://thesession.org/members/1/bookmarks) |
| Sets of tunes | [/members/ID/sets](https://thesession.org/members/1/sets) |

Activity Streams
----------------

There are a number of activity streams published on The Session to the [Activity Streams JSON specification](http://activitystrea.ms/specs/json/1.0/). You can access the activity streams by appending `?format=json` to these endpoints (paginate with `&page=2`, `&page=3`, etc.:

|     |     |
| --- | --- |
| The Session | [/activity](https://thesession.org/activity) |
| Tunes | [/tunes/activity](https://thesession.org/tunes/activity) |
| Recordings | [/recordings/activity](https://thesession.org/recordings/activity) |
| Trips | [/trips/activity](https://thesession.org/trips/activity) |
| Sessions | [/sessions/activity](https://thesession.org/sessions/activity) |
| Events | [/events/activity](https://thesession.org/events/activity) |
| Discussions | [/discussions/activity](https://thesession.org/discussions/activity) |

Activity streams are also available for individual items:

|     |     |
| --- | --- |
| Individual tune | [/tunes/ID/activity](https://thesession.org/tunes/27/activity) |
| Individual recording | [/recordings/ID/activity](https://thesession.org/recordings/4276/activity) |
| Individual trip | [/trips/ID/activity](https://thesession.org/trips/3/activity) |
| Individual session | [/sessions/ID/activity](https://thesession.org/sessions/3294/activity) |
| Individual event | [/events/ID/activity](https://thesession.org/events/3079/activity) |
| Individual discussion | [/discussions/ID/activity](https://thesession.org/discussions/31185/activity) |
| Individual member | [/members/ID/activity](https://thesession.org/members/1/activity) |

There are also individual activity streams for member notifications:

|     |     |
| --- | --- |
| Tunes | [/members/ID/notifications/tunes](https://thesession.org/members/1/notifications/tunes) |
| Recordings | [/members/ID/notifications/recordings](https://thesession.org/members/1/notifications/recordings) |
| Trips | [/members/ID/notifications/trips](https://thesession.org/members/1/notifications/trips) |
| Sessions | [/members/ID/notifications/sessions](https://thesession.org/members/1/notifications/sessions) |
| Events | [/members/ID/notifications/events](https://thesession.org/members/1/notifications/events) |
| Discussions | [/members/ID/notifications/discussions](https://thesession.org/members/1/notifications/discussions) |

Data dumps
----------

You can download CSV and JSON files of [data from The Session on Github](https://github.com/adactio/TheSession-data) ([.zip](https://github.com/adactio/TheSession-data/archive/master.zip)). These are updated about once a week.

Example apps
------------

Here are some things people have made using The Session’s API or data dumps:

[Tunetable](https://anton-bregolas.github.io/Tunetable/)

A web app for turning lists of tunes into tables.

[Nota](https://notabc.app/)

[An app](https://apps.apple.com/us/app/nota-abc-session-tunes/id6446770292) for iPhone and iPad for managing tune collections.

[FolkFriend](https://folkfriend.app/)

A web app that recognises tunes from audio input.

[Session Maker](https://play.google.com/store/apps/details?id=com.sessionmaker)

An Android app for creating sets of tunes. It integrates with your tunebook here on The Session.

[TradMusician’s ABC music](https://play.google.com/store/apps/details?id=nodeslight.tradmusician2)

An Android app for managing your tunebook.

[geoTrad](https://www.google.com/maps/d/u/0/viewer?mid=1ck967b4xL-6XUr-CUwTojdJNa97b43jL&ll=53.45307877071246%2C-8.028519600000001&z=7)

A map showing the distribution of Irish traditional tunes which reference place names in Ireland.

[SessionBuddy](https://github.com/ColmanOB/SessionBuddy)

A Java helper library to make it easier for Java developers to work with The Session’s API.

[The Craic](http://thecraic.co/)

[An app](https://apps.apple.com/app/the-craic/id586009292) for iPhone and iPad for searching across multiple online tune collections.

[back](#) [menu](#top)

[Log in](https://thesession.org/login?redirect=%2Fapi) or [Sign up](https://thesession.org/signup)

* [Tunes](https://thesession.org/tunes)
* [Discography](https://thesession.org/recordings)
* [Trips](https://thesession.org/trips)
* [Sessions](https://thesession.org/sessions)
* [Events](https://thesession.org/events)
* [Discussions](https://thesession.org/discussions)

* [help](https://thesession.org/help)
* [privacy](https://thesession.org/privacy)
* [contact](https://thesession.org/contact)
* [links](https://thesession.org/links)
* [donate](https://thesession.org/donate)

[back to top](#top) [Log in](https://thesession.org/login?redirect=%2Fapi)