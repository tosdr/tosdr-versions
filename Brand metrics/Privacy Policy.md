1



Privacy Design



The guideline at Brand Metrics for personal information is to avoid it. When implementing

features where personal information needs to be stored top management must review and

approve the design first. This document goes into details about how and what data is collected,

processed, stored and used.



The individuals that use the system can be divided into two main groups;



• Customers and Users, typically employed by Customers of Brand Metrics



• Respondents, consumers and visitors to Customers web sites.



The interaction with the system is separated and quite different between Respondents and Users.

This document covers both groups. Starting with explaining Respondents in detail and describes

how and what data Brand Metrics collects, processes, stores and uses regarding Respondents.

Subsequently a detailed description of what data Brand Metrics as s supplier collects, stores and

uses regarding its Users and Costumers.

Respondents



Brand Metrics is involved in the business of insight and offers its Customers a software solution

designed for continuous measurement of digital advertisement. The respondent is the Customer’s

end-user, id est a person (web browser) that visits and consumes a Customer’s web site or

service.



When a person (web browser) visits a Customer’s web site it may be exposed to an ad that is part

of a Brand Metric measurement. Subsequently the visitor may be targeted with a Brand Metric

survey and may give its consent and by answering the survey becoming a Respondent.



As a visitor loads a Customer’s site there could be an ad tagged with a Brand Metrics pixel, when

the pixel is loaded a Unique ID (cookie) is set in the browser. Simultaneously an asynchronous

JavaScript from Brand Metrics is also loaded. This JavaScript handles the surveys automatically

– meaning it reads the visitors cookies and according to the information serves the visitor with a

survey or not. The JavaScript library communicates with the backend, controlling how many times

the browser has been exposed to the ad (id est the Brand Metrics pixel) and if the measurement

needs more responses in that group of exposed.



The Brand Metric survey contains one question covering the Respondents relationship to an

advertiser. This cannot be regarded as personal data. The survey can in some cases be covering

questions of where the answers can be regarded as personal information, the following cases:



• Survey contains demographical question such as gender and age



• Customized questions - a customer can define his own questions, there answer can be

defined as personal information



The following chapters goes through all cookies used, requests made and how data is stored and

deleted.

2



Cookies



First party cookies

Name Value Description

\__bmdnt empty A cookie that is set if a user opts out from the Brand Metric

measurements. If it's set the site script will not initialize itself.



Third party cookies

Name Value Description

\__bmp_[mid] (see

below)

Measurement cookie, keeps measurement information on a browser

level. It’s updated by the backend when the browser is exposed to an

ad or when a survey is triggered or answered. It’s read when the server

makes a decision to show a survey. Information from the cookie is

stored when a survey is answered. The expiration date of the cookie is

set to 3 weeks after the measurement is done.

\__bmsrvdnt 'all' or a

list of

siteids



A cookie that is set if a user opt out from Brand Metric measurements,

it could be set on a site level or on all Brand Metric measurements.



\__cfduid id Cloudflare cookie https://support.cloudflare.com/hc/en-

us/articles/200170156-What-does-the-CloudFlare-cfduid-cookie-do-



Data in measurement cookie

Field Name Description

0 Version A number identifying the version of this protocol

1 NbrOfExposures A counter for how many times the browser has been exposed to

ads in the measurement.

2 LastExposureTime A timestamp from when the browser was last exposed of a pixel in

the measurement

3 NbrOfSurveys A counter for how many times the survey for the measurement has

been triggered for the browser

4 LastSurvey A timestamp from the last time a survey was triggered

5 IsAnswered True if the survey is answered

6 Pixels If a measurement has many pixels we keep a counter for each pixel

in this field.

7 Id A random guid used as id for the browser during the measurement.

The id is used when the survey has more than one answer.

3



Requests

Path Description

info Called by the pixel tag, updates the measurement cookie, increase the

impression counter for the pixel, DeviceType, NbrOfExposure

combination.

Survey/Script/[siteid].js Returns a script that is customized for each site, cloudflare is used as

a cdn.

Survey/Config When the site script is initiated it makes a request to config, config

checks the measurement cookies and makes a decision if a survey

should be triggered, if it decides to show a survey the SurveyTriggered

counter is increased.

Survey/Show/[pixel].js Returns a script that is a combination of script and config, it will not

make the call to config, instead it will always show the survey. The

script is returned on a pixel level and not on a site level.

Template/[mid] Returns an html document to be used as src in an ifram, the

document contains the complete survey. dt and siteid is used to show

a custom survey for the context.

Survey/Info Is called by the survey when 1, a survey has been rendered. 2, When a

survey is inview. 3, if a survey is closed, 4, when a survey is completed.

It increase a counter and updates the measurement cookie.

Survey/Answer Called when a respondent answers a question, the response is stored

together with NbrOfExposures, dt, siteid and when the measurement

has more than one question the id from the measurement cookie.

diagnostics Used to log error messages, only used when troubleshooting.



Parameters

Name Description Usage

siteid Unique id for a site, this id is created by

the system when the site definition is

created.



This id flows through the system, it’s used to

get the custom javascript for the site and

then it is sent with the requests to make it

possible to know if there is any active

measurement, show a branded survey, and

to breakdown counters and answers on site

level.

mid Uniqe id for a measurement, this id is

created by the system when the

measurement is created



Used to show the right survey and to

connect answers to a measurement.



pixel Unique id, A measurement can have

one or more pixels, each pixel is

created with the measurement



Used to break down exposed into different

groups, which the system can’t figure out by

itself.

qdata Data from a survey. mid|type|q1=1;...,

measurement id is stored in the first

field, the data type is stored in the next

field, it could be, answer, rendered,



Answers to the questions in a survey, stored

and processed. It’s also used by ‘survey/info’

to identify for which measurement a survey

has been rendered.

4



inview, closed, completed. The last

fields is a list of answers.

dt Device type (phone, tablet, desktop).

Calculated from the useragent by the

site script



Used to break down answers and exposed

into different groups and to customize the

survey.

toploc Host name calculated from the location

by the site script

Used for troubleshooting and if siteid is

missing it’s used to try to find the siteid on

backend.

test ‘true’ or ‘false’ Used to filter out testdata when the data is

processed. The parameter should be set in

different test contexts.

rnr A random number Added to requests to not get cached

answers

msg A log message Used by ‘diagnostics’, Critical exceptions in

the site script can be logged, normally we do

not log anything, it’s turned on if we need to

troubleshoot.



Request Processing



When a request is processed we use the user agent to decide devicetype if the dt parameter is

missing. We also use the user agent to detect if the request comes from a browser that supports

3p cookies.



When an answer is stored we take a timestamp, the timestamp is used when we decide if we

need to collect more surveys and it could be used to breakdown the result from the processing.



We do not store or use any other information from the request i.e. IP Address.

5



Storage



Data from the collection phase is stored in Azure Table Storage.

Counters



We buffer the calls to increase counters then we group them by type and properties and store a

new row for each group.



Name Description

Type Impression/SurveyTriggered/SurveyRenderd/SurveyInview/SurveyAnswer/Surtvey

Closed

Time Timestamp when stored

Properties pixel, dt, siteid, exposures, test, ThirdPartyCookieSupport

Count nbr of events to add



Survey

Name Description

UniqueId Unique id for a browser during a measurement

Time Timestamp when stored

Properties pixel, dt, siteid, exposures, test, ThirdPartyCookieSupport

Answers A list of (questionid,answer)



Processing



The counters are accumulated each hour and used during a measurement to be able to show

progress and alert problems.



The surveys are aggregated during the measurement to decide if we need to show more

interviews.



To calculate the results (KPIs):

- The Impression counter is filtered, and used to calculate total impressions and unique.

- From the total impression and unique values frequencies are calculated.

- From the answer table we use the answers and exposed to calculate KPIs, time and properties

are used for breakdowns.

Retention



When a measurement is carried out and the KPIs are calculated we store the project in the

reference database, in the reference database the KPI:s are stored together with aggregates from

unique and counters. We also store the answers, but we remove the uniqueId.



When a measurement is completed we keep it in table storage for a couple of week to be able to

reprocess and troubleshot, after that we delete the tables.



The measurement cookie has an expiration date set to 3 weeks after the measurement ends and

will be removed by the browser.

6



Do not track



Most browsers implement the DNT header where a user optionally can opt out from tracking. The

browser then adds a header to all requests. The backend looks for the DNT header before it sets

any cookies.



Brand Metrics also has its own do not track cookie which could be set from our site or by a

command in the js library.

Data visualization



https://collector.brandmetrics.com/cookies shows all the information that is stored in the cookies

Brand Metrics has created in a browser. All non-anonymized information Brand Metrics has about

a browser can also here easily be deleted.



Customers and Users



The Brand Metric system deals with personal data in the following cases:



• Users - we keep email addresses



• Customers - we keep contact information



Both these personal data is related to the Brand Metrics booking interface, where measurements

are booked, handled and reported.



How Brand Metrics handles Personal Data is described in Brand Metrics Privacy Policy (to be

found below).



Brand Metrics Privacy Policy

General Information about processing personal data



Brand Metrics take personal integrity very seriously and protect your personal data. Brand Metrics

comply with legislation that is applicable at any given time with the aim of protecting you as a

private individual.



Brand Metrics objective is that you should feel secure that your personal integrity is respected and

that your personal data is processed correctly. Brand Metrics take responsibility that personal

data that is processed by Brand Metrics is used solely for the intended purposes and protected

against unauthorised access. All processing of personal data within Brand Metrics takes place in

accordance with applicable personal data legislation. From 25 May 2018, the general data

protection regulation (GDPR) applies within the EU/EES.



Please read this integrity policy carefully in order to understand how and for which purposes

Brand Metrics process your personal data. In providing your personal data to us and approving

7



applicable conditions, you consent to your personal data being processed in accordance with that

stated in the specific terms and conditions for the respective service and this integrity policy. If the

law requires more specific consent from you, we will naturally ask for it.



Amendments in this integrity policy are notified and published on Brand Metrics's websites.



What is personal data and processing of personal data?



”Personal data” refers to all information that can be directly or indirectly linked together with other

information about a currently living natural person. It means that widely divergent information

such as name and contact details, IP-addresses, survey responses, choices made and behaviour

comprise personal data.



Processing of personal data is everything that takes place with personal data. Every measure that

is taken with personal data constitutes processing, regardless of whether or not it is compiled

automatically, such as collection, registration, organisation, structuring, storage, processing or

change, production, reading, use, issue through transfer, dissemination or supply by other means,

adjustment or compilation, limitation, deletion or destruction.



To ensure that you have as good an insight as possible into how we work with personal data, we

have organised our integrity policy in the following sections:



1. Who is responsible for your personal data and contact information

2. Legal grounds and legitimate interests for personal data processing

3. What personal data do we process?

4. Why we collect your personal data and how long it is saved

5. What rights you have

6. Who we share your information with

7. Security measures



1. Who is responsible for your personal data?



Brand Metrics AB is data controller for the information that is provided directly to us by an

individual. In certain contexts Brand Metrics can act as data processor. In these cases, a data

processor agreement is drawn up in order to regulate how your personal data is processed by

Brand Metrics. If you have points of view, questions or other considerations concerning our

integrity policy or processing of personal data, you are always welcome to contact us via e-mail

(info@brandmetrics.com) or by post to:



Brand Metrics AB

Kungsportsplatsen 1

SE-411 10 Göteborg

Tel.: +46 (0)70-264 09 04

Corp. ID no. 559139-4332

8



2. Legal grounds and legitimate interests for personal data processing



Brand Metrics always processes your personal data in accordance with applicable legislation. We

process your personal data when it is necessary to fulfil a contract with you or answer a request

from you and when we have another legitimate and rightful interest to process your personal data,

e.g. an interest in marketing ourselves to visitors in our digital channels or an interest in

developing our digital channels. If Brand Metrics should process your personal data for any

purpose which, according to applicable legislation, requires your consent, we will obtain your

consent in advance.



3. What data do we process?



When you visit/use Brand Metrics digital channels or their services or communicate with us, we

may collect information about you such as name, address, postal address, e-mail address,

telephone number, identification details, information about your usage of our services and

products and transaction history and for certain services, images and site information as

well. Where appropriate, personal identity number and card details may also be processed. In

addition, Brand Metrics may collect technical data about the units you use to gain access to our

digital channels, including IP-address, unique unit ID, type of web browser and cookie information.



The collection described herein takes place, for example, through you providing your personal data

in various forms in our digital channels or their services, that you communicate with Brand

Metrics and others via Brand Metrics's platforms and in social media, provide points of view in our

contact form or via telephone, download reports from Brand Metrics's web pages or register for

newsletters or events that Brand Metrics arranges.



When you contact us via forms in our digital channels, in connection with queries for example,

your contact details and case information will be processed by us.



If you visit or communicate with us via our accounts in social media (i.e. third party platforms

such as Facebook and Twitter for example), Brand Metrics may receive information concerning

your profile and your interactions on the third party platform from the supplier of the platform.



4. Why and for how long do we process your personal data?



Within Brand Metrics we process personal data for users and customers of Brand Metrics who

use our services. We process personal data about you principally in order to administer our

services, mailings of offers and information to you. In detail, we use your personal data:



To enable us to supply the products and services you ordered and administer our contract with

you;



To enable us to communicate with you in contacts via telephone, e-mail, forms and in our

accounts in social media;



To ensure that the information we have about you is correct and current;

9



To administer marketing activities;



For marketing purposes, including marketing via post, e-mail and SMS/MMS (which you can

deselect via a link in each mailing made via e-mail or SMS/MMS);



To analyse and group the visitors according to selection, priority and preferences, which means

that so-called profiling takes place with the aim of being able to provide you with relevant and

customised information, surveys, recommendations, advertisements and offers. It is also possible

that data which derives from usage of various digital channels from Brand Metrics and from our

collaborative partners is coordinated for this purpose, as well as for the purpose of developing

products and services;



To process inward payments and/or outward payments or prevent or detect fraud;



To produce statistics about the use of our digital channels and their services; and



To maintain, develop, test and improve our digital channels and the technical platforms on which

they are provided.



4, a. Processing of personal data for children



Children refers to persons under 16 years old, in accordance with ESOMAR's ethical rules.



Brand Metrics's digital channels are not targeted at children and consequently Brand Metrics does

not consciously collect personal data about children. If you are guardian and become aware that

your child has provided personal data to Brand Metrics, we ask you to contact us at the addresses

indicated in item 1 so that you can exercise your rights with respect to, for example, correction or

removal.



4, b. External links



This integrity policy applies for information which Brand Metrics processes about you within the

framework of our digital channels. Brand Metrics's digital channels can sometimes contain links

to external websites or services that we do not control. If you follow a link to an external website,

you are urged to appraise yourself of the principles for personal data processing and information

about cookies that applies for the relevant page.



5. Your rights



If you want to utilise any of the following rights, please contact us via email (mail address) or post

to the address provided in item 1.



• Right to information: you can ascertain at any time which information, if any, we have about you in

our register and how we process it. We will respond to your wishes without unnecessary delay and

within one month. If for any reason we are not able to fulfil your wishes, a justification will be

provided.

10



• Right to correction: You are entitled to request correction in relation to personal data that we

process about you. At your request or when Brand Metrics detects it, Brand Metrics will correct or

delete incorrect or incomplete information.

• Right to deletion/be forgotten: You can request at any time that we cease processing your personal

data and also delete the information we have about you. If you have registered for newsletters,

subscriptions or notification of other updates and do not want to have further e-mail messages, you

can also unsubscribe via the link in the mailing.

• Data portability: you are entitled to access the information you have provided yourself in order to

transfer it to another service.

• Objection to processing: you are entitled to object to processing of your personal data.

• You are also entitled at any time to submit a complaint to the applicable supervisory authority if you

consider that your personal data is being processed in contravention of applicable personal data

legislation.



Brand Metrics is not responsible for problems that arise as a result of the personal data being old

or incorrect if you have neglected to notify us of the change.



6. Who do we share your information with?



Brand Metrics can engage external collaborative partners (suppliers) to perform tasks on Brand

Metrics's behalf, e.g. to provide IT-services, payment solutions or help with marketing, analyses or

statistics. The execution of these services may mean that Brand Metrics's collaborative partners,

both within the EU/EES and outside the EU/EES, have access to your personal data. Companies

which process personal data on Brand Metrics's behalf always sign a contract with Brand Metrics

to ensure there is a high level of protection for your personal data at our collaborative partners

too. In relation to collaborative partners outside the EU/EES, specific precautionary measures are

instituted, for example, contracts which include standard clauses for data transfer which have

been adopted by the European Commission and which are available on the European

Commission's website.



Brand Metrics may provide personal data to third parties, for example, the police or another

authority, if it concerns investigation of crime or if we are otherwise legally obliged to provide such

data based on an official decision.



Brand Metrics will not surrender your personal data to any another extent than that described in

this item 6.



6, a. Cookies



A cookie makes it possible to recognise your computer and collect information about which pages

and functions have been visited. Cookies are sometimes used to collect information that is

regarded as constituting personal data, for example: IP-addresses and information linked to the IP

address. Cookies are essentially used by all websites and are often a prerequisite that the website

or the digital channel is able to function.



On Brand Metrics's websites cookies are used from:

11



• Google Analytics in order to analyse web traffic and user behaviour. These cookies store

information about how the visitors use the website, for example, where they come from, how

many and which pages are visited and how long they spent on the website. These cookies help us

to analyse the visitors' behaviour on the website in order to improve the user experience and

ensure the website's functionality.



An approval of web tracking and analysis can be withdrawn at any time. An addition to your web

browser can be downloaded from Google's website and installed

(https://tools.google.com/dlpage/gaoptout). Alternatively, you can delete cookies from your

computer or mobile unit yourself via the web browser. For instructions on how to manage and

delete cookies, go to the ”Help” option in your web browser. You can select to deactivate cookies

or obtain a notification each time a new cookie is sent to your computer or mobile unit. Note that

if you select to deactivate cookies, you will not be able to utilise all functions on our website



No information is transferred to any third parties.



7\. Security measures



Brand Metrics takes appropriate technical and organisational steps to ensure that your personal

data is processed securely and in accordance with this policy against improper access, alteration,

distribution and/or destruction.



8. IAB \& IAB Transparency and Consent Framework



Brand Metrics Sweden AB is a member of IAB and certified according to IAB Transparency and

Consent Framework ant its guidelines. https://advertisingconsent.eu/vendor-list/