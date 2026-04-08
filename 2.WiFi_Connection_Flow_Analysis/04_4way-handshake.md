# 🔒 WPA2/WPA3 4‑Way Handshake

This generates dynamic encryption keys (PTK, GTK).

---

# 🔐 Steps

## 1. Message 1 (AP → STA)
AP sends:
- ANonce
- RSN Information

---

## 2. Message 2 (STA → AP)
STA replies with:
- SNonce
- MIC (key confirmation)
- RSN Selected Pairwise Cipher

---

## 3. Message 3 (AP → STA)
AP sends:
- GTK (encrypted)
- Install PTK command

---

## 4. Message 4 (STA → AP)
STA acknowledges installation.

---

🔑 After this:  
**Data is encrypted with CCMP/GCMP**