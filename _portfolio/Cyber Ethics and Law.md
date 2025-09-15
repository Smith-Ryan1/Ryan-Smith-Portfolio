---
title: "Cyber Ethics And Law"
excerpt: "A collection of Assignments from my Cyber Ethics and Law class at Hocking College"
collection: portfolio
---


# OSS and Disclosure Readiness
### License choice
I believe if I were to choose a open source license I would choose Apache. I feel it is the most middle ground of the three, requiring you to distribute changes to the source code while keeping patents. The original creators of works should see some sort of benifit from what they do, however, information should be readilly available and easy to access. 

### SIV (Safe Initial Vulnerability) Report
[reporting template.docx](https://github.com/user-attachments/files/22142433/reporting.template.docx)

The template provided is a rephrasing of the template provided by cisa.gov at https://www.cisa.gov/vulnerability-disclosure-policy-template?utm_source=chatgpt.com I have simply reworded most parts into a more re-constructable phrasing for future use. Most of the information provided by the template was perfectly applicable, if a bit wordy.

### Artifacts
[Weekly reflection- wk3- SmithRyan (1).docx](https://github.com/user-attachments/files/22143106/Weekly.reflection-.wk3-.SmithRyan.1.docx)
[Open Source, Closed Eyes- Case breif 3- SmithRyan.docx](https://github.com/user-attachments/files/22143109/Open.Source.Closed.Eyes-.Case.breif.3-.SmithRyan.docx)

### Whats next?
I want to look more deeply at some of the different creative commons licenses as that seems to be a mess within itself. However, with the symbol system it uses it should not be too hard to differentiate the nuancies of each licence. I can only see me learning more about different copyleft and right policys as a benifit as I do not know when, not if but when, I will use open source material and I wish to attribute properly.

# Incident responce and evidence notes

### First hour priorities
During the first hour, you are trying to minimize damage as much as possible and then gather information about why this happened. My first priority is containment, find the infiltrator, close off any possible in points it could have, then close off its exits, trap it, contain it to one place. Figure out why it is here, what it was attempting to do, make sure there is no damage caused to the machine. Every bit of knowledge about a potentially reoccuring threat is helpful knowledge. 

## Artifact: Incident and evidence response note
• Incident # 55671

• Timestamp (UTC) & Context: [2025-09-11 09:08 UTC] — Initial incident declaration: notified by [Sam Rivera/ Chief security analyst] that [Phishing emails were sent to staff to collect login credentials, using a fake dev webinar login ]. Ticket created with [Phishing]. 

• Authorization: [Sam Rivera / Chief security analyst] approved [blacklisting the sender] on [email services] for [four weeks, or until the email address provides non-malicious traffic].

• Actions Taken: Ran [traceroute] on [PC 1]; collected [port of entry for malicious email]; isolated [PC 1] per approval 

• Evidence Captured: Item [email file] — SHA-256: [1b6ffed2deb904d1b42aa7072f1cb3c604f2aa8a3f85b4f2021121fc3837caae] — Why: [Email is directly linked to possible security breach as main culprit] 

• Chain of Custody: Stored at [PC Alpha]; access: [Sam Rivera/ 09:09, John Smith / 10:01]; transfer records kept. 

• Redaction: no redactions made, should one need to be made, keep an unredacted file. 

• Next Step: Recommend [ensure emails cannot be received from sender, ensure staff is aware to not share login credentials to sender] (handoff to Upper management staff)

##Integrity and privacy controls
Hash can be utilized for artifacts to make sure changes that people say happened, actually do, and hold accountability for any unauthorized actions that took place. Store them in a very secure enviroment, so that only those with authorization can access the files, let alone change them. Redactions should occur on things that are not 100% nessesary, or out of scope. PII and such would just bog down the investigation.

##Reflection
I want to look over some professional examples of first hour priorities in businesses, ultimately if I wish to be in this field I need to learn how to thing link a professional. That being said I do not believe my priorities are bad, knowledge is power, attacks are repeated. If you know everything there is to know about how to identify an attack, you can prevent it before anything bad happens. However, I would still like to learn more professional vocabulary to better refine my priority list. 

