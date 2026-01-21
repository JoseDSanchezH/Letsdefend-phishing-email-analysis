# Letsdefend-phishing-email-analysis


## Objective 


The goal of this lab is to analyze a suspicious email claiming to be from **PayPal (in German)** and determine whether it is malicious by examining email headers, URLs, and indicators of compromise (IOCs).
This project simulates a SOC analyst email investigation workflow, focusing on phishing detection and incident triage.


# Phishing Email Analysis – LetsDefend Challenge
---

## 🧪 Challenge Information

- **Challenge Name:** Phishing Email  
- **Platform:** LetsDefend  
- **Prepared by:** @Fuuji  
- **Scenario:**  
  > Your email address has been leaked, and you received an email from PayPal written in German. Analyze the suspicious email.

- **File Location:**  
"C:\Users\LetsDefend\Desktop\Files\PhishingChallenge.zip"

I logged into the users desktop and was able to locate the file. I had to extract the Zip file and then open it. I used the -zip option to extract the file and then entered the password. 
<img width="900" height="438" alt="image" src="https://github.com/user-attachments/assets/b6fed61d-67e8-401b-a43e-e92973edb396" />

<img width="576" height="514" alt="image" src="https://github.com/user-attachments/assets/31ae84e1-e0bb-47b1-b5b7-0260e518cf2a" />

<img width="802" height="540" alt="image" src="https://github.com/user-attachments/assets/9d8ac73b-0758-4987-8204-cc4438265da4" />


I was able to open the file and view the email. From the "From" field, I can see this email came from "IHKH0MFEWW@kodehexa.net". 
To: "[an18]"@itlgopk.uk
The Date: 8/15/2022, 2:35 PM

<img width="942" height="732" alt="image" src="https://github.com/user-attachments/assets/66627ff2-d12d-4f67-ac75-a20b746e6d93" />


A red flag is the email, as it did not come from PayPal and has two different intended recipients. The Subject is another red flag that the user should have noticed. 
One more red flag, if I hover over the links from the email, it redirects me to a storage.google page. 

<img width="1020" height="806" alt="image" src="https://github.com/user-attachments/assets/f9551e2a-4d2d-4f85-8929-20d686ccc7bb" />


I want to know more about the email itself. I clicked on More on the right-hand side and selected "View Source". 

<img width="680" height="546" alt="image" src="https://github.com/user-attachments/assets/030a5afb-4f89-4d48-ac31-74590a419512" />


### 1️⃣ What is the return path of the email?
*bounce@rjttznyzjjzydnillquh.designclub.uk.com*
<img width="1088" height="736" alt="image" src="https://github.com/user-attachments/assets/02b45ee6-99f6-4b6d-9321-c0bb2ebd0a48" />


### 2️⃣ What is the domain name of the URL in this mail?
*storage.googleapis.com*

<img width="792" height="72" alt="image" src="https://github.com/user-attachments/assets/5ecf7d06-b486-4166-ad8a-e6d1476c6625" />



### 3️⃣ Is the domain mentioned in the previous question suspicious?
Yes



### 4️⃣ What is the body SHA-256 hash of the domain?

*13945ecc33afee74ac7f72e1d5bb73050894356c4bf63d02a1a53e76830567f5*

I went on VirusTotal.com and looked up the URL of the return path I found. I went to the details tab to find out more information. 

<img width="1710" height="934" alt="image" src="https://github.com/user-attachments/assets/90dfa0b8-e428-46bc-9ed0-b71e9359ad27" />


### 5️⃣ Is this email a phishing email?
*Yes*

Based on header analysis, sender impersonation, suspicious redirection behavior, and threat intelligence findings, this email meets the criteria for a phishing attack and poses a risk of credential theft and financial fraud.



## 🛠️ Recommended Response Actions

- Block the malicious domains at the email gateway
- Remove the email from all affected mailboxes
- Reset credentials if user interaction occurred
- Educate users on identifying PayPal phishing attempts


