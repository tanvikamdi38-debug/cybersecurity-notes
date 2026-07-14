# 🔴 Module 4 — Incident Response

1️⃣
# ⚠️ ═══ Event vs Incident ═══ ⚠️
Before learning Incident Response, it's important to understand the difference between an **Event** and an **Incident**. Although these terms are often used together, they have different meanings in cybersecurity.
# What is an Event?
An **Event** is any observable activity or action that occurs on a system, network, or application. Events happen continuously and are not always harmful. They simply record what is happening within a system.

## Examples of Events
- 👤 User logs into a computer.
- 📁 A file is opened or deleted.
- 🌐 A website is accessed.
- ❌ A failed login attempt.
- 🔄 A system restart.

### What is an Incident?
An **Incident** is a security event that violates an organization's security policy or threatens the confidentiality, integrity, or availability (CIA) of systems or data.
In simple words, an incident is an event that has the potential to cause harm and requires investigation or response.

#### Examples of Incidents
- 🦠 Malware infection.
- 🎣 Successful phishing attack.
- 🔓 Unauthorized access to a system.
- 💾 Data breach.
- 🔐 Ransomware attack.

##### ⚖️ Event vs Incident
| ⚡ Event | 🚨 Incident |
|----------|-------------|
| Any activity that occurs on a system or network. | A security event that threatens an organization's systems or data. |
| Can be normal or suspicious. | Always requires investigation and response. |
| Does not always cause damage. | Has the potential to cause damage or impact business operations. |
| Recorded as a log. | Treated as a security incident. |

###### Real-Life Example
Imagine you receive an email.
- 📩 Receiving the email is an **Event**.
- 🎣 If the email contains a phishing link and you click it, compromising your system, it becomes an **Incident**.

> 💡 **Easy Way to Remember:**
> ✅ **Every Incident is an Event, but not every Event is an Incident.**
> An **Event** is any activity that occurs on a system.
> An **Incident** is an event that threatens the confidentiality, integrity, or availability (CIA) of an organization's systems or data and requires a response.

2️⃣
# 🚑 ═══ Cybersecurity Incident ═══ 🚑
A **Cybersecurity Incident** is any event that compromises or has the potential to compromise the **Confidentiality, Integrity, or Availability (CIA)** of an organization's systems, networks, or data.
In simple words, it is a security event that can cause harm to an organization's information or business operations and requires investigation and response.

## Common Examples of Cybersecurity Incidents
- 🦠 Malware Infection
- 🎣 Phishing Attack
- 🔓 Unauthorized Access
- 💾 Data Breach
- 🔐 Ransomware Attack
- 🌐 Distributed Denial-of-Service (DDoS) Attack

###  Example
Imagine an employee receives a phishing email that looks legitimate. The employee clicks the malicious link and enters their login credentials. The attacker then gains unauthorized access to the organization's email account.
This is considered a **Cybersecurity Incident** because it compromises the organization's security and requires immediate investigation and response.

#### 💡 Easy Way to Remember
🚑 **Cybersecurity Incident = A security event that threatens the CIA (Confidentiality, Integrity, or Availability) of an organization's systems or data.**

3️⃣
# 🛠️ ═══ Incident Handling ═══ 🛠️
**Incident Handling** is the structured process of identifying, managing, and responding to cybersecurity incidents in a way that minimizes damage, restores normal operations, and prevents similar incidents from happening again.
Its primary goal is to ensure that security incidents are handled quickly, efficiently, and with minimal impact on the organization.

## Why is Incident Handling Important?
Incident Handling helps organizations to:
- 🛡️ Minimize the impact of cyber attacks.
- ⚡ Respond to security incidents quickly and effectively.
- 🔍 Identify the root cause of an incident.
- ♻️ Restore affected systems and business operations.
- 📚 Improve security by learning from previous incidents.

### Role of Incident Handling for a SOC Analyst
A SOC Analyst plays an important role in the Incident Handling process by:
- 🚨 Monitoring and responding to security alerts.
- 🔎 Investigating suspicious activities.
- 📊 Collecting and analyzing security logs.
- 📂 Escalating confirmed incidents to the Incident Response team.
- 📝 Documenting findings and maintaining incident records.
- 🤝 Working with other security teams to resolve incidents.

#### Example
Imagine an organization receives multiple alerts about unusual login attempts. The SOC Analyst investigates the alerts, confirms unauthorized access, escalates the incident, and works with the Incident Response team to contain and resolve the attack.
This complete process is part of **Incident Handling**.

## 💡 Easy Way to Remember
**Incident Handling = Detect → Investigate → Respond → Recover → Improve**

4️⃣
# 🔄 ═══ NIST Incident Response Lifecycle ═══ 🔄
**NIST (National Institute of Standards and Technology)** is a U.S. government organization that develops cybersecurity standards, guidelines, and best practices to help organizations protect their systems, networks, and data.
NIST provides a structured approach to cybersecurity, making it easier for organizations to prepare for, respond to, and recover from security incidents.

## Why is NIST Important?
Organizations follow NIST because it helps them to:
- 📋 Follow industry-standard cybersecurity practices.
- 🛡️ Improve incident detection and response.
- ⚡ Minimize the impact of cyber attacks.
- 📚 Build a structured Incident Response process.
- 🔄 Continuously improve their overall security posture.

### NIST Incident Response Lifecycle
The **NIST Incident Response Lifecycle** provides a step-by-step framework for handling cybersecurity incidents efficiently while minimizing damage and restoring normal business operations.
```text
┌────────────────────────────────────┐
│ 🔄 NIST Incident Response Lifecycle│ 
└────────────────────────────────────┘
                │
                ├────────► ┌────────────────────────────┐
                │          │ a) 📝 Preparation          │      
                │          └────────────────────────────┘
                │
                ├────────► ┌────────────────────────────┐
                │          │ b) 🔎 Detection & Analysis │   
                │          └────────────────────────────┘
                │
                ├────────► ┌────────────────────────────────────────────────┐
                │          │c) 🛡️ Containment → 🧹 Eradication → ♻️ Recovery│ 
                │          └────────────────────────────────────────────────┘
                │
                └────────► ┌────────────────────────────┐
                           │ d) 📚 Post Incident Activity│   
                           └────────────────────────────┘
```
# **a) 📝 Preparation**
Preparation is the **first phase** of the **NIST Incident Response Lifecycle**. It focuses on ensuring that an organization is ready to detect, respond to, and recover from cybersecurity incidents before they occur.
The main goal of the **Preparation** phase is to build a strong incident handling capability and implement preventive security measures that reduce the risk and impact of cyber attacks.

## Main Objectives of Preparation
```text
                    🎯 Objectives
                         │
        ┌────────────────┴────────────────┐
        │                                 │
🏢 Establish an                    🛡️ Protect Against &
Incident Handling Capability       Prevent IT Security Incidents
```
### 🏢 Objective 1: Establish an Incident Handling Capability
This objective focuses on preparing the organization's **people, processes, and resources** to respond effectively when a cybersecurity incident occurs.
| Activity | Brief Explanation | Simple Example |
|----------|-------------------|----------------|
| 📋 Incident Response Policies & Procedures | Defines how the organization should respond to different security incidents. | A company has a policy to immediately report any ransomware attack to the SOC team. |
| 📖 Documentation & Playbooks | Step-by-step guides for handling different types of incidents. | A phishing playbook explains how to investigate and contain a phishing attack. |
| 👨‍💻 Team Training | Ensures SOC and Incident Response teams know how to respond during incidents. | Analysts regularly practice investigating simulated attacks. |
| 🛠️ Security Tools | Deploys the tools required to monitor, detect, and respond to threats. | Installing SIEM, EDR, Firewall, and Antivirus solutions. |
| 💾 Backup & Recovery Planning | Ensures important data can be restored after an incident. | Daily backups allow systems to be restored after a ransomware attack. |
| 📊 SIEM Configuration | Configures SIEM and detection rules before incidents occur. | Create a rule that alerts after multiple failed login attempts. |
| 🧪 Tabletop & Purple Team Exercises | Tests the organization's incident response readiness. | Teams simulate a cyber attack to improve response capabilities.| 

#### 🛡️ Objective 2: Protect Against & Prevent IT Security Incidents
This objective focuses on implementing preventive security controls to reduce the chances of a successful cyber attack.
| Security Control | Brief Explanation | Simple Example |
|------------------|-------------------|----------------|
| 🔐 Multi-Factor Authentication (MFA) | Adds an extra verification step during login. | After entering your password, you approve the login using your phone or an authenticator app. |
| 📧 DMARC, SPF & DKIM | Protect email domains from spoofing and phishing emails. | They help verify whether an email claiming to be from **support@amazon.com** is genuine. |
| 🖥️ Endpoint Hardening | Secures devices by reducing unnecessary attack surfaces. | Disable unused services and keep Windows updated. |
| 🛡️ Endpoint Detection & Response (EDR) | Continuously monitors endpoints for suspicious activities. | Detects ransomware behavior and isolates the infected laptop. |
| 🌐 Network Protection | Protects the network from unauthorized or malicious traffic. | A firewall blocks suspicious incoming connections. |
| 👤 Privileged Identity Management (PIM) | Controls access to privileged accounts. | An administrator receives admin rights only when needed. |
| 🔑 Strong Password Policies | Reduces the risk of weak passwords. | Require passwords with at least 12 characters and multiple character types. |
| 🔍 Vulnerability Scanning | Identifies security weaknesses before attackers exploit them. | A scanner detects outdated software that requires patching. |
| 👨‍🏫 Security Awareness Training | Educates employees about common cyber threats. | Employees learn how to identify phishing emails. |
| 🏢 Active Directory Security Assessment | Reviews Active Directory for security weaknesses. | Remove inactive administrator accounts and unnecessary permissions. |

##### Example
Before a cyber attack occurs, an organization:
- 🔐 Enables **Multi-Factor Authentication (MFA)** for employees.
- 📧 Configures **DMARC, SPF, and DKIM** to protect company emails.
- 📊 Deploys **SIEM** and **EDR** to monitor suspicious activities.
- 🔍 Performs regular **vulnerability scans**.
- 👨‍🏫 Conducts **security awareness training** for employees.
These activities help prevent attacks and ensure the organization is prepared to respond effectively if a cybersecurity incident occurs.
---
> **Note:** The security controls listed above are **preventive measures**. Their purpose is to reduce the likelihood of a cybersecurity incident before the Incident Response process begins.

## 💡 Easy Way to Remember
**Preparation = Plan → Protect → Prepare Before an Incident Happens**
> **📝 Note:** According to the **NIST Incident Response Lifecycle**, **Containment, Eradication, and Recovery** are grouped into one phase. However, they are commonly explained separately because each phase has a different objective during incident response.

# **b) 🔎 Detection & Analysis**
Detection & Analysis is the second phase of the **NIST Incident Response Lifecycle**. In this phase, the organization identifies suspicious activities, analyzes security events, and determines whether they represent a real cybersecurity incident.
The main goal of this phase is to **Detect, analyze, and validate suspicious activities before initiating incident response, investigate them, determine their impact, and collect enough evidence to support an effective response.**

## Main Objectives of Detection & Analysis
```text
                 🎯 Objectives
                      │
        ┌─────────────┴─────────────┐
        │                           │
🔍 Detect Security Events      🕵️ Analyze & Investigate
```
### 🔍 How is Detection Performed?
Organizations detect suspicious activities by monitoring different layers of their environment.
| Detection Layer | Security Controls | Purpose |
|-----------------|------------------|---------|
| 🌐 Network Perimeter | Firewall, IDS, IPS | Monitor incoming and outgoing network traffic. |
| 🏢 Internal Network | Internal Firewall, IDS, IPS | Detect suspicious activities within the internal network. |
| 💻 Endpoint Level | EDR, Antivirus | Monitor laptops, desktops, and servers for malicious behavior. |
| 🌍 Application Level | Application Logs | Detect suspicious activities within applications and web services. |
---
#### 🕵️ Initial Investigation
Once suspicious activity is detected, the SOC Analyst begins the initial investigation to understand:
- ❓ What happened?
- 👤 Who was affected?
- 🖥️ Which systems are impacted?
- 📅 When did it happen?
- 🌐 Where did it originate?
- 🎯 What is the potential impact?
  
##### Investigation Cycle
The investigation process is continuous and repeats until enough evidence has been collected.
```text
              🔎 Initial Investigation
                       │
                       ▼
      🎯 Identify Indicators of Compromise (IOCs)
                       │
                       ▼
       💻 Identify New Leads & Impacted Systems
                       │
                       ▼
        📊 Collect & Analyze Additional Evidence
                       │
                       ▼
          🔁 Repeat Until Investigation Ends
```
> **📝 Note:** During this phase, SOC Analysts continuously discover new evidence. Each new Indicator of Compromise (IOC) may reveal additional compromised systems, requiring further investigation.
> 
###### SOC Analyst's Role
- 📊 Monitor alerts generated by SIEM.
- 🔍 Perform Alert Triage.
- 📂 Analyze logs from multiple sources.
- 🖥️ Identify affected systems.
- 🚨 Confirm whether the incident is a **True Positive** or **False Positive**.
- ⬆️ Escalate confirmed incidents to the Incident Response team.
- 
####### Example
The SIEM generates an alert after detecting multiple failed login attempts followed by a successful login from an unusual location.
The SOC Analyst reviews the logs, identifies the compromised user account, checks other affected systems, and collects additional evidence before confirming the security incident. 

## 💡 Easy Way to Remember
**Detection = Find the Threat**
**Analysis = Understand the Threat**

## **c) 🛡️ Containment, Eradication & Recovery**
This phase focuses on **stopping the attack, removing the threat, and restoring normal business operations**. Once an incident has been confirmed, the organization works to minimize its impact and ensure that the attacker no longer has access.

## Main Objectives
```text
                    🎯 Objectives
                         │
      ┌──────────────────┼──────────────────┐
      │                  │                  │
🛡️ Containment      🧹 Eradication      ♻️ Recovery
```

# 🛡️ Containment
Containment is the process of **limiting the impact of a cybersecurity incident** and preventing it from spreading to other systems while the investigation continues.
The main goal is to isolate the affected systems and protect the rest of the organization's environment.

## Types of Containment
| Type | Purpose | Example |
|------|---------|---------|
| ⚡ **Short-Term Containment** | Immediately stop the attack from spreading. | Disconnect an infected computer from the network or disable a compromised user account. |
| 🛠️ **Long-Term Containment** | Apply permanent fixes while allowing business operations to continue safely. | Patch vulnerable systems, change compromised passwords, or rebuild affected servers. |

### SOC Analyst's Role
- Identify affected systems.
- Isolate compromised devices.
- Block malicious IP addresses or domains.
- Coordinate with the Incident Response team.

# 🧹 Eradication
Eradication is the process of **completely removing the root cause of the incident** so that the attacker can no longer access the environment.
The objective is to ensure that no malicious files, backdoors, or vulnerabilities remain.

## Common Activities
- 🦠 Remove malware.
- 🔐 Reset compromised passwords.
- 🩹 Patch security vulnerabilities.
- 🚫 Remove malicious accounts or backdoors.
- 🔍 Verify that no additional systems are compromised.

### SOC Analyst's Role
- Identify the root cause.
- Verify that the threat has been removed.
- Support the Incident Response team during cleanup.

# ♻️ Recovery
Recovery is the process of **restoring affected systems and returning business operations to normal** after the threat has been removed. The organization continues monitoring to ensure the attacker does not regain access.

## Common Activities
- 💾 Restore systems from clean backups.
- ✅ Verify that systems are functioning normally.
- 📊 Monitor systems for recurring malicious activity.
- 🚀 Return systems to production.

### SOC Analyst's Role
- Monitor recovered systems.
- Verify that no suspicious activity returns.
- Confirm that normal operations have resumed safely.

#### Example
A ransomware attack encrypts an employee's computer.
- 🛡️ **Containment:** The infected computer is disconnected from the network to stop the ransomware from spreading.
- 🧹 **Eradication:** The malware is removed, compromised accounts are secured, and the vulnerability is patched.
- ♻️ **Recovery:** The computer is restored from a clean backup and monitored before being returned to the employee.

## 💡 Easy Way to Remember
- 🛡️ **Containment = Stop the attack from spreading.**
- 🧹 **Eradication = Remove the attacker and the root cause.**
- ♻️ **Recovery = Restore normal business operations safely.**

# **d) 📚 Post-Incident Activity**
Post-Incident Activity is the **final phase** of the **NIST Incident Response Lifecycle**. After the incident has been contained, eradicated, and systems have recovered, the organization reviews the entire incident to understand **what happened, what actions were taken, how effective those actions were, and what improvements can be made to prevent similar incidents in the future.**
The main goal of this phase is to **document the incident, identify lessons learned, and improve the organization's Incident Response process.**

## Example
After recovering from a ransomware attack, the security team reviews the incident, documents the actions taken, updates the Incident Response playbook, and improves security controls to reduce the risk of similar attacks in the future.

## 💡 Easy Way to Remember
**Post-Incident Activity = Review → Document → Improve**

5️⃣
# 🎯 ═══ Indicators of Compromise (IOCs) ═══ 🎯
An **Indicator of Compromise (IOC)** is a piece of digital evidence or a digital footprint that indicates a system, network, or device **has been compromised** by a cyber attack.
IOCs help security teams investigate incidents, identify affected systems, understand what happened, and improve future detection and prevention.

## Why are IOCs Important?
IOCs help organizations to:
- 🔍 Detect compromised systems.
- 🕵️ Support incident investigations.
- 📊 Understand how an attack occurred.
- 🛡️ Improve future detection and prevention.

### Example
During a ransomware investigation, a SOC Analyst discovers a **malicious IP address**, a **suspicious file hash**, and a **phishing email** used by the attacker.
These digital footprints indicate that the system has been compromised and help the security team investigate the incident.

> ** Remember:** **IOA (Indicator of Attack)** focuses on suspicious attacker behavior and helps detect attacks before or while they are happening.

## 💡 Easy Way to Remember
- 🎯 **IOC = Digital evidence left behind after an attack.**
- 🚨 **IOA = Suspicious behavior that indicates an attack is in progress.**

  6️⃣
# 📄 ═══ Reporting ═══ 📄
Reporting is the process of documenting a cybersecurity incident from the moment it is detected until it is fully resolved.
The main goal of reporting is to maintain a complete record of the incident by documenting **what happened, how it happened, what actions were taken, the evidence collected, and the final outcome**. This documentation helps organizations improve future incident response, support audits and compliance requirements, and serves as a reference for future investigations.

## What Does an Incident Report Include?
- 🕒 Incident timeline
- 🚨 Type of incident
- 🔍 Root cause
- 💻 Affected systems
- 🛠️ Actions taken by the security team
- ✅ Final resolution
- 📚 Recommendations for future improvements

###  Example
A ransomware attack is detected on a company's file server.
The SOC team documents the **incident timeline**, affected systems, investigation findings, actions taken during containment and recovery, and recommendations to prevent similar attacks in the future.
This complete document is known as the **Incident Report**.

> **📝 Remember:** During investigations involving digital evidence, organizations may also maintain a **Chain of Custody** to ensure that evidence is properly collected, handled, and preserved without being altered.

## 💡 Easy Way to Remember
**Reporting = Document → Record → Improve**

---

# ⚡ Quick Revision Summary
✔️ An **Event** is any activity on a system, while an **Incident** is an event that threatens security and requires a response.
✔️ A **Cybersecurity Incident** compromises or has the potential to compromise the **Confidentiality, Integrity, or Availability (CIA)** of systems or data.
✔️ **Incident Handling** provides a structured approach to detecting, investigating, responding to, and recovering from cybersecurity incidents.
✔️ The **NIST Incident Response Lifecycle** consists of **Preparation**, **Detection & Analysis**, **Containment, Eradication & Recovery**, and **Post-Incident Activity**.
✔️ **Preparation** focuses on building incident response capabilities and implementing preventive security controls.
✔️ **Detection & Analysis** identifies suspicious activities, investigates alerts, and confirms whether a security incident has occurred.
✔️ **Containment** limits the spread of an attack, **Eradication** removes the root cause, and **Recovery** restores systems to normal operations.
✔️ **Post-Incident Activity** reviews the incident, documents findings, and improves future incident response.
✔️ **Indicators of Compromise (IOCs)** are digital evidence that help investigators identify compromised systems and understand how an attack occurred.
✔️ **Reporting** documents the entire incident, supporting future investigations, compliance, and continuous improvement.

---

# 🚀 Next Module
➡️ **Module 5 – Threat Intelligence & Investigation**
