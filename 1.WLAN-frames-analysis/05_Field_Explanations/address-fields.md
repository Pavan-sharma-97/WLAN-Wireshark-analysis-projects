# 🏷 Address Fields (A1, A2, A3, A4)

Meaning depends on ToDS/FromDS.

+--------+-----------------+-----------------------------+
| ToDS   | FromDS          | Meaning                     |
+--------+-----------------+-----------------------------+
| 0      | 0               | IBSS                        |
| 1      | 0               | STA → AP                    |
| 0      | 1               | AP → STA                    |
| 1      | 1               | WDS/Mesh                    |
+--------+-----------------+-----------------------------+

## STA → AP (1,0)
- A1 = AP
- A2 = STA
- A3 = Ethernet Destination

## AP → STA (0,1)
- A1 = STA
- A2 = AP
- A3 = Ethernet Destination