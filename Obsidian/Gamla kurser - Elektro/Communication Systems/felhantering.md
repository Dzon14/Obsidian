---
tags: [komsys]
aliases: [error control]
---
# Error Control
- För att säkerställa att data kommer fram korrekt till mottagaren.
Två sätt:
- Forward Error Correction (FEC) - mottagaren korrigerar bitfel själv.
	  - Bygger på samma princip som feldetektering, sändaren lägger till bitar,
- Retransmission - sänder om hela [[datapaket|datapaketet]](ramen)

"Flow control" - the receiver acknowledges (ACK) all correctly received packets. 
![[Pasted image 20230124114603.png|400]]

## Felhantering via omsändningar (Retransmission)
Att ett [[datapaket|paket]] kommer fram rätt bekräftas av mottagaren med ACK. Detta an vara positiv och mottagaren talar om vilket sekvensnummer som den väntar på. Är den istället negativ (NAK) talar mottagaren om vilka sekvensnummer som den inte har tagit emot rätt

Finns två olika sätt:
- [[stop-and-wait ARQ]]
- [[go-back-n ARQ]]
(Även [[selective repeat ARQ]])