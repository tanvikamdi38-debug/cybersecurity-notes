# 🟠 Module 3 — SOC Fundamentals

1️⃣
# 🏢 ═══ What is a Security Operations Center (SOC)? ═══ 🏢
A **Security Operations Center (SOC)** is a dedicated team of cybersecurity professionals responsible for continuously **monitoring, detecting, investigating, and responding** to security threats within an organization.
The main goal of a SOC is to protect an organization's systems, networks, and data by focusing on two key functions:
- 🔍 **Detection**
- 🚨 **Response**
  
| 🔍 Detection | 🚨 Response |
|-------------|-------------|
| Detect Vulnerabilities | Supports the Incident Response process |
| Detect Unauthorized Activities | Investigates security incidents |
| Detect Policy Violations | Contains and mitigates threats |
| Detect Intrusions | Restores normal operations |

## Three Pillars of a SOC
A successful Security Operations Center is built on three important pillars.
| 👥 People | 📋 Process | 💻 Technology |
|-----------|------------|---------------|
| Security professionals who monitor, investigate, and respond to threats. | Standard procedures and workflows followed to handle security incidents. | Security tools and platforms used to detect, investigate, and respond to cyber threats. |

### 💡 Easy Way to Remember
 **SOC = Detection + Response**
- 👥 **People** → Who performs the work.
- 📋 **Process** → How the work is done.
- 💻 **Technology** → Which tools are used.

2️⃣
# 👨‍💻 ═══ Roles & Responsibilities of a SOC Analyst ═══ 👨‍💻
SOC Analysts work together as a team, with each level having different responsibilities based on their experience and expertise.
## 👥 SOC Team Roles & Responsibilities
| Role | Responsibility |
|------|----------------|
| 🟢 **Level 1 (SOC Analyst)** | Performs basic alert triage, monitors alerts, and escalates suspicious activities. *(0–1 year experience)* |
| 🟡 **Level 2 (SOC Analyst)** | Investigates alerts, collects evidence, and performs detailed analysis to determine the impact. |
| 🔴 **Level 3 (SOC Analyst)** | Performs advanced investigations, analyzes threat indicators, and supports the Incident Response process. |
| ⚙️ **Security Engineer** | Deploys, configures, and maintains security tools and solutions. |
| 🛠️ **Detection Engineer** | Designs, builds, and maintains detection rules to identify threats. |
| 👨‍💼 **SOC Manager** | Leads the SOC team, manages daily operations, and coordinates incident response activities. |

### 💡 Easy Way to Remember
🟢 **Level 1** → Monitor & Triage
🟡 **Level 2** → Investigate
🔴 **Level 3** → Respond
⚙️ **Security Engineer** → Build & Maintain Security Tools
🛠️ **Detection Engineer** → Create Detection Rules
👨‍💼 **SOC Manager** → Lead the SOC Team

3️⃣
# 🔄 ═══ SOC Workflow ═══ 🔄
The **SOC Workflow** is the step-by-step process followed by a Security Operations Center (SOC) to detect, investigate, and respond to cyber threats.

      👨‍💻 Attacker Launches an Attack
            ↓
      ⚡ Suspicious Activity Occurs
            ↓
      📝 Event is Generated
            ↓
      📋 Log is Generated
            ↓
      📊 SIEM Collects the Logs
            ↓
      🔍 SIEM Applies Detection Rules
            ↓
      🚨 Alert is Generated
            ↓
      👨‍💻 Level 1 SOC Analyst
        (Alert Triage)
            ↓
      ❓ True Positive or False Positive?
             ↓                 ↓
        False Positive      True Positive
             ↓                    ↓
        Close Alert      Escalate Investigation
                          ↓
                         🔎 Investigation
                          ↓
                          Confirm Security Incident
                          ↓
                         🚨 Incident Response Begins
                          ↓
                         Containment → Eradication → Recovery
                          ↓
                         📝 Documentation & Lessons Learned
                          ↓
                         ✅ Case Closed

> **💡 Remember:** A **Detection Rule** is a predefined condition that tells the SIEM what suspicious activity to look for. If a log matches the rule, an alert is generated.

4️⃣
# 📊 ═══ SIEM Fundamentals ═══ 📊
# What is SIEM?
**SIEM (Security Information and Event Management)** is a security solution that collects, monitors, and analyzes logs from different devices and applications to detect suspicious activities.
It helps SOC Analysts identify potential security threats by analyzing logs and applying predefined detection rules. When suspicious activity is detected, SIEM generates an alert for further investigation.

## Why Do SOC Analysts Use SIEM?
SOC Analysts use SIEM to:
- 📋 Collect logs from multiple devices and applications.
- 🔍 Analyze user and system activities.
- 🚨 Detect suspicious or malicious behavior.
- ⚡ Generate alerts based on detection rules.
- 🕵️ Help investigate potential security incidents.

### How Does SIEM Work?
```text
💻 Devices & Applications
(Windows, Linux, Firewall, Active Directory, etc.)
                    ↓
📝 Logs are Generated
                    ↓
📊 SIEM Collects & Analyzes Logs
                    ↓
🔍 Detection Rules are Applied
                    ↓
🚨 Alert is Generated
                    ↓
📂 Case Management Platform
(TheHive / ServiceNow / Jira, etc.)
                    ↓
📋 Case is Created
                    ↓
👨‍💻 SOC Analyst
(Alert Triage & Investigation)
```

### 📌 Example
Imagine an employee normally logs in from **Mumbai** every day. One day, the same account attempts to log in from **Russia** after **five failed login attempts**. The SIEM collects these logs, analyzes the activity, and applies its detection rules. Since this behavior is unusual, the SIEM generates an alert. The alert is then forwarded to a **Case Management Platform** (such as **TheHive**), where a case is created and assigned to a SOC Analyst for investigation.

** Important:** SIEM can **collect logs, analyze them, apply detection rules, and generate alerts**, but it **cannot determine whether an alert is a True Positive or a False Positive**. That decision is made by the **SOC Analyst** during the **Alert Triage and Investigation** process.

## 💡 Easy Way to Remember
**Logs → SIEM → Detection Rules → Alert → Case Management → SOC Analyst**

5️⃣
# 🚨 ═══ Alert Lifecycle ═══ 🚨
# 🚨 What is an Alert Lifecycle?
An **Alert Lifecycle** is the complete journey of a security alert, from the moment it is generated until it is investigated, resolved, and finally closed.
It helps SOC Analysts track the status of every alert and ensures that no security incident is missed during the investigation process.

## Why Do SOC Analysts Use the Alert Lifecycle?
SOC Analysts use the Alert Lifecycle to:
- 📌 Track the progress of every security alert.
- 🔍 Ensure each alert is properly investigated.
- ⚡ Identify whether an alert is a **True Positive** or a **False Positive**.
- 📂 Maintain proper documentation of security incidents.
- ✅ Ensure every alert is resolved before closing the case.

           <img width="1536" height="1024" alt="image" src="https://github.com/user-attachments/assets/f4febcf1-6d5e-4987-8b99-705377550e06" />

> **💡 Remember:** Every alert follows a lifecycle—from **Alert Generated** to **Case Closed**. The purpose of the Alert Lifecycle is to ensure that every alert is properly tracked, investigated, documented, and resolved.

