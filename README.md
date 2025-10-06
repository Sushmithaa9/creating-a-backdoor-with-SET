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
<img width="987" height="973" alt="image" src="https://github.com/user-attachments/assets/30d7f381-e8e8-4b94-aa89-f1f12d03a806" />


**2. Navigate:**
```bash
1) Social-Engineering Attacks  
2) Website Attack Vectors  
3) Credential Harvester Attack Method  
```
<img width="1915" height="702" alt="image" src="https://github.com/user-attachments/assets/80e157b1-5a11-4f0a-8022-a5238c0aa83f" />

<img width="918" height="652" alt="image" src="https://github.com/user-attachments/assets/81a76ba1-5e6b-4d09-ae8c-60c084b140bf" />

**3. Enter your IP address as the attacker server.**
**4. Choose:**
```bash
2) Site Cloner
```
<img width="799" height="161" alt="image" src="https://github.com/user-attachments/assets/ed2ec62d-b29b-4875-99f7-2753ef7bdd01" />

**5. Enter the URL of the legitimate site ```(e.g., https://accounts.google.com)```**

<img width="1280" height="720" alt="image" src="https://github.com/user-attachments/assets/03fef797-e651-4f69-9206-51cd1f4e1411" />



**6. Send the generated link to the victim.**

**7. Once the victim logs in → their credentials are stored in:**
```bash
/var/www/html/
```

<img width="716" height="301" alt="image" src="https://github.com/user-attachments/assets/2fdeaa33-1401-47da-86ec-bdc52beb1877" />



## RESULT:
The Social Engineering Toolkit (SET) is used to create backdoor is  examined successfully
