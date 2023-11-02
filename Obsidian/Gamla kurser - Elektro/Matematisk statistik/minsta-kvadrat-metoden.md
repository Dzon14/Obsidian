---
tags: [matstat]
aliases: [MK-metoden]
---
# Minsta-kvadrat-metoden
## Dataanalys (ekonomi)
Härleder formlerna för [[enkel linjär regression]]

#### Hur fick vi fram formlerna för $b_{0}$ och $b_{1}$
![[Pasted image 20231001182322.png|500]]


## MatStat

$$Q(\theta) = \sum\limits_{i=1}^{n}(x_{i}-\mu_{i}(\theta))^{2}$$där $x_{1}...$ är utfall av [[oberoende stokastiska variabler]] $X_{1}...$ vars [[väntevärden]] är kända. Vi antar $E(X_{i})=\mu_{i}(\theta)$ där $\mu_{1}...$ är kända funktioner och $\theta$ okänd parameter i parameterrummet.

## Definition 11.8
Det värde $\theta^{*}_{obs}$, för vilket $Q(\theta)$ antar sitt minsta värde inom $\Omega_{\Theta}$, kallas MK-skattningen av $\theta$. 

## MK-metoden kan generaliseras:

1) fördelningen innehåller k okända parametrar $\theta_{1}, ..., \theta_{k}$.
   Uttrycket Q blir då en funktion av dessa parametrar, och man bestämmer en skattning för var och en så att Q blir så litet som möjligt. 
2) Värdena $x_{1},...,x_{n}$ är observationer av[[stokastisk variabel|s.v]]. $X_{1},...,X_{n}$ med olika fördelningar som beror av samma okända parameter eller parametrar. 
![[Pasted image 20221125151916.png]]

## Exemplen
![[Pasted image 20221125151532.png|550]]

