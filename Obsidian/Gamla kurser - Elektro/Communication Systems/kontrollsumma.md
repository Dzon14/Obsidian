---
aliases: [checksum]
tags: [komsys]
---
# Kontrollsumma
Ännu ett sätt att detektera bitfel. 
- Sändaren delar upp data i segment bestående av ett antal bitar. Alla dessa segment adderas sedan till varandra och resultatet blir en delsumma. Eventuella carry bits adderas sedan och bildar en slutsumma.
- Mottagaren delar upp datan i samma segment som sändaren. Även kontrollsumman. Segmenten adderas och carry bits adderas. Sedan tas komplementet av denna summa, om den är noll har [[datapaket|datapaketet]] tagits emot korrekt. 

##### Checksum
A bit more complicated method. We add more bits.
A better system.
Used by several internet protocols
![[Pasted image 20230123154805.png|550]]


Add m bit sequences together (binary addition) and then add the answer with a part of itself. Then the complementary is the answer we're looking for.