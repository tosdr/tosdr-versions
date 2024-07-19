Privacy Report[¶](#privacy-report "Link to this heading")
=========================================================

We hold personal data about vendors, administrators, clients and other individuals for a variety of purposes. This policy sets out how we seek to protect personal data and ensure that administrators understand the rules governing their use of personal data to which they have access in the course of their work. In particular, this policy requires that the Data Protection Officer (DPO) be consulted before any significant new data processing activity is initiated to ensure that relevant compliance steps are addressed.

Scope[¶](#scope "Link to this heading")
---------------------------------------

This policy applies to all users who have access to any of the personally identifiable data.

Who is responsible for this policy?[¶](#who-is-responsible-for-this-policy "Link to this heading")
--------------------------------------------------------------------------------------------------

As the Data Protection Officer, [Richard Hughes](mailto:richard%40hughsie.com). has overall responsibility for the day-to-day implementation of this policy. The DPO is registered with the Information Commissioner’s Office (ICO) in the United Kingdom as a registered data controller.

Fair and lawful processing[¶](#fair-and-lawful-processing "Link to this heading")
---------------------------------------------------------------------------------

We must process personal data fairly and lawfully in accordance with individuals’ rights. This generally means that we should not process personal data unless the individual whose details we are processing has consented to this happening, or where such collection is unavoidable and/or considered pragmatic in the context, e.g. logging the number of downloads of a particular file.

We do not consider an IP address to represent a single user (due to NAT or VPN use), and as such metadata requests are not considered personal data using the draft GDPR guidelines.

Accuracy and relevance[¶](#accuracy-and-relevance "Link to this heading")
-------------------------------------------------------------------------

We will ensure that any personal data we process is accurate, adequate, relevant and not excessive, given the purpose for which it was obtained. We will not process personal data obtained for one purpose for any unconnected purpose unless the individual concerned has agreed to this or would otherwise reasonably expect this. Individuals may ask that we correct inaccurate personal data relating to them. If you believe that information is inaccurate you should inform the DPO.

Your personal data[¶](#your-personal-data "Link to this heading")
-----------------------------------------------------------------

You must take reasonable steps to ensure that personal data we hold about hardware vendors is accurate and updated as required. For example, if your personal circumstances change, please update them using the profile pages or inform the Data Protection Officer.

Data security[¶](#data-security "Link to this heading")
-------------------------------------------------------

We keep personal data secure against loss or misuse. Where other organizations process personal data as a service on our behalf, the DPO will establish what, if any, additional specific data security arrangements need to be implemented in contracts with those third party organizations.

### Storing data securely[¶](#storing-data-securely "Link to this heading")

All data is stored electronically. All documents and code are held on a locked LUKS partition with a password adhering to security best practices.

### Data retention[¶](#data-retention "Link to this heading")

We must retain personal data for no longer than is necessary. What is necessary will depend on the circumstances of each case, taking into account the reasons that the personal data was obtained, but should be determined in a manner consistent with our data retention guidelines. Anonymized user data (e.g. metadata requests) will be kept for a maximum of 5 years which allows us to project future service requirements and provide usage graphs to the vendor.

### Transferring data internationally[¶](#transferring-data-internationally "Link to this heading")

There are restrictions on international transfers of personal data. We do not transfer personal data anywhere outside the EU without the approval of the Data Protection Officer, unless required to do so by law.

Subject Access Requests[¶](#subject-access-requests "Link to this heading")
---------------------------------------------------------------------------

Please note that under the Data Protection Act 1998, individuals are entitled, subject to certain exceptions, to request access to information held about them.

On receiving a subject access request, we will refer that request immediately to the DPO. We may ask you to help us comply with those requests. Please also contact the Data Protection Officer if you would like to correct or request information that we hold about you. There are also restrictions on the information to which you are entitled under applicable law.

Processing data[¶](#processing-data "Link to this heading")
-----------------------------------------------------------

We will never use identifiable vendor data for direct marketing purposes.

GDPR Provisions[¶](#gdpr-provisions "Link to this heading")
-----------------------------------------------------------

Where not specified previously in this policy, the following provisions will be in effect on or before 11 November 2020.

Transparency of data protection[¶](#transparency-of-data-protection "Link to this heading")
-------------------------------------------------------------------------------------------

Being transparent and providing accessible information to individuals about how we will use their personal data is important for our project. The following are details on how we collect data and what we will do with it:

### Firmware Vendor Information[¶](#firmware-vendor-information "Link to this heading")

* **What:** The hardware vendor name, password, GPG public key and content of original uploaded firmware files.
    
* **Why collected:** Secure authentication, to allow any possible future audit and to provide authorized users access to signed firmware files.
    
* **Where stored:** AWS hosted PostgreSQL database in Oregon, USA region.
    
* **When copied:** Full backups weekly, with daily snapshots both to AWS backup.
    
* **Who has access:** The hardware vendor (filtered by the QA group), Linux Foundation Infrastructure Team and the DPO.
    
* **Wiped:** When the vendor requests deletion of the user account.
    

### Service Event Log[¶](#service-event-log "Link to this heading")

* **What:** IP address (unhashed) and REST method requested, along with any error.
    
* **Why collected:** Providing an event log for checking what the various hardware vendors are doing, or trying to do.
    
* **Where stored:** AWS hosted PostgreSQL database in Oregon, USA region.
    
* **When copied:** Full backups weekly, with daily snapshots both to AWS backup.
    
* **Who has access:** The hardware vendor (filtered by the QA group), Linux Foundation Infrastructure Team and the DPO.
    
* **Wiped:** When the QA group is deleted.
    

### Firmware Download Log[¶](#firmware-download-log "Link to this heading")

* **What:** IP address, timestamp, filename of firmware, user-agent of client.
    
* **Why collected:** To know what client versions are being used for download, and to provide a download count over time for a specific firmware file.
    
* **Where stored:** AWS hosted PostgreSQL database in Oregon, USA region.
    
* **When copied:** Full backups weekly, with daily snapshots both to AWS backup.
    
* **Who has access:** The hardware vendor (filtered by the QA group), Linux Foundation Infrastructure Team and the DPO.
    
* **Wiped:** When the firmware is deleted, but the client IP address is cleared after 3 years.
    

### Firmware Reports[¶](#firmware-reports "Link to this heading")

* **What:** IP address, Machine ID (hashed), failure string and checksum of failing file, OS distribution name and version.
    
* **Why collected:** Allows the hardware vendor to assess if the firmware update is working on real hardware.
    
* **Where stored:** AWS hosted PostgreSQL database in Oregon, USA region.
    
* **When copied:** Full backups weekly, with daily snapshots both to AWS backup.
    
* **Who has access:** The hardware vendor (filtered by the QA group), Linux Foundation Infrastructure Team and the DPO.
    
* **Wiped:** When the firmware is deleted.
    

We will ensure any use of personal data is justified using at least one of the conditions for processing and this had been specifically documented above.

Consent[¶](#consent "Link to this heading")
-------------------------------------------

The data that we collect is subject to active consent by the data subject. This consent can be revoked at any time. Revoking consent to use data ends any vendor relationship with the LVFS.

Data portability[¶](#data-portability "Link to this heading")
-------------------------------------------------------------

Upon request, a data subject should have the right to receive a copy of their data in a structured format, typically an SQL export. These requests should be processed within one month, provided there is no undue burden and it does not compromise the privacy of other individuals. A data subject may also request that their data is transferred directly to another system. This is available for free.

Right to be forgotten[¶](#right-to-be-forgotten "Link to this heading")
-----------------------------------------------------------------------

A vendor may request that any information held on them is deleted or removed, and any third parties who process or use that data must also comply with the request. An erasure request can only be refused if an exemption applies.

Privacy by design and default[¶](#privacy-by-design-and-default "Link to this heading")
---------------------------------------------------------------------------------------

Privacy by design is an approach to projects that promote privacy and data protection compliance from the start. The DPO will be responsible for conducting Privacy Impact Assessments and ensuring that all changes commence with a privacy plan. When relevant, and when it does not have a negative impact on the data subject, privacy settings will be set to the most private by default.

Data audit and register[¶](#data-audit-and-register "Link to this heading")
---------------------------------------------------------------------------

Regular data audits to manage and mitigate risks will inform the data register. This contains information on what data is held, where it is stored, how it is used, who is responsible and any further regulations or retention timescales that may be relevant.

Reporting breaches[¶](#reporting-breaches "Link to this heading")
-----------------------------------------------------------------

All users of the LVFS have an obligation to report actual or potential data protection compliance failures. This allows us to:

* Investigate the failure and take remedial steps if necessary
    
* Maintain a register of compliance failures
    
* Notify the Supervisory Authority (SA) of any compliance failures that are material either in their own right or as part of a pattern of failures
    

Please refer to the DPO for our reporting procedure.

Monitoring[¶](#monitoring "Link to this heading")
-------------------------------------------------

Everyone who actively uses the LVFS must observe this policy. The DPO has overall responsibility for this policy. They will monitor it regularly to make sure it is being adhered to.

Consequences of Failing to Comply[¶](#consequences-of-failing-to-comply "Link to this heading")
-----------------------------------------------------------------------------------------------

We take compliance with this policy very seriously. Failure to comply puts both you and us at risk. The importance of this policy means that failure to comply with any requirement may lead to disciplinary action under our procedures. If you have any questions or concerns about anything in this policy, do not hesitate to contact the DPO.

[LVFS](https://lvfs.readthedocs.io/en/latest/index.html)
========================================================

### Navigation

Contents:

* [Introduction](https://lvfs.readthedocs.io/en/latest/intro.html)
* [Getting an Account](https://lvfs.readthedocs.io/en/latest/apply.html)
* [Metadata](https://lvfs.readthedocs.io/en/latest/metainfo.html)
* [Uploading Firmware](https://lvfs.readthedocs.io/en/latest/upload.html)
* [Downloading Firmware](https://lvfs.readthedocs.io/en/latest/download.html)
* [Firmware Testing](https://lvfs.readthedocs.io/en/latest/testing.html)
* [Claims](https://lvfs.readthedocs.io/en/latest/claims.html)
* [User Telemetry](https://lvfs.readthedocs.io/en/latest/telemetry.html)
* [Custom Protocol](https://lvfs.readthedocs.io/en/latest/custom-plugin.html)
* [Security](https://lvfs.readthedocs.io/en/latest/security.html)
* [Privacy Report](#)
    * [Scope](#scope)
    * [Who is responsible for this policy?](#who-is-responsible-for-this-policy)
    * [Fair and lawful processing](#fair-and-lawful-processing)
    * [Accuracy and relevance](#accuracy-and-relevance)
    * [Your personal data](#your-personal-data)
    * [Data security](#data-security)
    * [Subject Access Requests](#subject-access-requests)
    * [Processing data](#processing-data)
    * [GDPR Provisions](#gdpr-provisions)
    * [Transparency of data protection](#transparency-of-data-protection)
    * [Consent](#consent)
    * [Data portability](#data-portability)
    * [Right to be forgotten](#right-to-be-forgotten)
    * [Privacy by design and default](#privacy-by-design-and-default)
    * [Data audit and register](#data-audit-and-register)
    * [Reporting breaches](#reporting-breaches)
    * [Monitoring](#monitoring)
    * [Consequences of Failing to Comply](#consequences-of-failing-to-comply)
* [Offline Firmware](https://lvfs.readthedocs.io/en/latest/offline.html)
* [Product Certification](https://lvfs.readthedocs.io/en/latest/prodcert.html)
* [LVFS Releases](https://lvfs.readthedocs.io/en/latest/news.html)
* [Firmware Embedded SBoM Specification](https://lvfs.readthedocs.io/en/latest/sbom.html)
* [ChromeOS firmware testing](https://lvfs.readthedocs.io/en/latest/chromeos.html)
* [How to run fwupd tests with Moblab](https://lvfs.readthedocs.io/en/latest/moblab.html)

### Related Topics

* [Documentation overview](https://lvfs.readthedocs.io/en/latest/index.html)
    * Previous: [Security](https://lvfs.readthedocs.io/en/latest/security.html "previous chapter")
    * Next: [Offline Firmware](https://lvfs.readthedocs.io/en/latest/offline.html "next chapter")

### Quick search 

©2016-2020, Richard Hughes.