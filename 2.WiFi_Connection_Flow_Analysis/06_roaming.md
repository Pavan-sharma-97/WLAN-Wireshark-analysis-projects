# 🚶 Wi‑Fi Roaming (802.11k/v/r)

When STA switches APs inside same ESS.

---

# 🔧 Mechanisms

## 1. 802.11k
Radio measurements:
- Neighbor Reports
- Beacon Reports

## 2. 802.11v
Network-assisted steering:
- BSS Transition Management

## 3. 802.11r
Fast Roaming:
- Fast Transition Action Frames
- FT 4‑way handshake

---

# 🧩 Flow
1. STA receives neighbor list.
2. STA checks RSSI / channel.
3. STA sends Reassociation Request to target AP.
4. If 11r: FT handshake occurs before roam.