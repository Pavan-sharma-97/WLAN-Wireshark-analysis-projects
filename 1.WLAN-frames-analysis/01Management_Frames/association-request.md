# 📡 Association Request Frame (Management – Subtype 0)

## 📝 Purpose
The Association Request is sent by a STA when it wants to join a BSS (infrastructure mode).  
It carries the STA’s capabilities and SSID it wishes to join.

---

## ✔ Frame Control Breakdown
- **Type**: 00 (Management)
- **Subtype**: 0000 (Association Request)
- **ToDS/FromDS**: 0 / 0
- **Protected**: 0 (unencrypted)

---

## ✔ Address Fields
| Address | Meaning |
|--------|---------|
| Address1 | Receiver = AP |
| Address2 | Transmitter = STA |
| Address3 | Destination = BSSID of AP |

---

## ✔ Frame Body Fields
| Field | Purpose |
|--------|---------|
| Capability Info | STA capability (Short preamble, privacy, QoS, etc.) |
| Listen Interval | How often STA wakes for beacon TIM |
| SSID | ESS name |
| Supported Rates | PHY rates |
| Extended Supported Rates | Additional rates |
| HT Capabilities | 802.11n features |
| VHT Capabilities | 802.11ac features |
| RSN Information Element | WPA2/3 security fields |

---

## ✔ When It's Used
- After Authentication  
- Before 4-way handshake  
- During roaming (Reassociation)

---

## ✔ Wireshark Example Interpretation