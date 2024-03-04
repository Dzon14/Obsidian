---
tags:
  - datastat
---
# Villkor för DatStat

## Centrala gränsvärdessatsen (approx. normalfördelad)
- Oberoende observationer
	- Motiveras genom att vi gör ett slumpmässigt urval och att urvalet är högst 10% av populationen.
- Tillräckligt stort urval
	- Tumregel: $n \hat{p} \geq 10$ och $n \hat{q} \geq 10$
OBS: För ett urvalsmedelvärde är tumregeln att $n \geq 30$, om datan kommer från en normalfördelning kan vi dock strunta i detta. 

## Hypotesprövning för en andel
(One sample z-test)
Antar att samma gäller för konfidensintervall?
- Oberoende observationer
- Tillräckligt stort urval ($np_0 \geq 10$ och $nq_0 \geq 10$)

## Hypotesprövning för ett medelvärde
(One sample t-test)
Antar att samma gäller för konfidensintervall?
- Oberoende observationer (en indikator kan vara slumpvis urval)
- Tillräckligt stort urval (n $\geq 30$) **eller** normalfördelade data (motiveras med histogram och normalfördelningsplott)

## Hypotesprövning och konfidensintervall för två andelar
(Hypotesprövning - two sample z-test)
- Oberoende observationer
- Tillräckligt stora urval (samma som för en andel)
	- (Urvalet är högst 10% av populationen)

## Hypotesprövning och konfidensintervall för två medelvärden
(Hypotesprövning - two sample t-test)
- Oberoende observationer
- $n_{1}$ och $n_{2} \geq 30$ **eller** normalfördelade data
Kontroll:
- Slumpvis?
- Rita histogram och normalfördelningsplottar

## Parvis beroende data - konfidensintervall och hypotesprövning (paired t-interval and t-test)
1. Parvis beroende data
2. Oberoende differenser
3. Antingen n $\geq$ 30 **eller** normalfördelade differenser
##### Kontrollera villkoren exempel
![[Pasted image 20240220101349.png|550]]
![[Pasted image 20240220101950.png|500]]

## Test av fördelningsantagande (goodness-of-fit test), Homogenitetstest & Test av Oberoende
(Chi2-tester)
1. Data är antal
2. Oberoende observationer
3. Tillräckligt stort urval (tumregel: alla Exp $\geq$ 5)

## Enkel linjär regression
1. Linjärt samband mellan $x$ och $y$. (Dvs. vi vill varken ha icke-linjärt samband eller outlier)
2. Oberoende residualer
3. Jämn residualspridning (homoskedasticitet)
4. Normalfördelade residualer
	- Kontroll: Rita histogram och normalfördelningsplott för residualerna. Histogrammet ska vara symmetriskt och unimodalt, punkterna i normalfördelningsplotten ska följa en rät linje.
1-3 kan kontrolleras på två olika sätt:
- Rita spridningsdiagram för X och Y. Kolla att punkterna följer en rät linje och att vi inte har outliers. Kolla ocksa att molnet av punkter är någorlunda jämntjockt i vertikal led.
- Rita residualplottar för e och $\hat{y}$ eller för e och x. Kolla att det inte finns ett icke-linjärt samband och att det inte finns outliers. Vi vill se en stjärnhimmel. Kolla också att molnet av punkter ar någorlunda jämntjockt i vertikal led.
Exempel på residualplottar:
![[Pasted image 20240220113949.png|400]]
- Villkor för konfidensintervall för lutningen $\beta_{1}$ är densamma som för regression.
- Villkor för Hypotesprövning för lutningen $\beta_{1}$ är densamma som för regression.
- Villkor för konfidensintervall för medelvärdet $\mu_{y}$ är densamma som för regression.
- Villkor för prediktionsintervall för skattningen $\hat{y}$ är densamma som för regression.

# Typ-fel och styrka
- Typ I-fel (false positive)
- Typ II-fel (false negative)
- Styrkan för ett statistiskt test
- Effektstorlek

## Typ-fel
![[Pasted image 20231128154744.png|500]]
#### Exempel
![[Pasted image 20231128154825.png|550]]

## Styrka
![[Pasted image 20231128154845.png|550]]
![[Pasted image 20231128155026.png|550]]

## Effektstorlek och styrka
![[Pasted image 20231128155045.png|600]]
![[Pasted image 20231128155053.png|600]]