# 🟡 Chapter 6 — Blue Team Operations

1️⃣
## 🛡️ What are Blue Team Operations?
**Blue Team Operations** are the defensive activities performed by cybersecurity professionals to protect an organization's systems, networks, and data. Their responsibilities include monitoring, detecting, investigating, and responding to cyber threats using various security frameworks, techniques, and tools.
A Blue Team may include:
- 🛡️ SOC Analysts
- 🚨 Incident Responders
- 🔍 Threat Hunters
- 🦠 Malware Analysts
- 💻 Security Engineers
- 📊 Threat Intelligence Analysts
Although each role has different responsibilities, they all work together to detect, investigate, and respond to cyber threats.

2️⃣
# ⛓️ ═══ Cyber Kill Chain ═══ ⛓️
The **Cyber Kill Chain** is a cybersecurity framework that breaks a cyber attack into **seven sequential stages**, helping security teams understand how an attacker progresses from planning an attack to achieving their objective.
By understanding each stage, organizations can detect and stop an attack before it successfully compromises their systems.

## Why Do SOC Analysts Use the Cyber Kill Chain?
SOC Analysts use the Cyber Kill Chain to:\
- 🔍 Understand how attackers progress through each stage of an attack.
- 🚨 Detect malicious activities as early as possible.
- 🛡️ Identify opportunities to interrupt or stop an attack before it succeeds.
- 📊 Improve threat detection, investigation, and incident response.

### The Cyber Kill Chain consists of **seven sequential phases**. The illustration below provides a high-level overview of each stage before we explore them individually.

<img width="950" height="681" alt="image" src="https://github.com/user-attachments/assets/c66a0f6f-1ed7-4187-a5d0-07d656207612" />

## Example
An attacker sends a phishing email containing a malicious attachment. By using the **Cyber Kill Chain**, a SOC Analyst can determine **which stage the attacker has reached** and take appropriate action. For example, if the attack is detected during the **Delivery** stage, the malicious email can be blocked before the user opens it, preventing the attack from progressing further.

> **Remember:** The **Cyber Kill Chain** focuses on the **attacker's journey**. The earlier an attack is detected in the kill chain, the easier it is to stop before damage occurs.

## 💡 Easy Way to Remember
**Cyber Kill Chain = Understand → Detect → Interrupt → Defend**

3️⃣
# 🎯 ═══ MITRE ATT&CK Framework ═══ 🎯
## What is MITRE ATT&CK?
**MITRE ATT&CK** is a knowledge base that documents the **real-world behaviors of cyber attackers**. It is based on observations of actual cyber attacks and helps security professionals understand how adversaries operate using their **Tactics, Techniques, and Procedures (TTPs).**
**ATT&CK** stands for **Adversarial Tactics, Techniques, and Common Knowledge.**

## What is the MITRE ATT&CK Framework?
The **MITRE ATT&CK Framework** is a structured framework that organizes the ATT&CK knowledge base into **Tactics, Techniques, and Sub-techniques**. It provides security teams with a common framework to map attacker behavior, investigate incidents, perform threat hunting, and improve threat detection.

## Why Do SOC Analysts Use the MITRE ATT&CK Framework?
SOC Analysts use the MITRE ATT&CK Framework to:
- 🔍 Understand attacker behavior during an investigation.
- 🚨 Map suspicious activities to known attack techniques.
- 🛡️ Improve threat detection and detection rules.
- 🕵️ Support threat hunting and incident response.
- 📊 Identify security gaps and strengthen the organization's security posture.
- 🤝 Communicate investigations using a common industry-standard framework.

## Example
A SOC Analyst investigates a phishing incident where an employee opens a malicious email attachment. Using the **MITRE ATT&CK Framework**, the analyst maps the attack to the relevant **tactic**, **technique**, and **sub-technique**. This helps the team understand the attacker's behavior, improve detection rules, and prevent similar attacks in the future.

> **Remember:**
 • **Tactic** → The attacker's **goal or objective** (What the attacker wants to achieve.)
 • **Technique** → The **method** used by the attacker to achieve that goal.
 • **Sub-technique** → A **more detailed variation** of a technique that explains exactly how the attack is carried out.

## 💡 Easy Way to Remember
**MITRE ATT&CK = Understand → Map → Detect → Defend**

4️⃣
# 🔎 ═══ Threat Hunting ═══ 🔎
**Threat Hunting** is a proactive cybersecurity process in which security analysts actively search for hidden threats that may have bypassed traditional security tools. Instead of waiting for an alert, analysts investigate systems and networks to identify suspicious activities before they cause damage.

## Why Do SOC Analysts Perform Threat Hunting?
SOC Analysts perform Threat Hunting to:
- 🔍 Discover hidden threats that security tools may have missed.
- 🚨 Detect advanced or stealthy attacks at an early stage.
- 🛡️ Reduce the risk of future security incidents.
- 📊 Improve threat detection and strengthen security controls.
- 🕵️ Validate whether suspicious activities are malicious or benign.
  
##  Example
A SOC Analyst notices unusual PowerShell activity on multiple endpoints. Although no security alert has been triggered, the analyst proactively investigates the logs, identifies a malicious script, and prevents the attacker from establishing persistence within the network.

> **Remember:**
 **Threat Hunting is proactive**, whereas **Incident Response is reactive**.
 **Threat Hunting** → Actively searches for hidden threats before an alert occurs.
 **Incident Response** → Investigates and responds after a security incident or alert is detected.

## 💡 Easy Way to Remember
**Threat Hunting = Hunt → Investigate → Detect → Protect**

5️⃣
## 📊 What is Log Analysis?
**Log Analysis** is the process of collecting, reviewing, and analyzing log data generated by systems, applications, and network devices to identify suspicious activities, security incidents, and system issues.
Logs provide a record of events, helping security teams understand **what happened, when it happened, where it happened, and who was involved.**

## Why Do SOC Analysts Perform Log Analysis?
SOC Analysts analyze logs to:
- 🔍 Detect suspicious or malicious activities.
- 🚨 Investigate security alerts and incidents.
- 🕵️ Trace attacker actions during an investigation.
- 📊 Identify Indicators of Compromise (IOCs).
- 🛡️ Support threat hunting and incident response.
- 📑 Maintain evidence for reporting and forensic investigations.

## Example
A SOC Analyst receives an alert about multiple failed login attempts. By reviewing authentication logs, the analyst discovers repeated login attempts from the same IP address followed by a successful login. This helps identify a potential brute-force attack and allows the analyst to respond before further damage occurs.

> **📝 Remember:**
 • A **log** is a record of an event that occurs on a system, application, or network device.
 • Logs are **automatically generated** by software or operating systems whenever an event occurs. SOC Analysts **analyze** logs—they don't create them.

## 💡 Easy Way to Remember
**Log Analysis = Collect → Review → Investigate → Respond**

6️⃣
# 🪟 ═══ Windows Event Logs ═══ 🪟
**Windows Event Logs** are built-in logs generated by the Windows operating system that automatically record important system, security, and application events. They help administrators and SOC Analysts monitor system activity, troubleshoot issues, and investigate security incidents.

## Why Do SOC Analysts Use Windows Event Logs?
SOC Analysts use Windows Event Logs to:
- 🔍 Monitor user login and authentication activities.
- 🚨 Detect suspicious or unauthorized actions.
- 🕵️ Investigate security incidents and attacker behavior.
- 📊 Collect forensic evidence during investigations.
- 🛡️ Identify Indicators of Compromise (IOCs) and support incident response.

## Main Types of Windows Event Logs
| Log Type | Purpose |
|----------|---------|
| 🔐 **Security** | Records login attempts, account activity, privilege changes, and other security-related events. |
| ⚙️ **System** | Records events generated by Windows, such as driver, hardware, and operating system activities. |
| 🖥️ **Application** | Records events generated by installed applications and software. |

## Example
A SOC Analyst receives an alert about a suspected brute-force attack. By reviewing the **Security** log, the analyst identifies multiple failed login attempts followed by a successful login, helping confirm the attack and begin the investigation.

> **📝 Remember:**
 • **Windows Event Logs** are automatically generated by the Windows operating system.
 • Every important Windows activity (such as logins, system changes, or application events) can create an event log that helps SOC Analysts investigate incidents.

## 💡 Easy Way to Remember
**Windows Event Logs = Monitor → Record → Investigate → Respond**

7️⃣
# 📑 ═══ Sysmon ═══ 📑
**Sysmon (System Monitor)** is a Microsoft Sysinternals tool that provides **detailed event logging** about system activities, such as process creation, network connections, file changes, and process execution. It helps security teams detect and investigate advanced threats.

## Why Do SOC Analysts Use Sysmon?
SOC Analysts use Sysmon to:
- 🔍 Monitor detailed system activities.
- 🚨 Detect suspicious or malicious behavior.
- 🕵️ Investigate cyber attacks more effectively.
- 📊 Collect detailed forensic evidence.
- 🛡️ Support threat hunting and incident response.

## Example
A SOC Analyst uses **Sysmon** to detect that **PowerShell** executed a suspicious script and connected to an unknown IP address, helping identify a potential malware infection.

> **📝 Remember:**
 • **Windows Event Logs** record general system events, while **Sysmon** provides **more detailed security events** for investigations.
 • Sysmon must be **installed and configured** before it starts generating logs.

## 💡 Easy Way to Remember
**Sysmon = Monitor → Detect → Investigate**

8️⃣
# 🤖 ═══ SOAR ═══ 🤖
**SOAR (Security Orchestration, Automation, and Response)** is a security platform that integrates multiple security tools into a single workflow and automates repetitive security tasks. It helps SOC Analysts investigate and respond to security incidents more efficiently, reducing manual effort and response time.

## Why Do SOC Analysts Use SOAR?
SOC Analysts use SOAR to:
- 🔗 Integrate multiple security tools into one platform.
- ⚡ Automate repetitive investigation tasks.
- 📊 Collect evidence from different security tools.
- 🚨 Speed up incident response.
- 🛡️ Reduce manual work and improve efficiency.

## How SOAR Works
```text
Security Alert
      │
      ▼
Collect Evidence
(VirusTotal, Microsoft Defender, EDR, Threat Intelligence, etc.)
      │
      ▼
Run Automated Response Playbook
      │
      ▼
Create Incident
      │
      ▼
Send to SOC Analyst
      │
      ▼
Analyst Reviews
(True Positive / False Positive)
      │
      ▼
Incident Response
```
## Example
A phishing email is detected by the SIEM. SOAR automatically gathers evidence from VirusTotal and Microsoft Defender, creates an incident, and sends it to the SOC Analyst. The analyst reviews the evidence, confirms whether it is a true or false positive, and takes the appropriate response.

> **Remember:**
 • **SOAR automates repetitive tasks, not decision-making.**
 • It helps SOC Analysts investigate incidents faster by collecting evidence and following predefined response playbooks.

## 💡 Easy Way to Remember
**SOAR = Integrate → Automate → Investigate → Respond**

9️⃣
# 🧪 ═══ Sandboxing ═══ 🧪
**Sandboxing** is a security technique that runs suspicious files, programs, or untrusted code in an **isolated and controlled environment** to observe their behavior without affecting the actual system.

## Why Do SOC Analysts Use Sandboxing?
SOC Analysts use Sandboxing to:
- 🔍 Analyze suspicious files safely.
- 🦠 Detect malware and zero-day threats.
- 🛡️ Prevent malicious files from affecting the network.
- 📊 Understand the behavior of unknown files.

  <img width="2720" height="2024" alt="sandbox_malware_analysis_flow" src="https://github.com/user-attachments/assets/8a8f0370-128a-43f3-815b-8679ae2abf21" />


## Example
A suspicious email attachment is opened inside a **sandbox**. If the file behaves maliciously, it is isolated and prevented from spreading to other systems.

> **📝 Remember:**
 • A **sandbox** is an isolated environment used to safely test suspicious files.
 • If a file is malicious, it can be blocked or quarantined before it impacts the network.

## 💡 Easy Way to Remember
**Sandbox = Isolate → Analyze → Protect**
---

## ⚡ Quick Revision Summary
✅ **Blue Team Operations** focuses on defending organizations by detecting, analyzing, and responding to cyber threats using security tools, processes, and defensive strategies.
✅ **Cyber Kill Chain** helps security teams understand the different stages of an attack, from reconnaissance to achieving attacker objectives.
✅ **MITRE ATT&CK Framework** provides a knowledge base of real-world adversary tactics and techniques, helping defenders detect and respond to attacker behavior.
✅ **Threat Hunting** is a proactive security approach where analysts search for hidden threats, suspicious activities, and attacker behavior that may bypass traditional security tools.
✅ **Log Analysis** helps SOC Analysts investigate security events, identify abnormal patterns, and detect possible security incidents.
✅ **Windows Event Logs** provide visibility into system activities such as authentication, process execution, and user actions. Important Event IDs include:
- 4624 → Successful Logon
- 4625 → Failed Logon
- 4688 → Process Creation
✅ **Sysmon** improves Windows monitoring by collecting detailed information about processes, network connections, file activities, and system changes.
✅ **Sandbox Analysis** is a safe isolated environment used to execute and analyze suspicious files or malware without affecting the real system. It helps analysts observe malware behavior, network activity, file changes, and indicators of compromise (IOCs).
✅ **SOAR (Security Orchestration, Automation, and Response)** acts as a virtual assistant for SOC Analysts by integrating multiple security tools and automating repetitive tasks. It helps collect evidence, enrich alerts, execute response playbooks, and improve incident response efficiency.
✅ **Together, Blue Team techniques, SOAR, and Sandbox Analysis help SOC teams improve threat detection, automate investigations, safely analyze malware, and respond to security incidents faster.**

---

## 🚀 Next Module
➡️ **Module 7 — Digital Forensics**
