# 🧷 Association Flow (Joining the BSS)

After authentication, the STA requests to join AP’s BSS.

---

# 📝 Steps

## 1. Association Request (STA → AP)
Contains:
- Capability Info
- Listen Interval
- SSID
- Supported Rates
- RSN IE (selects WPA2/WPA3)
- HT/VHT/HE Capabilities

---

## 2. Association Response (AP → STA)
Contains:
- Status Code
- AID (Association ID)
- AP Capability
- Negotiated PHY features

After this step, the STA is authenticated + associated but not yet encrypted.