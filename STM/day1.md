# DAY 1  19/11/24
# Intro to Information Security:


We must understand terms:

## 1. Information Security[ InfoSec ]:

**What is Information:** [Differ b/w Info & Data]
   - Meaningful form of data
   - Can be called as processed data
   - Data has no context, info does
**Example**
-  Computer is data
-  This is my computer is information





---

**NOTE:** Information in digital systems makes cyber security [Information involving cyber space].

---
## 2. Information Security Threats:

- Threat is a constant danger to an asset
- It can be a person, object or an event
- Threat can be categorized and ranked

**Type of Threats :**

- Inadvertent Threat	[ Human Failure ]
- Physical Threat 	[ Natural disasters ]
- Technical Failure	[ Hardware / Software ]
- Deliberate acts	[ Hacking / Espionage->related to spy ]





## 3. Introduction to Cyber Security:
**Information Security does not deal with?**

- Cyber Warfare		[Govt Web Hacks, DDOS, etc.]
- Information Warfare	[Intel]
- Negative Impact of people on Internet ( sexual abuse, cyber stalking, etc. )
- IoT Security

Then who deal with them?

**Cyber Security:**

- Protection of Cyber Space against Cyber Threats and Cyber Space vulnerabilities.
- Any threats to Information via Cyber Space
- Deal with Deliberate acts
- Doesn't deal with physical and personal security
- Threats via Cyber Space, not threats for Cyber Space.

**Objective of Cyber Security:**
- **Confidentiality:** No telling to unauthorized parties
- **Integrity:** Completeness and accuracy of data
- **Availability:** When needed, data is available
- **Non-repudiation:** I should accept i sent you the message and you should accept you received it.
- **Authenticity:** You should actually be who you tell you are




## Confidentiality
The concealment of information or resources

* Applies to content and existence 
* Supported by access contorl mechanism:
   - Cryptography and Stegganoraphy 
   - File permissions 
   - Whitelists / Blacklists 
* Enforcement relies on system services (e.g. Kernel)
   - Assumptions and Trust

## Integrity
The trustworthiness of data  or resources. 

* Data:Integrity and origin integrity 
   - Origin -> "Authentication" 
   - Impacts creedibility 
* Prevention mechanisms and detection mechanisms
   - **Prevention:** block unauthorized changes to the data 
   - **detection:** report loss of trustworthine of data's integrity

* Correctness and trustworthiness
   - Origin, Transmission, storage

## Availability
The ability to use the information or resource desired.

* An Unavilabe system is at least as bad as no system at all 
   - Reliability
   - Example: compromised secondary,unavailable primary 

* Denial of service (Dos, DDos)
   - Attempts to block availability 
   - Difficult to detect and distinguish



### The Basics: Threats and Attacks 

- **Threat:** potential violation of security  
- **Attacks:** actions that cause violations of security. 
- **Attackers:** those who execute attacks. 
- **Assets:** the objects of attack. 


**4 classes of threat:**
- **Disclosure:** unauthorized access to information 
- **Deception:** acceptance of false data
- **Disruption:** interrupton or prevention of correct operation 
- **Usurpation:** unauthorized control


# Garden Variety Threats
 - Snopping 
 - Modification or Alteration
 - Masquerading or Spoofing 
 - Repudiation of Origin 
 - Denial of Receipt 
 - Delay 
 - Denial Of service 
 
Cause and Result are important, Intention is not. 

## Snooping 
 - unauthorized access to information 
 - Packet sniffers and wiretappears 
 - Illicit copying of files and programs

  ![image](https://github.com/user-attachments/assets/7e85c5cd-f6a5-4743-a197-75ce570f6010)



## Modification

- Stop the flow of message 
- Delay and optionally modify the message 
- Release the message again

![image](https://github.com/user-attachments/assets/b605eb6b-9699-4449-b5f7-d14e2f925a0f)


## Spoofing

-  Unauthorized assumption of other's identity
-  Generate and distribute objects under this identity

![image](https://github.com/user-attachments/assets/24110247-7b3c-4511-8c74-ca12d9135244)


## Delay and Denial of Service  

* Destroy hardware (cuttig fiber) or software
* Modify software in a subtle way (alias commands)
* Corrupt packets in transist

  ![image](https://github.com/user-attachments/assets/a0affe6f-113f-48de-a2de-d0ca063e2b2a)

  
* denial of service (DoS):
   * Crashing the server
   * Overwhelm the server (use up its resource)
 
## Man-In-The-Middle
* Passive man in the middle (wire tapping)
   * Listen to communication without altering contents.
* Active man in the middle (wire tapping)
   * Modify data being transmitted
   * Example: 

## What is Hacking 
- There are no standard defination of hacking
- Media continues to add false information about hacking
- There are good hackers, and there are bad

## Terminologies
- **Vulnerability:** A weakness that can be exploited
- **Threat:** One who exploits a vlun
- **Risk:** Damage caused by exploiing vuln
- **Asset:** Which needs to be accessed after exploitation
- **Bug:** Error, fault or flow in a computer program that may cause unexpected behaviour

## Profrssional Terms 

- **Penetration Testing:** Testng and reporting the security loopholes, exploit the bug
- **Vulnerability Assessment:** Testing and reporting the security loopholes, and tell how to fix them 
- **Cyber Espionage:** Spying on someone to gain illict access to confidential information

- **Exploits:** Designed to cause unexpected behaviours that an attacker can take advantage of to perform harmful actions 

- **Zero-day Exploits:** Vulnerabilities not known to professionals only to be exploited by hackers


## TCP 
- src----SYN---->dst
- src<---SYN/ACK--->dst
- src<----ACK----->dst
* flag sets:
   * SYN->Synchronize
   * ACK->Acknowledgement
   * FIN->Finish
   * RST->Reset
   * URG->Urgent
   * PSH->Push  
  

## Prots
- **Well-known ports:** 0 to 1023
- **Registered ports:** 1024 to 49151
- **Dynamic and/or open ports:** 49152 to 65535

Required for Cyber Sec :
```
https://tryhackme.com/room/dnsindetail

https://tryhackme.com/room/httpindetail

https://tryhackme.com/room/walkinganapplication

https://tryhackme.com/room/introwebapplicationsecurity

https://tryhackme.com/room/introtooffensivesecurity

https://tryhackme.com/room/owasptop102021

https://cmdchallenge.com/#/list_files
https://hackxor.net/

https://www.moteldivine.com/customer-profile-show.action?wcId=2960
```



