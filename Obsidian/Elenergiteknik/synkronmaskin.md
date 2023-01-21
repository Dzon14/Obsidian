---
tags: [elenergi]
aliases: [synkronmaskinen, SM]
---
# Synkronmaskin
En elektrisk maskin för växelspänning. Dess rotor roterar synkront med växelspänningen i nätet, därmed namnet.

## Generisk synkronmaskin - induktion
- Två ledare bildar en lindning som roterar i B-fältet:
![[Pasted image 20230117084031.png|600]]
- I ledarna längs rotationsaxeln induceras $e_{1}$ respektive $e_{2}$
- Ena ledaren motsatt riktad + rör sig motsatt $\Rightarrow e_{1}= e_{2}, \ e=2e_{1}$
- När en ledarslinga roteras i ett magnetfält B induceras e som är noll två gånger per varv. 
- Ledarens periferihastighet är $v_{periferi} = \omega r$ och skär fältet med vertikala komponenten av $v_{pereferi}$ så $v=v_{periferi}sin \theta = \omega r sin \theta$
- I ena ledaren induceras $e_{1}=Bvl = Bl \omega r sin \theta$. $e=2e_{1}$ och $\theta=\omega t$.
- $\Rightarrow$ När en ledarslinga roteras med vinkelhastighet $\omega$ i ett magnetfält $B$ induceras $e=Bl \omega r sin \theta = \hat{e}sin \omega t$.
![[Pasted image 20230117085448.png|300]]

## Kraft
![[Pasted image 20230117084456.png|650]]
- På axiell ledare verkar $F = Bil$ oberoende av slingans läge ($i=i_{DC}$)
- Hävarm vinkelrätt mot F gånger F ger vridmoment
		- Maximalt när ledare står mitt för polerna
		- Noll när ledare står mitt emellan polerna.
- Hävarm $= rcos(\frac{\pi}{2}- \theta)=rsin \theta$
- Totalt vridmoment $T = 2Frsin \theta = 2Frsin \omega t$, vilket med $F=Bil \ (i=i_{DC})$ blir $\Rightarrow T =2Bilrsin \theta = 2Bilrsin \omega t$ 
		- Detta vridmoment är när ledarslingan har **likström**.

## Induktion och vridmoment
![[Pasted image 20230117092436.png|300]]
- Anslut en resistans $R_{L}$ som belastning
- När slingan roteras induceras e i slingan.
		- ger strömmen $i = \frac{e}{r_{L}}$ ($i=i_{AC}$)
		- ger ett vridmoment
- strömmen störst när slingan skär fältet mest.
- e störst vid polerna och noll mittemelllan. Samma gäller ström och vridmoment. 
- Vridmomentet är riktat **mot** rotationen.

- $e=2Bl \omega r Sin \omega t$, $u = e$
- Ger strömmen (i lasten) $i = \frac{2Bl \omega r sin (\omega t)}{R_{L}}$
- Strömmen och fältet ger vridmomentet$$T = 2Bil r sin \omega t = ... = (2Blr)^{2} \frac{\omega}{R_{L}} \frac{(1-cos2\omega t)}{2}$$

## Synkronmaskin och spänningskälla
- Synkronmaskinen beter sig som en växelspänningskälla $e(t) = \hat{e}sin \omega t$
- Anslut växelspänningskälla $u(t) = e(t)$
![[Pasted image 20230117085713.png|550]]
- i(t) blir noll, vridmoment blir noll. Kallas [[tomgång]] ($\omega \neq 0$).
- Växelspänningens frekvens bestäms av axelns varvtal
		- 3000 rpm $\Leftrightarrow$ 50 Hz

## Stillastående lindning
- I praktiken är lindningen still och magneten som skapar fältet roterar
- Definition: Lindning där emk induceras   = eng. armature winding, sv. ankarlindning och anges med index a

## Tvåfasig synkronmaskin
![[Pasted image 20230117092626.png|200]]
- Den horisontella lindningen ovan ger ett pulserande vridmoment T
		- $T_{H}$ ungefär proportionellt mot $sin^{2}\omega t$.
- Inför en vertikal lindning; förskjuten $90 \degree$
		- $T_{V}$ ungeför proportionell tmot $cos^{2} \omega t$
- På axeln verkar summan = 1 (trigetta) som är konstant.

## Trefasig synkronmaskin - spänningar
- Tre lindningar riktade 0, 120, 240$\degree$
- Tre sinusspänningar fasförskjutna 0, -120, -240$\degree$
- Sex gånger per varv induceras max $\lvert e \rvert$.
 ![[Pasted image 20230117093001.png|600]]

## Synkronmaskinens vektordiagram
![[Pasted image 20230118143115.png|500]]
Då de tre vektorerna summeras fås en den totala inducerade spänningen i form av en vektor vilken ligger 90° efter flödesvektorn. Om samma vektoraddition göres i varje godtyckligt rotorläge finner man att den resulterande inducerade spänningen alltid är lika stor och alltid ligger 90° efter en tänkt rotorflödesvektor.

## Trefasig synkronmaskin - moment
$$T_{fas} \text{ kurvform } \propto isin \omega t \propto sin^{2}(\omega t) \propto 1-cos2 \omega t$$
- Strömmar och moment i de tre faserna förskjutna $\pm 120 \degree$
- Varje lindning bidrar till vridmomentet $$T(t) = T_{a}(t) +T_{b}(t) + T_{c}(t)$$
- T(t) är konstant på samma sätt som för tvåfasig maskin

## Tvåfas vs trefas
![[Pasted image 20230117093510.png]]
Används överallt. (Kollar man på ledningar så är det alltid 3 st).

## Synkringenerator - ekvivalent schema
![[Pasted image 20230117103634.png|200]]
- Strömmen ger ett eget roterande flöde $\vec{\Phi}_{ar}$ i fas med $\vec{I}_{a}$. Detta kallas **ankarreaktion**
- alla $\Phi$ inducerar $E$.
- Ankarreaktionen ser ut som ett spänningsfall över en reaktans $- \vec{E}_{ar} = jX_{ar}\vec{I}_{a}$.

## Lastvinkel
- Vinkeln mellan $\vec{E}_{m}$ och $\vec{E}_{i}$ kallas lastvinkel, betecknas $\delta$
- Vid [[tomgång]] är $\vec{E}_{m} = \vec{E}_{i}$ och $\delta=0$
- $\delta$ är samtidigt vinkel i rummet mellan två flöden och (fas)vinkel mellan två spänningar

## Synkronmaskin - tre driftfall
![[Pasted image 20230117095115.png]]
- Rotor med sitt $\Phi_{m}$ roterar synkront - har alltid samma $\omega$
- Tomgång är ett neutralläge där axeln inte uträttar arbete
- Om axeln drivs på av en momentkälla blir det generatordrift
- Om axeln bromsas blir det motordrift