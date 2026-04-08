# 🔎 Wi‑Fi Probe Flow (Active Scanning)

This is the first step in the Wi‑Fi connection process.  
A STA scans the environment to discover APs.

---

# 📡 Step‑by‑Step

## 1. Probe Request (STA → Broadcast)
- Type: Management
- Subtype: Probe Request (0x04)
- Address1: FF:FF:FF:FF:FF:FF
- Address2: STA MAC
- Address3: Broadcast

### Fields
- SSID (may be wildcard)
- Supported Rates
- HT/VHT/HE Capabilities

---

## 2. Probe Response (AP → STA)
- Contains Beacon‑like IEs.
- Advertises:
  - SSID
  - Supported PHY
  - Channel
  - Security (RSN)

STA now knows AP’s capabilities.