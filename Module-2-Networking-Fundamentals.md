# 🔵 Module 2 — Networking Fundamentals

1️⃣
# 🌍 ═════ What is Networking? ═════ 🌍
A **Network** is a collection of **two or more devices** connected together so they can communicate with each other and perform tasks by sharing data and resources.
These devices can be laptops, computers, mobile phones, printers, servers, routers, or any other network-enabled devices.
**Example:** Your laptop, mobile phone, and Wi-Fi router connected together form a **network**.

## What is Networking?
**Networking** is the process of connecting two or more devices and allowing them to communicate and exchange data with each other. In simple words, **Network** is the connection, whereas **Networking** is the communication that happens through that connection.
**Example:** When your mobile phone is connected to Wi-Fi and you open YouTube, your phone sends a request through the network and receives the video from YouTube's server. This entire communication process is called **Networking**.

### Easy Real-Life Example
Imagine your house.
- 🏠 **House** = Your Device (Laptop, Mobile, Computer)
- 🚪 **Main Gate** = Network (The connection or path)
- 👨‍👩‍👧‍👦 **People entering through the gate and talking to you** = Networking (Communication)
Just like people need a gate to enter your house and communicate with you, devices also need a network to communicate with each other.
Without the gate, no one can enter your house.
Similarly, without a network, devices cannot communicate with each other.

#### Why are Networking Fundamentals Important?
Networking Fundamentals help us understand how computers and other devices communicate with each other.
For anyone learning cybersecurity, networking is one of the most important topics because almost every cyber attack takes place over a network. 
Understanding networking helps you:
- 💻 Understand how computers communicate.
- 🔧 Troubleshoot basic network-related problems.
- 🌐 Understand how data travels between devices.
- 🛡️ Understand cyber attacks such as **Phishing, Man-in-the-Middle (MITM), Distributed Denial of Service (DDoS), and Malware**.
- 🔍 Build a strong foundation for cybersecurity, SOC, digital forensics, and incident response.

Without networking knowledge, understanding how cyber attacks happen and how security professionals investigate them becomes much more difficult.

2️⃣
# 🏛️ ═════ OSI Model ═════ 🏛️
The **OSI (Open Systems Interconnection) Model** is a conceptual model that explains **how data travels from one device to another over a network**. It acts like a **roadmap for data communication**, where each of the **seven layers** performs a specific task to ensure data is transmitted correctly from the sender to the receiver.
Understanding the OSI Model helps us identify where communication problems occur and makes troubleshooting networks much easier.

## 📚 The 7 Layers of the OSI Model
| Layer | Name | Purpose | Example |
|-------|------|---------|---------|
| **7** | **Application** | User accesses network services. | Opening YouTube or Gmail. |
| **6** | **Presentation** | Formats and secures the data. | HTTPS encrypting your login. |
| **5** | **Session** | Starts and manages communication. | Joining a Zoom meeting. |
| **4** | **Transport** | Delivers data reliably. | Sending a WhatsApp message. |
| **3** | **Network** | Finds the best path for data. | Router forwarding data. |
| **2** | **Data Link** | Transfers data within the same network. | Laptop sending data to a Wi-Fi printer. |
| **1** | **Physical** | Transmits data through cables or Wi-Fi. | Ethernet cable or Wi-Fi signals. |

### 📞 OSI Model in Real Life
Imagine you're calling your friend.
```text
You open the Phone app
        ↓
🖥️ Application
        ↓
🔒 Presentation (Voice is converted into digital data)
        ↓
🤝 Session (The call connection starts)
        ↓
📦 Transport (Data is divided into packets)
        ↓
🗺️ Network (Finds the best route)
        ↓
🔗 Data Link (Delivers data within the local network)
        ↓
📡 Physical (Data travels as electrical or wireless signals)
        ↓
📱 Friend's phone receives the data
        ↓
Same 7 layers work in reverse
        ↓
🎙️ Your friend hears your voice
```
> **💡 Remember:** Every time data is sent, it moves from **Layer 7 → Layer 1**. When the receiver gets the data, it moves from **Layer 1 → Layer 7**.
