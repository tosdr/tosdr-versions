[Back to all legal agreements](https://www.gemini.com/legal)

* [Welcome to the Gemini API](#section-welcome-to-the-gemini-api)
* [Using Our API](#section-using-our-api)
* [Permission](#section-permission)
* [Documentation](#section-documentation)
* [Account Data and Transactions](#section-account-data-and-transactions)
* [OEMS Service Providers](#section-oems-service-providers)
* [Request Types](#section-request-types)
* [Request Limits](#section-request-limits)
* [Gemini Market Data](#section-gemini-market-data)
* [Authorized Access and Security](#section-authorized-access-and-security)
* [Suspension or Termination](#section-suspension-or-termination)
* [Indemnification](#section-indemnification)
* [Warranties and Limitation of Liability](#section-warranties-and-limitation-of-liability)
* [Questions](#section-questions)

[Back to all legal agreements](https://www.gemini.com/legal)

API Agreement
=============

Last updated: December 2, 2022

* * *

#### Welcome to the Gemini API

Welcome! Thanks for visiting Gemini, a global digital asset platform. You agree and understand that by accessing or using Gemini’s application programming interface (the “API”), you are agreeing to enter into this API agreement (the “API Agreement”) and be legally bound by its terms and conditions, so please read them carefully. If any term or condition of this API Agreement is unacceptable to you, please do not use our API. This table describes which Gemini entity or entities (collectively “Gemini,” “we,” “us,” or “our”) you are contracting with:

| Your Place of Residency | Services Provided | Your Gemini Entity | Contact Address |
| --- | --- | --- | --- |
| Anywhere outside of EEA and UK | \-Fiat services  <br>  <br>\-Digital Asset services | Gemini Trust Company, LLC NY Entity No: 5002896  <br>  <br>(d/b/a Gemini Exchange, LLC in AZ, CA, DE, FL, ID, IL, KS, KY, MA, MI, MN, NC, ND, NM, OH, OR, SD, UT, and VA; d/b/a Gemini Exchange in AK and WA) | 600 Third Avenue, 2nd Floor New York, NY 10016 |
| UK  | \-E-money services | Gemini Payments UK, Ltd Company No: 11497305 FCA Register No: 900988 | Suite 1, 7th Floor, 50 Broadway, London SW1H 0BL |
| UK  | \-Digital Asset services | Gemini Intergalactic UK, Ltd Company No: 12471710 FCA Register No: 921817 | Suite 1, 7th Floor, 50 Broadway, London SW1H 0BL |
| European Economic Area (EEA) | \-E-money services | Gemini Payments Europe Limited Company No: 669681 CBI Reference No: C432664 | 70 Sir John Rogerson’s Quay, Dublin 2, Ireland |
| European Economic Area (EEA) | \-Digital Asset services | Gemini Intergalactic Europe Limited Company No: 698251 CBI Reference No: C453651 | 70 Sir John Rogerson’s Quay, Dublin 2, Ireland |
| United States | \-Credit Card | Gemini Constellation LLC | 600 Third Avenue, 2nd Floor New York, NY 10016 |
| United States | \-Digital Assets portfolio management services | Bitria, Inc. | 600 Third Avenue, 2nd Floor New York, NY 10016 |
| Any Jurisdiction in which Gemini Derivatives is Available | \-Gemini Derivatives | Gemini Artemis Pte. Ltd. | 18 Robinson #17-01, 18 Robinson Road, Singapore 048547 |

#### Using Our API

By accessing or using Gemini’s API, you represent and affirm that you are at least 18 years old, have the legal capacity to enter into this API Agreement, and agree to be legally bound by the terms and conditions of this API Agreement in their entirety.

You agree and understand that this API Agreement is subject to the terms and conditions set forth in your User Agreement(s), which also govern this API Agreement. In case of conflict, the User Agreement(s) shall control. You further agree and understand that the defined terms used in this API Agreement, if defined in your User Agreement(s), shall have the meanings set forth in your User Agreement(s). Your use of our API must comply with your User Agreement(s).

Feel free to print and keep a copy of this API Agreement, but please understand that we reserve the right to change any of these terms and conditions at any time. But don’t worry, you can always find the latest version of this API Agreement here on this page.

You agree and understand that by accessing or using Gemini’s API following any change to this API Agreement, your access or use of Gemini’s API shall constitute your agreement to the amended API Agreement, and you agree to be legally bound by its terms and conditions as amended. You should, therefore, read this API Agreement from time to time. If you do not agree to be bound by this API Agreement, you should not access or use Gemini’s API.

##### Permission

Subject to the terms and conditions set forth in this API Agreement, we hereby grant to you a non-assignable, non-exclusive, worldwide, and royalty-free limited license to use our API. You may not use our API if (i) you are not at least 18 years old and do not have the legal capacity to enter into this API Agreement, (ii) you are a person barred from using our API under the applicable laws of the United States or other countries, including the country in which you are resident or from which you use our API, and (iii) you do not agree to be legally bound by the terms and conditions of this API Agreement in their entirety.

##### Documentation

Our API documentation is available here:

[https://docs.gemini.com/](https://docs.gemini.com/)

If you are using our API, please complete our API Use Form, which is available here:

[https://geminiapi.typeform.com/to/Ryq6yl](https://geminiapi.typeform.com/to/Ryq6yl)

This will help us ensure that our API meets your needs.

##### Account Data and Transactions

If you would like to use our API to access data specific to your User Account and its related Gemini Account, such as account balances or transaction history (collectively, “Account Data”), or to perform certain actions, such as placing orders on Gemini, you will need an API key. You can register for an API key here:

[https://exchange.gemini.com/settings/api](https://exchange.gemini.com/settings/api)

##### OEMS Service Providers

If you would like to use our API via an OEMS Service Provider, you may do so pursuant to your User Agreement(s).

You agree and understand that any OEMS Service Provider must first be authorized by us to provide OEMS Services, and such authorization will only be granted by us to an OEMS Service Provider that enters into an OEMS Service Provider Agreement with Gemini. All OEMS Service Providers are subject to the terms and conditions set forth in such OEMS Service Provider Agreement, as well as the terms and conditions set forth in our User Agreement, our API Agreement, and our Market Data Agreement.

If you are an OEMS Service Provider and would like to request our OEMS Service Provider Agreement, please email [bizdev@gemini.com](mailto:bizdev@gemini.com).

##### Request Types

The following chart summarizes our API request types and whether or not they require an API key.

| API Request Type | API Key Required? |
| --- | --- |
| Gemini Market Data | No  |
| Account Data (i.e., account balances, transaction history, pending orders and order status) | Yes |
| Perform actions (i.e., place orders, cancel orders, etc.) | Yes |

##### Request Limits

Subject to the terms and conditions set forth in this API Agreement, you are free to use our API within the following limits:

| API Request Type | Limit |
| --- | --- |
| Public API entry points (i.e., symbol list, public market data, current order book, etc.) | Up to 120 requests per minute |
| Private API entry points (i.e., place orders, cancel orders, account balances, transaction history, pending orders and order status) | Up to 600 requests per minute |

For more information on our rate limiting methodology please see our [API documentation](https://docs.gemini.com/rest-api/#rate-limits). If you require increased limits, please contact us [through this form](https://support.gemini.com/hc/en-us/requests/new).

#### Gemini Market Data

You may use our API to access Gemini Market Data, which is publicly available here:  
[https://docs.gemini.com/](https://docs.gemini.com/)

You agree and understand that your access and use of Gemini Market Data is subject to our Market Data Agreement.

By accessing or using our API, you acknowledge and agree that Gemini Market Data is proprietary to us and protected by applicable intellectual property laws.

#### Authorized Access and Security

When accessing or using our API, you must comply with all of our security policies and procedures at all times. You shall not, and shall not attempt to, reverse-engineer, decompile, disassemble, or otherwise attempt to determine or modify the source code of our API or create any derivative products from our API. Anyone who uses our API to access Account Data or to perform actions on Gemini must authenticate with an API key.

You agree that your login credentials and any other required forms of authentication, where applicable, have been chosen by you, when applicable. You also agree to keep your login credentials and any other required forms of authentication, including your API keys, confidential and separate from each other, as well as separate from any other information or documents relating to your use of Gemini.

You agree and understand that you are solely responsible (and you will not hold us responsible) for managing and maintaining the security of your login credentials and any other required forms of authentication, including your API keys. You further agree and understand that we are not responsible (and you will not hold us responsible) for any unauthorized access to or use of your Gemini account(s).

You agree to accept responsibility for any charges or losses caused as a result of, or in connection with, but not limited to, an Order placed or withdrawal request initiated through our API with your API key.

You agree and understand that you are responsible for monitoring your Gemini account(s). If you notice any unauthorized or suspicious activity in your account or if you believe your API key, your login credentials, any other required forms of authentication, and/or any other account associated with your Gemini account(s) has been compromised, please contact us [through this form](https://support.gemini.com/hc/en-us/requests/new) or email [fraud@gemini.com](mailto:fraud@gemini.com) and notify us immediately.

#### Suspension or Termination

You agree and understand that we may, in our sole discretion, change, suspend, discontinue, or terminate any aspect of our API, or its availability to you, at any time and without notice.

#### Indemnification

You shall indemnify, hold harmless and at your expense defend us, our affiliates, and our and their respective officers, managers, and employees (“Indemnified Persons”) from and against any and all losses, claims, demands, and expenses (including reasonable attorney’s fees of counsel selected by us) arising in connection with any (a) of your or your affiliates’ or, in the case of OEMS Service Providers subject to an OEMS Service Provider Agreement, Subscribers’ (i) breach of this API Agreement, or (ii) willful misconduct or negligence; or (b) in the case of OEMS Service Providers subject to an OEMS Service Provider Agreement, any claim or demand by any Subscriber (or any other Person that receives Gemini Market Data or Derived Data, directly or indirectly, from you or your affiliates) against any Indemnified Person relating to the Gemini Market Data or the use thereof. For the avoidance of doubt, the indemnites set forth in this section are in addition to, and not in place of, those set forth in the User Agreement.

#### Warranties and Limitation of Liability

You represent and warrant that you have the requisite authority to enter into this API Agreement according to its terms, and its performance does not violate any laws, regulations, or agreements applicable to you.

THE API AND GEMINI MARKET DATA IS PROVIDED ON AN “AS IS” BASIS. YOU AND YOUR AFFILIATES DISCLAIM ANY AND ALL EXPRESS OR IMPLIED WARRANTIES, INCLUDING, ANY WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE OR USE, OR OF NON-INFRINGEMENT OR ANY OTHER VIOLATION OF ANY THIRD PARTY INTELLECTUAL PROPERTY RIGHTS. WE AND OUR AFFILIATES DO NOT GUARANTEE OR MAKE ANY WARRANTY CONCERNING THE ACCURACY OR RELIABILITY OF THE API OR ANY GEMINI MARKET DATA, AND DISCLAIM ANY AND ALL LIABILITY (WHETHER IN TORT OR CONTRACT OR OTHERWISE) FOR ANY DIRECT, INDIRECT, INCIDENTAL, SPECIAL, OR CONSEQUENTIAL LOSS OR DAMAGE ARISING FROM ANY INACCURACIES OR OMISSIONS IN, OR ANY DELAY OR LOSS OF ACCESS TO, OR OTHERWISE IN CONNECTION WITH THE USE, STORING, COPYING OR, IN THE CASE OF OEMS SERVICE PROVIDERS SUBJECT TO AN OEMS SERVICE PROVIDER AGREEMENT, REDISTRIBUTION OF, ANY GEMINI MARKET DATA OR THE GEMINI API. 

TO THE MAXIMUM EXTENT PERMITTED UNDER APPLICABLE LAW, AND NOTWITHSTANDING ANY OF THE FOREGOING, WE WILL HAVE NO LIABILITY UNDER THIS API AGREEMENT OR OTHERWISE IN CONNECTION WITH YOUR USE OF THE GEMINI MARKET DATA. FOR THE AVOIDANCE OF DOUBT, THE WARRANTIES AND LIMITATIONS OF LIABILITY SET FORTH IN THIS SECTION ARE IN ADDITION TO, AND NOT IN PLACE OF, THOSE SET FORTH IN THE USER AGREEMENT.

#### Questions

If you have any questions, would like to provide feedback, or would like more information about our API, please feel free to contact us [through this form](https://support.gemini.com/hc/en-us/requests/new).

[Back to all legal agreements](https://www.gemini.com/legal)