# 📡 Association Response Frame (Management – Subtype 1)

## Purpose
AP sends this after receiving an Association Request.  
It tells the STA whether it's allowed to join.

---

## Frame Control
- Type: 00
- Subtype: 0001

---

## Address Fields
| Address | Meaning |
|--------|---------|
| Address1 | STA |
| Address2 | AP |
| Address3 | BSSID |

---

## Frame Body
| Field | Meaning |
|--------|---------|
| Capability Info | AP capability |
| Status Code | 0 = Success, Others = Failure |
| AID | Association ID assigned to STA |
| Supported Rates | Required rates |

---

## Typical Status Codes
- 0 = Success  
- 17 = AP Full  
- 18 = Unauthorized  
- 31 = Unsupported Capability  

---

## When It Appears
- After STA sends Association Request