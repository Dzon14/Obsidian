---
tags: [elenergi]
---
# Växelströmsmotor

## Växelströmsmotor i tomgång - sinus
![[Pasted image 20230207211425.png|300]]
- Ett flöde $\vec{\Phi}_{m}$ som roterar med $\omega$ motsvarar spänningen $\vec{E}_{m}$
$$\vec{E}_{m} = - \frac{d \vec{\Phi}_{m}}{dt} = - \frac{d}{dt} \left( \Phi_{m}e^{j \omega t}  \right) = - j \omega \Phi_{m}e^{j \omega t} = -j \omega \vec{\Phi}_{m}$$
- Tolkning: Flödesvektorn spets rör sig med riktning och fart som anges av $- \vec{E}_{m}$.
  I fortsättningen **struntar** vi i minuset
- Trefassinus i trefaslindningar ger spänningsvektorn $E_{m}e^{j \omega t}$

## Växelströms i tomgång - [[pulsbreddsmodulering|PWM]]
![[Pasted image 20230207212120.png]]
- Triangelvågsmodulation med trefassinus ger $E_{m}e^{j \omega t}$ i medel:
	  - Switcha mellan de två bäst riktade aktiva spänningsvektorerna ger medelspänningsvektor med rätt riktning 
	  - Switcha mellan aktiv spänningsvektor och nollvektor ger medelspänningsvektor med rätt belopp
- Kraftelektronik kan ge jämn och fin rotation! (se nedan)

##### Spännings och flödesvektor
![[Pasted image 20230207213103.png]]
- Spänningsvektorer väljs för bästa medelvektor
- Målet är en flödesvektor med en konstant hastighet och längd
		- Spetsen följer då en cirkel $\rightarrow$ vridmomentet konstant
- Resultat med [[pulsbreddsmodulering|PWM]] kan bli ganska nära
	  - I medel följer flödesvektorns spets en cirkel
	  - Litet momentrippel

## [[variabelt varvtal]] för asynkronmotor
![[Pasted image 20230207213553.png]]
