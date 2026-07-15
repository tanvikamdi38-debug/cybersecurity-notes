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

> **📝 Things to Remember**
> **Threat Intelligence** and the **Security Operations Center (SOC)** are different cybersecurity functions, but they work together.
> 🧠 **Threat Intelligence** focuses on researching cyber threats, analyzing attacker behavior, and providing actionable intelligence.
> 🛡️ **SOC Analysts** use that intelligence to monitor, detect, investigate, and respond to security incidents.

## 💡 Easy Way to Remember
🧠 **Threat Intelligence = The Brain (Research & Intelligence)**
🛡️ **SOC = The Shield (Detection & Defense)**
**Threat Intelligence = Collect → Analyze → Share → Protect**
