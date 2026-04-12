📡 WLAN Beacon Frame Analysis (IEEE 802.11)

🚀 Project Overview

This project focuses on analysis of IEEE 802.11 Beacon Frames captured using Wireshark. It demonstrates how an Access Point (AP) advertises its capabilities and how a client (STA) interprets them during network discovery.

The project is designed with an industry-oriented WLAN Protocol Engineer perspective, emphasizing practical packet analysis, key Information Elements (IEs), and real-world debugging relevance.

---

🎯 Objective

- Analyze Beacon Management Frames
- Understand Information Elements (IEs) using TLV format
- Interpret real capture values into practical WLAN behavior
- Build a strong base for protocol-level debugging

---

🧠 Key Concepts

- IEEE 802.11 Management Frames
- Beacon Frame Structure
- Information Elements (Tag-Length-Value)
- PHY & MAC interaction
- WLAN Security (RSN / WPA2)

---

📊 Beacon Frame Analysis

1️⃣ SSID Parameter Set (Tag 0)

- SSID: "test-ap"
- Length: 7

Analysis:

- Network is broadcast (not hidden)
- Used during network discovery
- Primary identifier of the AP

---

2️⃣ Supported Rates (Tag 1)

- Rates: 1, 2, 5.5, 11 Mbps
- Marked as Basic Rates

Analysis:

- Indicates 802.11b legacy support
- Basic rates are mandatory for all clients
- Ensures backward compatibility

---

3️⃣ DS Parameter Set (Tag 3)

- Channel: 1

Analysis:

- AP operates in 2.4 GHz band
- Helps STA tune to correct channel
- Important for interference analysis

---

4️⃣ RSN Information (Tag 48)

- RSN Version: 1
- Group Cipher: AES (CCMP)
- Pairwise Cipher: AES (CCMP)
- AKM: PSK

Analysis:

- Network uses WPA2-Personal
- Strong encryption using AES (CCMP)
- No legacy security (TKIP)

---

5️⃣ RSN Capabilities

- Management Frame Protection: Not supported
- Pre-authentication: Disabled
- Replay Counters: 1

Analysis:

- No 802.11w (Protected Management Frames)
- Indicates standard security configuration
- Helps identify security limitations

---

🚀 Advanced PHY Capabilities

6️⃣ HT Capabilities (802.11n)

Purpose: Defines high-throughput features

Includes:

- Channel Width: 20/40 MHz
- Short Guard Interval (SGI)
- MCS (Modulation Coding Scheme)
- Spatial Streams

Analysis:

- Indicates 802.11n support
- Enables higher throughput via MIMO and channel bonding
- Important for real data rate estimation

---

7️⃣ VHT Capabilities (802.11ac)

Purpose: Defines very high throughput features

Includes:

- Channel Width: 80/160 MHz
- MCS Map
- Beamforming

Analysis:

- Indicates 802.11ac support
- Enables high-speed WiFi (hundreds of Mbps to Gbps)
- Critical for modern device compatibility

---

⚙️ Engineering Relevance

Why Beacon Frames Matter

- First communication from AP to STA
- Used for:
  - Network discovery
  - Capability advertisement
  - Roaming decisions

Practical Use Cases

- Debugging connection failures
- Analyzing rate mismatches
- Understanding capability negotiation
- Identifying channel usage

---

🛠️ Tools Used

- Wireshark
- WLAN Adapter (Monitor Mode recommended)

---

📂 Project Structure

/pcaps
  └── beacon_capture.pcapng

/docs
  └── beacon_analysis.md

/screenshots
  └── wireshark_tags.png

---

🔥 Key Takeaways

- Beacon frames provide a complete snapshot of AP capabilities
- Information Elements follow TLV format
- Security and PHY capabilities are advertised before association
- HT/VHT define actual throughput performance
- Strong beacon understanding = strong WLAN foundation

---

📈 Future Scope

- Add HE (802.11ax / WiFi 6) analysis
- Compare multiple AP beacon frames
- Automate parsing using Python (Scapy)

---

👨‍💻 Author

This project is part of a focused preparation toward WLAN Protocol Engineering roles, emphasizing practical packet analysis and real-world relevance.