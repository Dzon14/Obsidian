---
tags:
  - datastat
---
# Multipel linjär regression

## Villkor för MLR
1. Linjärt samband mellan y och var och en av de förklarande variablerna. Vi vill varken ha icke-linjära samband eller outlier.
2. Oberoende [[residual|residualer]]
3. Jämn residualspridning (homoskedasticitet)
4. Normalfördelade [[residual|residualer]]

## Indikatorvariabel
Om man exempelvis vill undersöka Boarea (förklarande variabel x) mot slutpris (responsvariabel) med flera städer, blir den andra förklarande variabeln en indikatorbariabel. Den beskriver vilken stad det är, allts om Ind = 1 är det stad 1 och Ind = 0 är det stad 2.

Om man vill att modellen tar i hänsyn till fler än två kategorier, exempelvis vilken stadsdel lägenheten ligger i (med tre alternativ: Centrum, Norr och Söder), kan man införa en till indikatorvariabel. 
$Ind_{1}$ som är 1 för lägenheterna i Centrum och 0 för övriga
$Ind_{2}$ som är 1 för lägenheterna i Norr och 0 för de övriga. 

## Interaktionstermer
Om linjer (data) ej är parallella, som för kolhydrater vs kalorier för icke-vegetariskt och vegetariskt, duger inte endast en indikatorvariabel. 
![[Pasted image 20231002104346.png]]
![[Pasted image 20231002104445.png]]
![[Pasted image 20231002104603.png]]
![[Pasted image 20231002104647.png]]

## Motiv till regressionsanalys
![[Pasted image 20231002104956.png]]
