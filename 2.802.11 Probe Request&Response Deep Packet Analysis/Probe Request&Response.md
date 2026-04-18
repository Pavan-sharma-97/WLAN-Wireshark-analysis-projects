📡 802.11 Probe Request/Response Deep Packet Analysis

Advanced WLAN MAC Layer Analysis Project

📌 Project Overview

This project provides an in-depth analysis of IEEE 802.11 management and control frames, focusing on:

Probe Request / Probe Response exchange

Beacon interaction

ACK/control flow

Information Elements (IEs) decoding

Rate adaptation behavior

Channel and RF characteristics


The analysis is performed using real packet captures, interpreting MAC headers, frame fields, and PHY metadata to understand how Wi-Fi discovery and association works at a low level.


---

🎯 Objectives

Decode and interpret 802.11 MAC frames at byte-level granularity

Understand active scanning workflow (Probe Request → Response → ACK)

Analyze SSID discovery (broadcast vs directed)

Examine Supported Rates, HT/VHT capabilities

Study channel utilization and RF conditions

Correlate control frames (ACK) with reliability mechanisms



---

🧠 Key Concepts Covered

1. 802.11 Frame Types

Management Frames

Probe Request

Probe Response

Beacon


Control Frames

ACK




---

2. Probe Request Analysis

🔍 Observations:

Type/Subtype: Management / Probe Request

Destination: FF:FF:FF:FF:FF:FF (Broadcast)

SSID Cases:

Empty SSID → Wildcard scan

Specific SSID ("OPEN") → Directed scan



💡 Insights:

Clients perform active scanning by broadcasting probe requests

Empty SSID indicates search for all available networks

Directed probe reduces scan overhead for known SSIDs



---

3. Probe Response Analysis

🔍 Observations:

Type/Subtype: Management / Probe Response

Source = BSSID → Access Point identity

Destination → Specific client


📦 Key Information Elements:

SSID

Example: MRN-EAP, OPEN


Supported Rates

24, 36, 48, 54 Mbps


HT Capabilities (802.11n)

VHT Capabilities (802.11ac)

Country Code

Regulatory domain (e.g., AU)


QBSS Load

Channel utilization

Station count



💡 Insights:

AP advertises capabilities + network identity

Supported rates define basic vs optional data rates

QBSS helps in load-aware client decisions



---

4. ACK Frame Analysis

🔍 Observations:

Type/Subtype: Control / ACK

Receiver: Transmitter of previous frame

Very short frame (14 bytes)


💡 Insights:

Ensures reliability in wireless medium

Immediate response → confirms successful reception

Critical for CSMA/CA operation



---

5. Frame Exchange Flow

📊 Typical Sequence Observed:

1. Client → Probe Request (Broadcast)


2. AP → Probe Response (Unicast)


3. Client → ACK


4. AP → Beacon (Periodic)



💡 Key Understanding:

Active scanning is client-driven

AP responds only when it matches SSID conditions

ACK ensures loss recovery mechanism



---

6. Data Rate Behavior

🔍 Observations:

Probe Request → 6 Mbps

Probe Response → 24 Mbps

ACK → 24 Mbps


💡 Insights:

Lower rates used for robust transmission

Higher rates used when link quality permits

Control frames often follow basic rate set



---

7. Channel & RF Analysis

Channel: 149 (5 GHz band)

Frequency: 5745 MHz

Signal Strength: ~ -41 to -45 dBm

Noise Level: ~ -93 to -95 dBm


💡 Insights:

Strong SNR → supports higher data rates

Clean RF environment → low interference

5 GHz preferred for higher throughput



---

8. Multi-BSSID Observation

Same AP vendor with:

Different BSSID values

Different SSIDs



💡 Insight:

Indicates multiple virtual APs (VAPs)

Common in enterprise deployments



---

🧪 Tools Used

Wireshark (Packet Capture & Analysis)

802.11 Protocol Dissector

RF Metadata Analysis



---

🧬 Deep Technical Takeaways

Active scanning is probabilistic + optimized

Management frames carry rich capability negotiation data

Control frames (ACK) are fundamental for reliability

Rate selection is dynamic and environment-dependent

APs broadcast network intelligence via IEs

WLAN is not just data transfer → it's negotiation + adaptation



---

🚀 What This Project Demonstrates

✅ Strong understanding of 802.11 MAC layer internals
✅ Ability to interpret real packet captures
✅ Knowledge of RF + protocol interaction
✅ Exposure to enterprise Wi-Fi behaviors
✅ Skills relevant to:

WLAN Firmware Engineering

Driver Development

Protocol Stack Analysis

Performance Optimization



---

📈 Future Enhancements

Add 802.11ax (HE) frame analysis

Study MU-MIMO & OFDMA behavior

Analyze roaming (802.11r/k/v)

Build automated packet parser scripts

Correlate with throughput & latency metrics



---

🏁 Conclusion

This project provides a deep dive into Wi-Fi discovery and communication mechanisms, demonstrating how devices:

Discover networks

Exchange capabilities

Adapt transmission rates

Maintain reliable communication


It reflects a system-level understanding of WLAN, aligning with real-world expectations in chipset companies like Qualcomm and Broadcom.

