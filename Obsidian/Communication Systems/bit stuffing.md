---
tags: [komsys]
---
# Bit Stuffing
- A way to correct problems when flag and data match

- If given a flag 01111110
- Task: avoid 6 consecutive 1's in payload
- solution:
		- Sender: In payload add a 0 after 5 consecutive 1's
		- Receiver: Remove bit following 5 consecutive 1's
![[Pasted image 20230123153324.png|400]]