# 📄 Legacy Data Frame (Type 10, Subtype 0000)

## Purpose
Carries MSDUs (IP packets, ARP, DHCP, etc.) without QoS enhancements.

## Frame Control
- Type = 2 (Data)
- Subtype = 0 (Data)

## Address Fields Depend on:
- ToDS / FromDS bits

Typical:
- STA → AP (ToDS=1, FromDS=0)
- AP → STA (ToDS=0, FromDS=1)

## Components
- Frame Control
- Duration
- Address1 (RA)
- Address2 (TA)
- Address3 (DA or BSSID)
- Sequence Control
- Payload
- FCS