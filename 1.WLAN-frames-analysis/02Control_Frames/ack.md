# 🟧 ACK Frame (Subtype 0x0C)

## Purpose
Confirms successful reception of a unicast frame.

## Function
- Sent after any unicast Data, QoS Data, or management frame.
- Not used for multicast.

## Fields
- Receiver Address (RA)
- Duration (usually very short Nav=0)

## Frame Details
- Type: 01
- Subtype: 1100