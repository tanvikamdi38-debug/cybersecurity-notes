# 🟠 Chapter 5 — Threat Intelligence & Investigation

1️⃣
# 🧠 ═══ Threat Intelligence Basics ═══ 🧠
## What is Threat Intelligence?
**Threat Intelligence** is the process of collecting, analyzing, and sharing information about existing and emerging cyber threats. It helps organizations understand attacker behavior, identify potential risks, and take proactive measures to prevent cyber attacks.
Instead of waiting for an attack to happen, Threat Intelligence provides knowledge that helps security teams stay prepared and make informed decisions.

## Why Do SOC Analysts Use Threat Intelligence?
Although **Threat Intelligence** and the **Security Operations Center (SOC)** are different cybersecurity functions, they work closely together.
SOC Analysts use Threat Intelligence to:
- 🔍 Identify known malicious IP addresses, domains, and file hashes.
- 🚨 Detect emerging cyber threats before they impact the organization.
- 🕵️ Understand attacker behavior, tactics, techniques, and procedures (TTPs).
- 📊 Investigate security alerts more effectively.
- 🛡️ Improve detection rules and strengthen the organization's security posture.

## Types of Threat Intelligence
| Type | Purpose | Example |
|------|---------|---------|
| 🎯 Strategic Intelligence | Supports management in making long-term cybersecurity decisions. | A company increases its ransomware protection after learning that ransomware attacks are increasing in its industry. |
| 🛠️ Operational Intelligence | Provides information about ongoing or planned cyber attacks. | Security teams receive intelligence about an active phishing campaign. |
| 🔍 Tactical Intelligence | Focuses on attacker behavior, tactics, techniques, and procedures (TTPs). | Analysts learn that attackers are exploiting Remote Desktop Protocol (RDP) to gain initial access. |
| 💻 Technical Intelligence | Provides technical indicators used to detect threats. | Malicious IP addresses, domains, URLs, file hashes, and malware signatures. |

## How Threat Intelligence Works: Standalone & with SOC
| 🌐 Threat Intelligence Lifecycle | 🛡️ How Threat Intelligence Supports a SOC |
|----------------------------------|-------------------------------------------|
| ```text                          | ```text                                   |
| 🌐 Cyber Threats                 | 🌐 Threat Intelligence                    |
|        │                         |         │                                 |
|        ▼                         | Researches Cyber Threats                  |
| 📥 Collect Threat Information    |         │                                 |
|        │                         |         ▼                                 |
|        ▼                         | Shares Threat Intelligence                |
| 🔍 Analyze & Validate            | (IOCs, TTPs, Threat Reports)              |
|        │                         |         │                                 |
|        ▼                         |         ▼                                 |
| 📚 Produce Intelligence          | 🛡️ SOC Team                              |
|        │                         |         │                                 |
|        ▼                         |         ▼                                 |
| 🤝 Share Intelligence            | Detect → Investigate → Respond            |
| ```                              | ```                                       |

## Example
A Threat Intelligence team discovers a new phishing campaign targeting financial organizations. They identify the malicious domains and file hashes and share them with the SOC team.
The SOC team updates its SIEM detection rules, blocks the malicious domains, and investigates any alerts related to those indicators before users are affected.

> **Think of it this way:**
> 🧠 **Threat Intelligence = The Brain (Research & Intelligence)**
> 🛡️ **SOC = The Shield (Detection & Defense)**

## 💡 Easy Way to Remember

**Threat Intelligence = Collect → Analyze → Share → Protect**
