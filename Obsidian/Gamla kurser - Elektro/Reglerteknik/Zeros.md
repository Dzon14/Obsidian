---
aliases: [zero, nollställe, nollstället, nollställen]
tags: [matte]
---

# Zeros

see [[Z-transform]]

## Reglerteknik 
Nollor har en stor betydelse vid börvärdeshanteringen (gör länk).


![[Pasted image 20220927164004.png]]

- Lägg till ett nollställe i z $$G_{1}= G(1- \frac{s}{z})$$
Vi kan nu beskrive det med 
![[Pasted image 20220927164021.png]]

- Addera viktning av $\dot{y}$ till $y$. 
Vi får $$y_{1}= y- \frac{1}{z}\dot{y}$$
$y_{1}$ beskrivs som en viktad summa av den gamla mätsignalen och dess derivata.

Nollställets position $z$ avgör hur denna viktning sker. 
- Störst inverkar nära origo, då $\lvert z \rvert$ är liten. 

![[Pasted image 20220927164522.png]]