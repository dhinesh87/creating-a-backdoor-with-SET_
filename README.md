# creating-a-backdoor-with-SET
creating a backdoor with SET - Ethical Hacking Techniques course

# AIM:
To Create a backdoor with Social Engineering Toolkit (SET)

## DESIGN STEPS:

### Step 1:

Install kali linux either in partition or virtual box or in live mode


### Step 2:

Investigate on the various categories of tools as follows:

### Step 3:

Open terminal and try execute some kali linux commands

### Architecture Diagram

```
+----------------+        +------------------------+        +----------------------+
| Attacker's PC  | -----> | SET (Credential        | -----> | Fake Login Page      |
| (Kali Linux)   |        | Harvester via Apache)  |        | (Hosted by SET)      |
+----------------+        +------------------------+        +----------------------+
       |                                                             |
       |                                                             v
       |   1. Configure SET with phishing site (e.g., Gmail clone)   |
       |                                                             |
       |                                                             v
       |                                                 +----------------------+
       |                                                 | Victim's Browser     |
       | <------------------------------------------------| Clicks Phishing Link|
       |                                                 +----------------------+
       |                                                             |
       |                                                             v
       |     2. Victim Enters Credentials → Sent to SET/Attacker    |
       |                                                             |
       |                                                             v
       |                                                 +----------------------+
       |                                                 | Credentials Captured |
       |                                                 | in Apache log/SET DB |
       |                                                 +----------------------+

```

## EXECUTION STEPS AND ITS OUTPUT:
Social Engineering attacks are the various cons used by the hackers to trick people into providing sensitive data to the attackers.

**Steps to Use SET for Phishing (Credential Harvester Attack Method)**

**1. Open terminal:**
```bash
sudo setoolkit
```
<img width="938" height="834" alt="image" src="https://github.com/user-attachments/assets/21253856-ebbb-4078-a6f5-61b36e41a91b" />

**2. Navigate:**
```bash
1) Social-Engineering Attacks  
2) Website Attack Vectors  
3) Credential Harvester Attack Method  
```
<img width="957" height="720" alt="image" src="https://github.com/user-attachments/assets/0c5282b2-792f-40d1-a536-7cd52de019a6" />
<img width="851" height="777" alt="image" src="https://github.com/user-attachments/assets/4b092420-6016-42ef-b668-abcc2840664d" />


**3. Enter your IP address as the attacker server.**
**4. Choose:**
```bash
2) Site Cloner
```
<img width="911" height="388" alt="Screenshot 2025-10-03 193158" src="https://github.com/user-attachments/assets/23a05281-e25e-4784-9ab2-eeca33449c63" />


**5. Enter the URL of the legitimate site ```(e.g., https://accounts.google.com)```**
<img width="931" height="331" alt="Screenshot 2025-10-03 193023" src="https://github.com/user-attachments/assets/8331990b-4741-4b1c-9a29-479a5853d8f7" />



**6. Send the generated link to the victim.**

<img width="913" height="670" alt="Screenshot 2025-10-03 191805" src="https://github.com/user-attachments/assets/39b60b56-78d1-44f8-9fa0-f8d3a37c3105" />


**7. Once the victim logs in → their credentials are stored in:**
```bash
/var/www/html/
```


<img width="902" height="337" alt="Screenshot 2025-10-03 191839" src="https://github.com/user-attachments/assets/85d6f64e-2147-4195-b183-0d2ae9a909fd" />


## RESULT:
The Social Engineering Toolkit (SET) is used to create backdoor is  examined successfully
