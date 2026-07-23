# 🟢 Chapter 7 — Digital Forensics

1️⃣
# 🔎 ═══ What is Digital Forensics ═══ 🔎? 
**Digital Forensics** is the process of **identifying, collecting, preserving, examining, analyzing, and reporting digital evidence** from computers, mobile devices, networks, cloud systems, and other digital devices.
Digital Forensics is based on the same principle as **Locard's Exchange Principle**, which states:
> **"Every contact leaves a trace."** — *Dr. Edmond Locard*
Similarly, in the digital world, **every digital action leaves a trace**. Activities such as logging in, opening files, browsing websites, sending emails, downloading files, or running programs generate digital artifacts like logs, metadata, browser history, registry entries, and network records. Digital Forensics examines these traces to determine **what happened, how it happened, who was involved, and what evidence can be recovered** during a cybersecurity incident.

## Why Is Digital Forensics Used?
Digital Forensics is **not limited to IT organizations**. Any organization that uses computers, mobile devices, servers, or digital systems may require Digital Forensics to investigate incidents, recover evidence, and understand what happened during an investigation.
## 📋 Digital Forensics in Organizations vs. SOC
| 🏢 **Digital Forensics in Organizations** | 👨‍💻 **Digital Forensics for SOC Analysts** |
|------------------------------------------|--------------------------------------------|
| Investigates cyber incidents and security breaches. | Investigates security alerts and suspicious activities. |
| Collects and preserves digital evidence. | Analyzes evidence to determine the root cause of an incident. |
| Helps recover deleted or hidden data. | Identifies compromised systems, users, and files. |
| Supports legal investigations and compliance requirements. | Supports incident response and threat hunting activities. |
| Improves security after an incident. | Creates attack timelines and recommends remediation. |
| Used in banks, hospitals, government agencies, educational institutions, law enforcement, and IT organizations. | Primarily used by SOC teams to investigate, contain, and respond to cyber threats. |

## Example
A SOC Analyst receives an alert about suspicious activity on an employee's computer. During the investigation, the analyst examines system logs, browser history, downloaded files, running processes, and deleted data. The investigation reveals that the employee opened a malicious email attachment, which installed malware and connected to an attacker's server. Using **Digital Forensics**, the analyst reconstructs the attack timeline, identifies the affected systems, and collects evidence to support incident response.

> **Remember:**
 • Digital Forensics follows the principle that **every digital action leaves a trace**, making investigations possible.
 • It focuses on **identifying, collecting, preserving, examining, analyzing, and reporting digital evidence**.
 • Digital Forensics is used across many industries—not just IT—to investigate digital incidents and support security and legal investigations.

## 💡 Easy Way to Remember
**Digital Forensics = Identify → Collect → Preserve → Examine → Analyze → Report**
**Locard's Principle = Every Contact Leaves a Trace**
**Digital Forensics = Every Digital Action Leaves a Trace**

2️⃣
## 🔗 What is Chain of Custody?
**Chain of Custody (CoC)** is the documented process of recording **how digital evidence is collected, handled, preserved, transferred, stored, and presented** throughout an investigation.
It ensures that the evidence remains **authentic, unaltered, and trustworthy** from the moment it is collected until the investigation is completed or the evidence is presented in court.

## Why is Chain of Custody Important?
Chain of Custody is important because it:
- 🛡️ Protects the integrity of digital evidence.
- 📝 Records every person who handled the evidence.
- ⚖️ Ensures the evidence is legally admissible.
- 🔍 Prevents evidence from being altered, lost, or tampered with.
- 🤝 Increases the credibility of the investigation.

## Who Maintains the Chain of Custody?
The **Chain of Custody** is maintained by **every authorized person who handles the evidence** during an investigation.
In a SOC, it usually begins with the **L1 SOC Analyst**, continues through the **L2 SOC Analyst/Incident Response Team**, and, if required, is handed over to a **Digital Forensic Investigator**. The Chain of Custody remains active until the evidence is securely stored, archived, or the investigation is officially closed.

## Example
A **L1 SOC Analyst** receives a malware alert and collects the affected system's logs and file hash. The evidence is then transferred to the **L2 SOC Analyst** for further investigation. If a detailed forensic examination is required, it is handed over to the **Digital Forensic Investigator**. Throughout the investigation, every transfer and action performed on the evidence is documented to maintain the Chain of Custody.

> **Remember:**
 • Every person who handles the evidence must document their actions.
 • If the Chain of Custody is broken, the evidence may lose its credibility or legal admissibility.
 • The Chain of Custody begins when evidence is collected and ends only after the investigation is completed and the evidence is securely stored or presented.

# 💡 Easy Way to Remember
**Chain of Custody = Collect → Document → Preserve → Transfer → Analyze → Store**

3️⃣
# 💾 ═══ Evidence Acquisition ═══ 💾
**Evidence Acquisition** is the process of **collecting and securing digital evidence** from a device or system without altering its original data. The objective is to obtain a reliable copy of the evidence while preserving its integrity for further investigation.

## How is Evidence Acquisition Maintained?
Evidence Acquisition is maintained by:
- 🔒 Collecting evidence without modifying the original data.
- 📝 Documenting when, where, how, and by whom the evidence was collected.
- 🛡️ Preserving the integrity of the evidence throughout the investigation.
- 🔗 Following the **Chain of Custody** during every stage of evidence handling.

> **Remember:**
 • Always preserve the original evidence.
 • Never modify the original data during acquisition.
 • Follow the Chain of Custody to maintain evidence integrity.

## 💡 Easy Way to Remember
**Evidence Acquisition = Collect → Secure → Preserve**

4️⃣
# 🔍 ═══ Types of Digital Forensics ═══ 🔍
Digital Forensics is divided into different branches based on the type of digital evidence being investigated. Each branch focuses on collecting, preserving, and analyzing evidence from a specific source.

# A) 💽 Disk Forensics
**Disk Forensics** is the process of collecting, preserving, and analyzing data stored on storage devices such as HDDs, SSDs, USB drives, and external storage devices.
Investigators never perform routine analysis on the original storage device. Instead, they create a **forensic image** and analyze the copied evidence.

## Disk Evidence Collection & Preservation
```text
Receive and Secure the Compromised System
                    ↓
        Check the Power Condition
          ┌─────────┴─────────┐
          │                   │
     System is ON        System is OFF
          │                   │
Do Not Shut It Down      Do Not Turn It On
          │                   │
Capture Volatile Data    Remove & Access the Disk
(using a trusted RAM     (remove HDD/SSD or connect
acquisition tool stored  the storage device to a
on a clean USB flash     forensic workstation)
drive)
          │                   │
          └─────────┬─────────┘
                    ↓
Connect the Original Disk to a Write Blocker
                    ↓
Create a Bit-by-Bit Forensic Image
                    ↓
Calculate & Verify Hash Values
                    ↓
Securely Preserve the Original Disk
                    ↓
Analyze the Forensic Image
                    ↓
Document Every Step
(Chain of Custody)
```
> **📝 Remember:**
 • If the system is ON, capture RAM first.
 • If the system is OFF, never power it on.
 • Analyze the forensic image, not the original disk.
---
# B) 🌐 Browser Forensics
**Browser Forensics** is the process of collecting, preserving, and analyzing browser artifacts to investigate a user's web activities.

## Browser Evidence Collection & Preservation
```text
Identify the Browser
        │
        ├──► Chrome
        ├──► Edge
        ├──► Firefox
        └──► Other Browser
               │
               ▼
Collect Browser Artifacts
(History, Cookies, Cache,
Downloads, Bookmarks,
Saved Credentials)
               │
               ▼
Create a Forensic Copy
               │
               ▼
Calculate & Verify Hash Values
               │
               ▼
Analyze Browser Artifacts
               │
               ▼
Document Every Step
(Chain of Custody)
```
> **Remember:**
 • Browser evidence is collected from browser artifacts.
 • Always preserve the original browser data.
---
# C) 🧠 Memory Forensics
**Memory Forensics** is the process of collecting and analyzing **volatile data stored in RAM** while the system is running.

## Memory Evidence Collection & Preservation
```text
Running System
        │
        ▼
Insert a Clean USB Flash Drive
(with a trusted RAM
acquisition tool)
        │
        ▼
Capture Memory Dump
        │
        ▼
Save Memory Dump
        │
        ▼
Calculate & Verify Hash Values
        │
        ▼
Preserve the Original Memory Dump
        │
        ▼
Analyze the Working Copy
        │
        ▼
Document Every Step
(Chain of Custody)
```
> **📝 Remember:**
 • RAM is volatile and must be captured before shutdown.
 • Investigators analyze the memory dump, not the live RAM.
---
# D) 📧 Email Forensics
**Email Forensics** is the process of collecting, preserving, and analyzing email evidence to investigate phishing, spoofing, malware delivery, and other email-related attacks.

## Email Evidence Collection & Preservation
```text
Identify Suspicious Email
        │
        ▼
Collect Original Email
        │
        ├──► Email Header
        ├──► Attachments
        ├──► Message Body
        └──► Metadata
               │
               ▼
Preserve Original Email
               │
               ▼
Calculate & Verify Hash Values
               │
               ▼
Analyze Email Evidence
               │
               ▼
Document Every Step
(Chain of Custody)
```
> **Remember:**
 • Preserve the original email, including headers and attachments.
 • Email headers are one of the most important sources of forensic evidence.
---

## 💡 Easy Way to Remember
- 💽 **Disk Forensics** → Storage Devices
- 🌐 **Browser Forensics** → Browser Artifacts
- 🧠 **Memory Forensics** → RAM (Volatile Data)
- 📧 **Email Forensics** → Emails, Headers & Attachments
