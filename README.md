# WLAN-Wireshark-analysis-projects
Practical WLAN (802.11) analysis using Wireshark with real packet captures. Explore probe, authentication, association, and data flows, apply filters, and debug connectivity issues. Built to develop strong packet-level insight for wireless protocol engineering and Wi-Fi troubleshooting roles.

### *Advanced 802.11 MAC‑Layer Analysis • Wireshark Deep Dives • Real‑World WLAN Debugging*

Practical WLAN (802.11) analysis using Wireshark with real packet captures.  
Explore probe, authentication, association, and data flows, apply industry‑grade filters, and debug real connectivity issues.  
Built to develop strong **packet‑level insight** for **wireless protocol engineering**, **Wi‑Fi validation**, and **chipset debugging** roles.

A comprehensive engineering‑grade repository focused on **802.11 Wi‑Fi protocol analysis**, **MAC‑layer frame decoding**, and **practical troubleshooting techniques** used by leading wireless companies like **Qualcomm**, **Broadcom**, **Intel**, **Mediatek**, and **Marvell**.

This project demonstrates end‑to‑end WLAN expertise through structured Wireshark analysis, including:

*   Detailed frame breakdowns
*   Full Wi-Fi connection flows
*   QoS + EDCA behavior
*   Block‑ACK & A‑MPDU aggregation
*   Power‑save & U‑APSD signaling
*   WPA2/WPA3 security packet flows
*   Roaming (11k/11v/11r)
*   Radiotap PHY interpretation

It serves as a practical showcase of skills relevant to **Wireless System Test**, **Wi‑Fi Validation**, **Modem/WLAN Firmware**, **Protocol Engineering**, and **Chipset Debugging** roles.

***

# 🎯 **Objectives of This Repository**

### ✔ Demonstrate expert‑level knowledge of IEEE 802.11 MAC

Covers frame structure, A1–A4 addressing, Frame Control bits, QoS fields, Sequence Control, fragmentation, and encryption encapsulation.

### ✔ Show proficiency in Wireshark debugging

Includes display filtering, radiotap analysis, MCS/NSS/GI interpretation, aggregation analysis, and packet‑level troubleshooting.

### ✔ Highlight real‑world wireless engineering skills

Aligns directly with chipset development workflows such as bring‑up, interoperability testing, roaming validation, and performance debugging.

### ✔ Provide a clean, structured knowledge base for WLAN analysis

Useful for:

*   Technical interviews
*   Lab debugging
*   Wireless protocol learning
*   Reverse engineering
*   PCAP‑based problem solving

***

# 📡 **802.11 Frame‑Level Analysis Included**

## 🟦 **Management Frames**

Complete, per‑field analysis of:

*   Beacon
*   Probe Request / Probe Response
*   Authentication
*   Association / Reassociation
*   Disassociation & Deauthentication
*   Action Frames (11k / 11v / 11r / CSA / QoS actions)
*   TIM, RSN, HT/VHT/HE elements

## 🟧 **Control Frames**

Includes detailed breakdowns of:

*   RTS / CTS
*   ACK
*   PS‑Poll
*   Block ACK (BA)
*   Block ACK Request (BAR)
*   CF‑End & CF‑End + CF‑ACK

## 🟥 **Data Frames**

Analysis of:

*   Legacy Data
*   QoS Data (WMM / 802.11e)
*   QoS Null & Null Data
*   A‑MPDU subframes & aggregation logic
*   Protected Data (CCMP/GCMP)
*   Block‑ACK reordering windows

***

# 🔁 **Complete Wi‑Fi Connection Flow Decoded**

Each major connection step is captured and analyzed:

### 1️⃣ Active & Passive Scanning

Probe Requests, capability matching, SSID filtering.

### 2️⃣ Authentication

802.11 Open System, WPA2/WPA3 initiation.

### 3️⃣ Association

Capability negotiation, Listen Interval, Supported Rates, RSN IE processing.

### 4️⃣ WPA2/WPA3 4‑Way Handshake

ANonce/SNonce exchange, MIC verification, PTK/GTK installation.

### 5️⃣ Encrypted Data Transfer

QoS buffering, EDCA behavior, BA windows, AMPDU chains.

### 6️⃣ Roaming (802.11k/v/r)

Neighbor reports, BSS Transition Management, Fast Transition.

***

# 🛠️ **Chipset‑Relevant Insights (Qualcomm‑Style)**

This repository reflects the type of analysis performed in:

*   Wi‑Fi modem bring‑up
*   Firmware validation
*   Interoperability testing (IOT)
*   Field/callbox debugging
*   PHY/MAC issue reproduction
*   Throughput + latency investigations

Topics covered include:

*   AMPDU aggregation & Block‑ACK windows
*   TID → Access Category mapping
*   EDCA contention parameters
*   Retry/Sequence Control behavior
*   U‑APSD / TIM / EOSP power‑save signaling
*   Trigger‑based uplink fundamentals (11ax)
*   Radiotap fields: MCS, NSS, GI, BW, RSSI

***

# 🔍 **Useful Wireshark Filters**

```bash
wlan.fc.type_subtype == 0x08      # Beacon
wlan.fc.type_subtype == 0x04      # Probe Request
wlan.fc.type_subtype == 0x05      # Probe Response
wlan.fc.type_subtype == 0x28      # QoS Data
wlan.fc.protected == 1            # Encrypted frames
wlan.qos.tid == 6                 # Voice traffic (AC_VO)
wlan.ba                            # Block ACK frames
eapol                               # WPA2/WPA3 4-Way Handshake
```

These filters are **highly relevant** for:

*   Debugging association/auth flow
*   Examining roaming triggers
*   Analyzing aggregation (AMPDU)
*   Validating QoS prioritization
*   Debugging connection drops
*   Understanding protected frame exchanges

***ce README with visuals + TOC + banner.”**

