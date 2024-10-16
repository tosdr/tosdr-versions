[](https://www.planningcenter.com/)Menu

[](https://www.planningcenter.com/)![](/images/header/icon-close.svg)

* Products
* Resources
* Use cases
* [What’s new](https://www.planningcenter.com/blog)
* [Pricing](https://www.planningcenter.com/pricing)

[Sign up](https://www.planningcenter.com/pricing)[Log in](https://login.planningcenteronline.com/)

Back![](/images/header/icon-close.svg)

[](https://www.planningcenter.com/)

Products

People & Communication

* [people
    
    Free membership database](https://www.planningcenter.com/people)
* [groups
    
    Community engagement & chat](https://www.planningcenter.com/groups)

Events

* [calendar
    
    Scheduling, facilities, & resources](https://www.planningcenter.com/calendar)
* [registrations
    
    Signups, tickets, & payments](https://www.planningcenter.com/registrations)
* [check-ins
    
    Attendance & volunteer tools](https://www.planningcenter.com/check-ins)

Worship & Teams

* [services
    
    Worship planning & scheduling](https://www.planningcenter.com/services)
* [music stand
    
    Digital sheet music & chord charts](https://www.planningcenter.com/music-stand)

Mobile App & Website

* [church center
    
    Custom mobile app for your church](https://www.planningcenter.com/church-center)
* [publishing
    
    Custom pages, video, & audio library](https://www.planningcenter.com/publishing)

Donations

* [giving
    
    Tithes, offerings, & reporting](https://www.planningcenter.com/giving)

more

* [Integrations
    
    Products that work with ours](https://www.planningcenter.com/integrations)
* [Get Giving free for 12 months
    
    Apply for 12 months free](https://www.planningcenter.com/giving/free)

Resources

Learn & get help

* [Support
    
    Helpful responses in ~1 hour](https://www.planningcenter.com/support)
* [Training
    
    Learn how to use the system](https://www.planningcenter.com/training)
    * [Planning Center University videos](https://www.planningcenter.com/university)
    * [How-to articles](https://www.planningcenter.com/blog/tags/tips-and-tricks/1)
* [Community
    
    Connect with customers on Facebook or Slack](https://www.planningcenter.com/community)

Switch to Planning Center

* [Compare systems
    
    How we can replace your current solution](https://www.planningcenter.com/compare-planning-center-to-other-systems)
* [Calculate savings
    
    See how much you’ll save on giving fees](https://www.planningcenter.com/processing-fee)
* [Getting started
    
    A roadmap to migration](https://www.planningcenter.com/getting-started)

Use Cases

* [Church planters
    
    Apply for 6 months free](https://www.planningcenter.com/use-cases/church-planters)
* [Children’s ministry
    
    Care for families & volunteers](https://www.planningcenter.com/use-cases/childrens-ministry)
* [Church management system
    
    Equip your team, support your church](https://www.planningcenter.com/use-cases/chms)

[What’s new](https://www.planningcenter.com/blog)[Pricing](https://www.planningcenter.com/pricing)

[Sign up](https://www.planningcenter.com/pricing)[Log in](https://login.planningcenteronline.com/)

Security
========

Artboard 8

[Terms of Service](https://www.planningcenter.com/terms)[Privacy Policy](https://www.planningcenter.com/privacy)[Congregant Privacy](https://www.planningcenter.com/congregant-privacy)[GDPR](https://www.planningcenter.com/gdpr)[Security](https://www.planningcenter.com/security)

* [Overview](#overview)
* [SOC 2 Type 2 Certified](#section1)
* [PCI Compliance](#section2)
* [Technical Security and Encryption](#section3)
* [Secure Coding Practices](#section4)
* [Data Durability and Recovery](#data-durability-and-recovery)
* [Security Bug Bounty](#section5)
* [Physical Security](#section6)
* [Local Equipment Security](#section7)
* [Personnel Security](#section8)
* [Security Culture](#section9)
* [Questions](#section10)

### Security, Compliance, Practices, and Procedures at Planning Center

The security of your data and the personal information of your congregation matters deeply to us, and we’re committed to protecting it. Here we outline the physical and technical procedures we use to ensure your data is kept safe, and the external certifications and audits we comply with to verify our practices.

SOC 2 Type 2 Certified
----------------------

Planning Center is SOC 2 Type 2 certified. The American Institute of Certified Public Accountants (AICPA) created the Service Organization Control (SOC 2) framework to test organizations’ ability to protect data from potential threats.

To pass SOC 2, we worked with an AICPA-approved auditor, [Johanson Group](https://www.johansonllp.com/), to critique our company based on five areas: security, availability, processing integrity, confidentiality, and privacy. This audit included a review of our policies, backup and disaster recovery, incident response, firewall configurations, and other critical areas of our business. After completing the audit, we received an Auditor’s Report, proving Planning Center meets and exceeds the SOC 2 criteria. [We can provide the full report upon request.](https://pcoprivacy.churchcenter.com/people/forms/411901)

PCI Compliance
--------------

The [Payment Card Industry Data Security Standards](https://en.wikipedia.org/wiki/Payment_Card_Industry_Data_Security_Standard) (PCI DSS, or more commonly, PCI) are a set of standards set forth by the four major card associations to protect cardholder data. All merchants and processors need to have physical, electronic, and procedural controls in place to ensure that cardholder data is stored and handled securely at all times.

**Planning Center is a PCI Level One compliant merchant.**

Our payment processor, [Stripe](https://stripe.com/), is one of the largest, most advanced payment processors in the world. They handle payment processing for services like Kickstarter, Lyft, Shopify, Pinterest, Twitter, Heroku, SurveyMonkey, and [many other](https://stripe.com/gallery) companies. Stripe is also [a certified](https://www.visa.com/splisting/searchGrsp.do?companyNameCriteria=stripe,%20inc) "PCI Service Provider Level 1" payment processor.

Technical Security and Encryption
---------------------------------

Whenever your data is in transit between you and us, everything is sent encrypted over HTTPS, and our databases utilize encryption at rest. We limit brute force attacks with rate limiting, and all passwords are filtered from all our logs and are one-way encrypted using industry standard bcrypt.

Secure Coding Practices
-----------------------

We hire the best developers we can find. Since so many security exploits take advantage of coding errors, part of security is having well-tested, well-reviewed code. At Planning Center, code changes are reviewed by teammates, ran against an automated testing framework, and in most cases, manually QA’d. By the time new code is running on our production environments it has had lots of eyeballs on it. Developing this way means that it takes more time to get things done, but it also means that fewer mistakes get by.

Data Durability and Recovery
----------------------------

We employ a multilayered backup strategy that is designed to be resilient to hardware failure, regional disasters, and malicious acts. Both point in time backups and daily snapshots are available for use in recovery.

Security Bug Bounty
-------------------

We run an ongoing bounty program through [HackerOne](https://hackerone.com/) to provide penetration testing across all of our products. These security researchers are some of the best in the world at finding vulnerabilities and responsibly disclosing them.

Our bounty program is open to anyone who finds a security vulnerability. To report a vulnerability, please start by requesting an invite to our program by email at [hackerone@planningcenter.com](mailto:hackerone@planningcenter.com). Our average response time is less than one day.

Physical Security
-----------------

All of your data is stored in AWS data centers, which use industry leading practices in physical security, redundancy, and availability. You can learn more about Amazon's data centers [here](https://aws.amazon.com/compliance/data-center/controls/).

Local Equipment Security
------------------------

At the most basic level, our main physical space is locked and alarmed during off hours. In the event of a break-in, we may lose some expensive monitors, but since our servers don't reside in our buildings, they aren't vulnerable to smash-and-grab robberies. Local computers are password protected and encrypted. In the course of conducting customer support, employees access customer data using an encrypted connection and must invoke a time-based one-time password upon connection.

Personnel Security
------------------

Planning Center is a small company, so thankfully we are able to hire some brilliant people who care about its success. Our employee turnover is extremely low (especially for the tech industry). To protect company data, including customer data, all employees sign a non-disclosure agreement when hired.

Security Culture
----------------

Lastly, a word about the culture here in general. Most of us who work at Planning Center are also users of our software. Our personal data is in the same database as our customers. We've checked-in our children using [Planning Center Check-Ins](https://www.planningcenter.com/check-ins/) at our own churches. We've donated to our churches using [Planning Center Giving](https://www.planningcenter.com/giving/). We protect your data like it’s our data because it is our data.

Questions
---------

If you have any questions that weren't addressed on this page, please don't hesitate to ask by emailing us at [support@planningcenter.com](mailto:support@planningcenter.com).

[](https://www.planningcenter.com/)

Get updates delivered to your inbox!

* [](https://twitter.com/PlanningCenter)
* [](https://www.facebook.com/PlanningCenter)
* [](https://www.instagram.com/PlanningCenter)
* [](https://youtube.com/PlanningCenter)

* Products
    
    * [Calendar](https://www.planningcenter.com/calendar)
    * [Check-ins](https://www.planningcenter.com/check-ins)
    * [Giving](https://www.planningcenter.com/giving)
    * [Groups](https://www.planningcenter.com/groups)
    * [People](https://www.planningcenter.com/people)
    * [Publishing](https://www.planningcenter.com/publishing)
    * [Registrations](https://www.planningcenter.com/registrations)
    * [Services](https://www.planningcenter.com/services)
    * [Music Stand](https://www.planningcenter.com/music-stand)
    * [Church Center](https://www.planningcenter.com/church-center)

* Resources
    
    * [Support](https://www.planningcenter.com/support)
    * [Training](https://www.planningcenter.com/training)
    * [Planning Center University](https://www.planningcenter.com/university)
    * [Getting Started](https://www.planningcenter.com/getting-started)
    * [Community](https://www.planningcenter.com/community)

* Use cases
    
    * [Church Plants](https://www.planningcenter.com/use-cases/church-planters)
    * [Children’s Ministry](https://www.planningcenter.com/use-cases/childrens-ministry)
    * [Church Management System](https://www.planningcenter.com/use-cases/chms)

* How we compare
    
    * [See Processing Fee Savings](https://www.planningcenter.com/processing-fee#calculate-fees)
    * [Compare Pushpay](https://www.planningcenter.com/compare-planning-center-vs-pushpay)
    * [Compare Tithe.ly](https://www.planningcenter.com/compare-planning-center-vs-tithely)
    * [Compare Breeze](https://www.planningcenter.com/compare-planning-center-vs-breeze)
    * [Compare ChurchTrac](https://www.planningcenter.com/compare-planning-center-vs-churchtrac)

* Company
    
    * [About us](https://www.planningcenter.com/about)
    * [Careers](https://www.planningcenter.com/careers)
    * [Developers](https://www.planningcenter.com/developers)
    * [Logos](https://www.planningcenter.com/logos)
    * [Terms of Service](https://www.planningcenter.com/terms)
    * [Privacy Policy](https://www.planningcenter.com/privacy)

* [Pricing](https://www.planningcenter.com/pricing)
* [Changelog](https://www.planningcenter.com/changelog)
* [Blog](https://www.planningcenter.com/blog)
* [Security](https://www.planningcenter.com/security)
* [Status](https://status.planningcenter.com/)
* [Downloads](https://www.planningcenter.com/check-ins/download)
* [Apply for a free  
    Giving subscription](https://www.planningcenter.com/giving/free)

![AICPA SOC](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2Fsoc.9c0606b4.png&w=96&q=90)

[Terms of Service](https://www.planningcenter.com/terms)[Privacy Policy](https://www.planningcenter.com/privacy)