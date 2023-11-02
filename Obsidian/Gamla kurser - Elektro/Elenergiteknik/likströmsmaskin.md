---
tags: [elenergi]
aliases: [DC-motor]
---
# Likströmsmaskin
![[Pasted image 20230119114613.png|400]]
[DC Motor, How it works? - YouTube](https://www.youtube.com/watch?v=LAtPHANEfQo&ab_channel=Lesics) 

## Omkoppling 
Kom ihåg att från [[synkronmaskin]] har vi att inducerad spänning $e(t)$ byter tecken vid $\theta=0$ och $180 \degree$.
Samma gäller vridmomentet T

- För en omkoppling vid nolläge på e och T så får vi teckenbyten och vi kastar om anslutningar till rotorn vid $\theta=0$ och $180 \degree$..
![[Pasted image 20230119112507.png|500]]
- Innanför omkopplaren: Sinus. Utanför: $u \geq 0$

- Omkoppling görs med [[kommutator]]
- Med [[kommutator]] så får vi **likspänning**

## Två lindningar
Två lindningar ger jämnare likspänning
- Andra lindningen förskjuten $90 \degree$ + kommutering varje $90 \degree$
- $e_{1}(t) = \hat{e}sin \omega t$, $e_{2}(t) = \hat{e}cos \omega t$, $e(t) = max(e_{1},-e_{1}, e_{2}, -e_{2})$

## Tre lindningar
- inducerad spänning från tre lindningar känner vi till 
		- Studera e(t) från [[synkronmaskin]] likriktad med trefasig diodbrygga
- Så skulle e(t) från likströmsgenerator med tre lindningar se ut
- Kommutatorn är en **mekanisk likriktare**

## Många lindningar
Verkliga likströmsmaskiner har betydligt fler lindningar och kommutatorsegment och vinkeln $\theta$ hålls nära $90 \degree$
- Med finindelad kommutator kan e(t) betraktas som likspänning
- Ex: dammsugarmotor (likströmsmaskin) som matas med växelspänning)

## Likströmsmaskin - induktion och moment
Inducerad spänning vid kommutator med många segment
- Under ett varv snuttar av $2NBl \omega rsin \omega t$ nära $90 \degree$
- Idealt $\theta = 90 \degree \rightarrow$ likspänning $E = 2NBlr \omega = k \omega$
- k beror på B och geometri

Vridmoment vid konstant ström
- Under ett varv snuttar av $2NBilrsin \omega t$ nära $90 \degree$
- Idealt $\theta = 90 \degree \rightarrow moment \ T=2NBlri \omega = ki \omega$ (samma k som ovan)
E induceras i rotorlindningen som då är ankarlindning
$E_{a}=k \omega$ och $T = ki_{a}$ med a för ankare aeller armature

## Ekvivalent schema och dynamisk modell
- Kommutatorn gör AC-källan till DC-källa:
![[Pasted image 20230119120710.png]]

## Likströmsmaskin i tomgång
![[Pasted image 20230119120804.png|400]]
- Om $E_{a}=U_{a}$ (eller om motorn ej ansluten) blir $i_{a}=0$ 
		- Vridmomentet T=0 och maskinen går i tomgång
- Eftersom $U_{a} = E_{a} = k \omega$ blir $U_{a}$ ett mått på varvtalet
- En "tachometer" är en likströmsmaskin i tomgång och används som varvtalsgivare

## Likströmsmaskinens driftlägen
1. Generatordrift
   - Momentkälla driver axeln, $E_{a}$ är källa och matar elkrets som bromsar elektriskt, $E_{a} > U_{a} \rightarrow i_{a} > 0$ 
2. Tomgång
   - Rotation utan elektrisk/mekanisk last, $E_{a} = U_{a} \rightarrow i_{a} = 0$
3. Motordrift
   - Spänningskälla driver axeln som bromsas mekaniskt
   -  $E_{a}$ är mot-EMK, $E_{a} < U_{a} \rightarrow i_{a} < 0$
Precis som i [[synkronmaskin|synkronmaskinen]] beror $E_{a}$ enbart av rotationen, inte av vad som orsakat den. 

## Likströmsmaskinen i stationär drift
- Stationaritet: konstant $U_{a}$ och $T_{m}$ så $\frac{dx}{dt} = 0$
- Bestäm $\omega (T_{m})$ där $T_{m}$ är lastmoment
![[Pasted image 20230119121607.png]]

## Moment-varvtalskarakteristik $T(\omega)$
- Moment T maskinen utvecklar vid olika $\omega$ (rad/s) eller hellre n (rpm=revolutions per minute)
- Ofta föredras positivt T för motordrift
![[Pasted image 20230119121742.png]]

## Seriemagnetiserad likströmsmaskin
- Med permanentmagneter är maskinen **konstantmagnetiserad**
- Permanentmagneterna kan ersättas med en fältlindning och maskinen blir då **separatmagnetiserad**
		- Fältströmmen $i_{f}$ styr B, så $$k=k_{2}i_{f} \Rightarrow E_{a}=k_{2}i_{f}\omega \ \text{ och } \ T=k_{2}i_{f}i_{a}$$
- Fältlindning och ankarlindning kan kopplas i serie och maskinen blir då **seriemagnetiserad** och $i_{f}=i_{a}$
		- Vridmomentet $T=k_{2}i_{f}i_{a}=k_{2}i_{a}^{2}$ så $T > 0$ även för $i_{a}<0$

Den seriemagnetiserade motorn kan drivas med både AC och DC och kallas därför [[universalmotor]] eller allströmsmotor
- Vanlig i dammsugare, borrmaskiner, hårtorkar mm.

## Likströmsmotor och driftkvadranter
![[Pasted image 20230206105436.png|600]]
