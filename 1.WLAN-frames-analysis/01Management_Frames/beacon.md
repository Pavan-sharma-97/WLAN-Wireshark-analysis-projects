# 🏳️ Beacon Frame (Subtype 8)

Sent by AP every 100 ms.

---

## Purpose
- Announces SSID
- Parameters needed for STA to join BSS

---

## Key IEs in Beacon
- SSID
- Supported Rates
- TIM (Traffic Indication Map)
- DS Parameter Set (Channel)beacon.md
- RSN (Security)
- HT/VHT Information
- Vendor IEs

---

## Addressing
| Address | Meaning |
|--------|---------|
| A1 | Broadcast |
| A2 | AP |
| A3 | BSSID |