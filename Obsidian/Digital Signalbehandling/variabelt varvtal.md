---
tags: [elenergi]
---
# Variabelt varvtal 

## Variabelt varvtal för asynkronmotor ([[asynkronmaskin]])
- Enkel styrning av asynkronmotor ev synkronmotor
- Triangelvågsmodulation med trefassinus
- Välj frekvens för rätt synkront varvtal $$n_{syn} = \frac{2 \cdot 60}{p} f_{matning}$$
- Konstant (varvtalsoberoende) flöde $\rightarrow$ lika starkt vid alla varvtal
- $\vec{E}_{m} = - j \omega \vec{\Phi}_{m} \Rightarrow \text{ Konstant } \Phi_{m} \Leftrightarrow \text{ konstant } \frac{E_{m}}{\omega} \text{ kallas U/f-styrning}$ 
- Kvoten $\frac{E_{m}}{\omega}$ för märkflöde vid märkdrift

## Ändring av varvtal och rotationsriktning
- Snabba ändringar i spänning och frekvens ger höga strömmar och mekaniska påkänningar. Använd därför rampbegränsning av börvärde:
![[Pasted image 20230207214239.png]]
- Byte av rotationsriktning görs genom att kasta om switchordningen - växla styrsignal för två bryggben.

## Asynkronmotor med U/f-styrning
![[Pasted image 20230207214328.png]]
- Variera f $\rightarrow$ Synkront varvtal varieras
- Försök hålla U/f konstant
	  - Upp till 50 Hz: konstant flöde och maxmoment, $P_{max} = \omega T_{märk}$
	  - Vid 50 Hz nås märkfrekvens och $P_{max} = \text{ märkeffekt }$
	  - Över 50 Hz: bara f ökar $\rightarrow$ minskande flöde ("fältförsvagning") och minskande maxmoment, $T_{max}= \frac{P_{märk}}{\omega}$