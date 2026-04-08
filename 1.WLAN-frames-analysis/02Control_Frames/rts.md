# 🟦 RTS – Request to Send (Control Frame, Subtype 0x0A)

## Purpose
Used to reserve the wireless medium before sending large frames.  
Prevents collisions by triggering CTS from receiver.

## Fields
- **Receiver Address (RA)** – the intended receiver
- **Transmitter Address (TA)** – sender
- **Duration** – time reserved for RTS → CTS → DATA → ACK

## Used in:
- Hidden node situations
- When RTS/CTS threshold is exceeded

## Frame Details
- Type: 01
- Subtype: 1010 (0x0A)