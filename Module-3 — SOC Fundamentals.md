# 🟣 Module 3 — SOC Fundamentals

1️⃣
# 🏢 ═════ What is a Security Operations Center (SOC)? ═════ 🏢

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
# 👨‍💻 ═════ Roles & Responsibilities of a SOC Analyst ═════ 👨‍💻
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
# 🔄 ═════ SOC Workflow ═════ 🔄
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
                                                                    ↓                  ↓
                                                              False Positive        True Positive
                                                                    ↓                  ↓
                                                              Close Alert     Escalate Investigation
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
