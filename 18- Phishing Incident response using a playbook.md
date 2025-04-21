# Alert Ticket - Complete Activity

## Ticket Details

- **Ticket ID:** A-2703  
- **Alert Message:** SERVER-MAIL Phishing attempt possible download of malware  
- **Severity:** Medium  
- **Details:**  
  The user may have opened a malicious email and opened attachments or clicked links.  
- **Ticket Status:** Escalated

---

## Ticket Comments

Based on the information provided in the ticket alert, I’ve decided to escalate the Ticket Status.

The following list includes all the information necessary to justify the escalation:

- **Alert severity:** Medium  
- **Receiver details:** hr@inergy.com — IP: `176.157.125.93`  
- **Sender details:** Suspicious email address with an IP that doesn't seem legitimate  
- **Subject line:** “Re: Infrastructure Egnieer role” — contains spelling errors  
- **Message body:** Contains grammatical errors  
- **Attachments/Links:**  
  - `filename="bfsvc.exe"` has a suspicious name  
  - The file is password protected  
  - The hash of the attachment was identified as malicious using VirusTotal  
  - Reported as: Malware / Backdoor / Trojan

According to the playbook recommendation, the ticket should be escalated and a Level-2 SOC analyst should be notified.

---

## Additional Information

- **Known malicious file hash:**  
  `54e6ea47eb04634d3e87fd7787e2136ccfbcc80ade34f246a12cf93bab527f6b`

---

## Email Details

 - From: Def Communications <76tguyhh6tgftrt7tg.su> <114.114.114.114>
 - Sent: Wednesday, July 20, 2022 09:30:14 AM
 - To: hr@inergy.com <176.157.125.93>
 - Subject: Re: Infrastructure Egnieer role

### Message Body:

> Dear HR at Ingergy,  
>  
> I am writing for to express my interest in the engineer role posted from the website.  
>  
> There is attached my resume and cover letter. For privacy, the file is password protected. Use the password **paradise10789** to open.  
>  
> Thank you,  
>  
> **Clyde West**

- **Attachment:** `bfsvc.exe`

---

