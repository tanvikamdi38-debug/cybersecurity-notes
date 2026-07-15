# 🟠 Chapter 5 — Threat Intelligence & Investigation

1️⃣
# 🧠 ═══ Threat Intelligence Basics ═══ 🧠
##  What is Threat Intelligence?
**Threat Intelligence** is the process of collecting, analyzing, and sharing information about existing and emerging cyber threats. It helps organizations understand attacker behavior, identify potential risks, and take proactive measures to prevent cyber attacks.
Instead of waiting for an attack to happen, Threat Intelligence provides knowledge that helps security teams stay prepared and make informed decisions.

##  Why Do SOC Analysts Use Threat Intelligence?
Although **Threat Intelligence** and the **Security Operations Center (SOC)** are different cybersecurity functions, they work closely together.
SOC Analysts use Threat Intelligence to:
- 🔍 Identify known malicious IP addresses, domains, and file hashes.
- 🚨 Detect emerging cyber threats before they impact the organization.
- 🕵️ Understand attacker behavior, tactics, techniques, and procedures (TTPs).
- 📊 Investigate security alerts more effectively.
- 🛡️ Improve detection rules and strengthen the organization's security posture.

##  Types of Threat Intelligence
| Type | Purpose | Example |
|------|---------|---------|
| 🎯 Strategic Intelligence | Supports management in making long-term cybersecurity decisions. | A company increases its ransomware protection after learning that ransomware attacks are increasing in its industry. |
| 🛠️ Operational Intelligence | Provides information about ongoing or planned cyber attacks. | Security teams receive intelligence about an active phishing campaign. |
| 🔍 Tactical Intelligence | Focuses on attacker behavior, tactics, techniques, and procedures (TTPs). | Analysts learn that attackers are exploiting Remote Desktop Protocol (RDP) to gain initial access. |
| 💻 Technical Intelligence | Provides technical indicators used to detect threats. | Malicious IP addresses, domains, URLs, file hashes, and malware signatures. |

## How Threat Intelligence Works
| 🌐 Threat Intelligence Lifecycle | 🛡️ Threat Intelligence Supporting the SOC |
|----------------------------------|--------------------------------------------|
| ```text | ```text |
| 🌐 Cyber Threats | 🌐 Threat Intelligence |
| │ | │ |
| ▼ | Researches Cyber Threats |
| 📥 Collect Threat Information | │ |
| │ | ▼ |
| ▼ | Shares Threat Intelligence |
| 🔍 Analyze & Validate | (IOCs, TTPs, Threat Reports) |
| │ | │ |
| ▼ | ▼ |
| 📚 Produce Intelligence | 🛡️ SOC Team |
| │ | │ |
| ▼ | ▼ |
| 🤝 Share Intelligence | Detect → Investigate → Respond |
| │ | |
| ▼ | |
| 🛡️ Improve Security | |
| ``` | ``` |

## Threat Intelligence & Investigation Tools
Threat Intelligence is not only about understanding cyber threats—it also involves **investigating, analyzing, and validating suspicious activities** using specialized security tools.
During a security investigation, **SOC Analysts** and **Threat Intelligence teams** use these tools to examine Indicators of Compromise (IOCs), investigate suspicious files, analyze malware, manage incidents, and share threat intelligence.
Each tool has a specific purpose, but together they help security teams detect threats, investigate incidents, and strengthen an organization's overall security posture.
```text
                 🛠️ Threat Intelligence Tools
                          │
      ┌──────────┬─────────┼─────────┬──────────┐
      │          │         │         │          │
🦠 VirusTotal 🐝 TheHive 📜 YARA 📂 OpenIOC 🔗 STIX
      │          │         │         │          │
 Analyze     Manage     Detect     Define     Share
 Threats      Cases     Malware     IOCs     Intelligence
```
## Example
A Threat Intelligence team discovers a new phishing campaign targeting financial organizations. They identify the malicious domains and file hashes and share them with the SOC team.
The SOC team updates its SIEM detection rules, blocks the malicious domains, and investigates any alerts related to those indicators before users are affected.

> ** Things to Remember**
> **Threat Intelligence** and the **Security Operations Center (SOC)** are different cybersecurity functions, but they work together.
> 🧠 **Threat Intelligence** focuses on researching cyber threats, analyzing attacker behavior, and providing actionable intelligence.
> 🛡️ **SOC Analysts** use that intelligence to monitor, detect, investigate, and respond to security incidents.

## 💡 Easy Way to Remember
 **Threat Intelligence = The Brain (Research & Intelligence)** 
 **SOC = The Shield (Detection & Defense)**
 **Threat Intelligence = Collect → Analyze → Share → Protect**

2️⃣
# 🦠 ═══ VirusTotal Investigation ═══ 🦠
**VirusTotal** is a free online threat intelligence platform that helps security professionals analyze suspicious files, URLs, IP addresses, domains, and file hashes using multiple antivirus engines and threat intelligence sources.
Instead of relying on a single antivirus, VirusTotal compares the submitted item against many security vendors, making it easier to identify potential threats.

## Why Do SOC Analysts Use VirusTotal?
SOC Analysts use VirusTotal to:
- 🔍 Verify whether a file or URL is malicious.
- 🌐 Investigate suspicious IP addresses and domains.
- 📁 Check file hashes against known malware.
- 🦠 Identify malware detected by multiple security vendors.
- 📊 Gather additional threat intelligence during investigations.
  
## What Can VirusTotal Analyze?
| Item | Purpose |
|------|---------|
| 📁 **Files** | Scan suspicious files for malware. |
| 🌐 **URLs** | Check whether a website is malicious or used for phishing. |
| 🌍 **Domains** | Investigate suspicious or malicious domains. |
| 📡 **IP Addresses** | Check the reputation of an IP address. |
| 🔑 **File Hashes (MD5, SHA-1, SHA-256)** | Determine whether a file is already known to be malicious. |

## Example
A SOC Analyst receives an alert about a suspicious email attachment. Instead of opening the file, the analyst uploads its **SHA-256 hash** to VirusTotal. VirusTotal reports that **45 out of 70 security vendors** identify the file as ransomware.
This helps the SOC Analyst quickly determine that the file is malicious and continue the investigation.

> ** Remember:** VirusTotal is an **investigation tool**, not a decision-making tool. It shows the results from multiple security engines, but the **SOC Analyst** is responsible for examining the evidence, considering the context, and deciding whether the file is a **True Positive** or a **False Positive**.

## 💡 Easy Way to Remember
**VirusTotal = Analyze → Verify → Investigate**

3️⃣
# 🐝 ═══ TheHive ═══ 🐝
**TheHive** is an open-source **Security Incident Response Platform (SIRP)** and **Case Management Platform** used by Security Operations Centers (SOCs) to investigate and manage cybersecurity incidents.
It helps SOC Analysts organize security alerts into investigation cases, document findings, collaborate with team members, and track the progress of an incident until it is resolved.

## Why is TheHive Useful During an Investigation?
During a security investigation, TheHive helps SOC Analysts to:
- 🚨 Convert security alerts into investigation cases.
- 📋 Organize evidence, observables, and investigation notes.
- 👥 Collaborate with SOC and Incident Response team members.
- 📝 Track investigation progress from start to finish.
- ✅ Maintain complete documentation until the case is closed.

## Example
A SIEM detects multiple failed login attempts followed by a successful login from an unusual location.
The alert is sent to **TheHive**, where a case is created. The SOC Analyst collects evidence, documents the investigation, adds notes, and tracks the case until it is resolved.

> ** Remember:** **TheHive does not detect threats.** It is a **Case Management Platform** that helps SOC Analysts organize, investigate, collaborate, and document security incidents throughout their lifecycle.

## 💡 Easy Way to Remember
**TheHive = Manage → Investigate → Document → Close**

4️⃣
# 📜 ═══ YARA ═══ 📜
**YARA** is a rule-based malware detection tool used by SOC Analysts, Incident Responders, and Malware Analysts to identify and classify malicious files based on specific patterns or characteristics.
Think of **YARA as a fingerprint scanner for malware**. Instead of identifying a person by their fingerprint, YARA identifies malware by matching predefined rules against files or memory.

## Why is YARA Useful During an Investigation?
During a security investigation, YARA helps analysts to:
- 🔍 Detect known malware using custom detection rules.
- 🦠 Identify malware families based on specific patterns.
- 📂 Scan files and memory for suspicious artifacts.
- 🛡️ Support malware analysis and incident investigations.
- ⚡ Improve threat detection by creating reusable detection rules.

## Example
A SOC Analyst receives a suspicious executable file during an investigation. Instead of manually analyzing the entire file, the analyst runs a **YARA rule** designed to detect ransomware. The rule matches the file's characteristics, indicating that it belongs to a known ransomware family, allowing the analyst to investigate further.

> ** Remember:** YARA does **not remove malware**. It helps security teams **identify and classify suspicious files** by matching them against predefined detection rules.

## 💡 Easy Way to Remember
**YARA is a rule-based detection engine that identifies malware by matching predefined patterns.**
**YARA = Create Rules → Match Patterns → Detect Malware**

5️⃣
# 📂 ═══ OpenIOC ═══ 📂
**OpenIOC** is an open standard developed by Mandiant (now part of Google Cloud) for describing, documenting, and sharing **Indicators of Compromise (IOCs)** in a structured and standardized format.
Instead of manually recording IOCs, OpenIOC provides a consistent way for security teams to represent and exchange threat information.

## Why is OpenIOC Useful During an Investigation?
During a security investigation, OpenIOC helps analysts to:
- 📂 Document Indicators of Compromise (IOCs).
- 🔄 Share IOCs in a standardized format.
- 🤝 Exchange threat information between security tools and teams.
- ⚡ Improve the speed and consistency of incident investigations.
- 🛡️ Support threat detection and future investigations.

## Example
During a malware investigation, a SOC Analyst identifies several **Indicators of Compromise**, including a malicious IP address, file hash, and registry key.
Instead of documenting each IOC manually, the analyst stores them in an **OpenIOC** document, allowing other security tools and analysts to reuse the same information during future investigations.

> ** Remember:** **OpenIOC does not detect threats or analyze malware.** It provides a **standardized format** for documenting and sharing Indicators of Compromise (IOCs) between analysts and security tools.

## 💡 Easy Way to Remember
**OpenIOC = Document → Standardize → Share IOCs**
 In **Module 4**, you learned **what an IOC is**. **OpenIOC** is one of the formats used to **organize and share those IOCs** in a structured way.

6️⃣
# 🔗 ═══ STIX ═══ 🔗
**STIX (Structured Threat Information eXpression)** is a standardized, **machine-readable language** used to exchange **Cyber Threat Intelligence (CTI)** between Security Operations Centers (SOCs), security teams, and security tools.
It provides a common framework for documenting and sharing information about **threat actors, attack patterns, Indicators of Compromise (IOCs), campaigns, and other threat intelligence** in a consistent format.

## Why is STIX Useful During an Investigation?
During a security investigation, STIX helps analysts to:
- 🔗 Share Cyber Threat Intelligence (CTI) in a standardized format.
- 🤝 Exchange threat information between security teams and organizations.
- 📊 Document attack patterns, threat actors, and Indicators of Compromise (IOCs).
- ⚡ Enable security tools to automatically process and understand threat intelligence.
- 🛡️ Improve collaboration and incident response.

## Example
A Threat Intelligence team identifies a phishing campaign targeting multiple organizations. They document the **threat actor, attack pattern, malicious domains, file hashes, and IOCs** using **STIX**.
This information can then be shared with other organizations and security tools, helping them detect and defend against the same threat more quickly.

> ** Remember:** **STIX does not detect threats.** It provides a **standardized language** for documenting and sharing Cyber Threat Intelligence (CTI) so that both analysts and security tools can understand and use the same information.

## 💡 Easy Way to Remember
**STIX = Standardize → Share → Strengthen Threat Intelligence**

---
> **💡 Remember:** Threat Intelligence provides the knowledge, while security tools help SOC Analysts transform that knowledge into effective detection, investigation, and response.
---
---

# ⚡ Quick Revision Summary
✔️ **Threat Intelligence** helps organizations collect, analyze, and share information about existing and emerging cyber threats.
✔️ **SOC Analysts** use Threat Intelligence to investigate alerts, understand attacker behavior, and improve threat detection.
✔️ **VirusTotal** is a threat intelligence platform used to analyze suspicious files, URLs, IP addresses, domains, and file hashes using multiple security engines.
✔️ **TheHive** is a Security Incident Response Platform (SIRP) and Case Management Platform that helps SOC Analysts manage and document security investigations.
✔️ **YARA** is a rule-based detection engine that identifies malware by matching predefined patterns and custom detection rules.
✔️ **OpenIOC** is an open standard used to store and share Indicators of Compromise (IOCs), enabling security tools and analysts to identify compromised systems more efficiently.
✔️ **STIX** is a standardized language used to represent and exchange Cyber Threat Intelligence (CTI) between security teams, organizations, and security tools.
✔️ Together, these tools help SOC Analysts collect threat intelligence, investigate security incidents, detect malware, manage cases, and share threat information effectively.

---

# 🚀 Next Module
➡️ **Chapter 6 – Blue Team Operations**
