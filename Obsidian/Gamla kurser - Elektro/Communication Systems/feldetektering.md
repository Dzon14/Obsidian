---
tags: [komsys]
aliases: [error detection]
---
# Feldetektering 
Störningar på länkar kan bidra till bitfel (bit error). Alltså att man tolkar en etta som nolla eller tvärtom.

- Man lägger till en eller flera bitar i slutet av ett datapaket. Värdet på dessa räknas ut mha bitarna i [[datapaket|datapaketet]]. Mottagaren gör samma beräkning och jämför med de extra bitarna. 

## Error detection process
![[Pasted image 20230123154046.png|500]]

## Error detection schemes
- [[paritetsbit]]
- [[kontrollsumma]]
- [[cyklisk redundanscheck]]

## Error types
![[Pasted image 20230123153652.png|500]]



## Error correction
1. Forward Error Correction (FEC)
	- Send each bit multiple times
	- Decode according to majority decision
2. Retransmission
	- Resend the entire [[datapaket|frame]]