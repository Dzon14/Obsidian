---
tags: [matstat]
aliases: [väntevärdet, väntevärdena, väntevärde]
---
# Väntevärden

## Definition 
Väntevärden för den [[stokastisk variabel|s.v]]. $X$ definieras av $$E(X) = \begin{cases} \sum\limits_{k}^{}kp_{X}(k) \ \ \ \ \text{ (diskret s.v.)} \\ \int\limits_{-\infty}^{\infty} xf_{X}(x) \ dx \ \ \ \ \text{ (kontinuerlig s.v.)} \end{cases}$$Alternativ term: förväntat värde. E för "Expectation". Istället för E kan även $\mu$ eller $\mu_{X}$ användas.

#### Exempel
![[Pasted image 20221109103125.png]]

## Väntevärde för en funktion av [[stokastisk variabel|s.v]]
**Sats:** 
Om $Y=g(X)$ gäller att $$E(Y) = \begin{cases} \sum\limits_{k}^{}g(k)p_{X}(k) \ \ \ \ \text{ (diskret)} \\ \int\limits_{-\infty}^{\infty} g(x)f_{X}(x) \ dx \ \ \ \ \text{ (kontinuerligt)} \end{cases}$$Där $Y=g(X)$ är en funktion. 

#### Exempel
![[Pasted image 20221109103629.png]]

## Väntevärdet för [[flerdimensionell stokastiska variabel]]
**Sats 5.2:** Om $Z = g(X,Y)$ gäller att $$E(Z) = \begin{cases} \sum\limits_{j,k}^{}g(j,k)p_{X,Y}(j,k) \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \  \ \text{ (diskret)} \\ \int\limits_{-\infty}^{\infty} \int\limits_{-\infty}^{\infty} g(x,y)f_{X,Y}(x,y) \ dx \ dy \ \ \ \ \text{ (kontinuerlig)} \end{cases}$$
**Sats 5.3:** Om X och Y är [[stokastisk variabel|s.v]] med väntevärden $E(X)$ och $E(Y)$ och om a,b,c är konsanter gäller att $$E(aX + bY + c) = aE(X) + bE(Y) + c$$
**Sats 5.4:** Om X och Y är [[oberoende stokastiska variabler]] gäller att $$E(XY) = E(X)E(Y)$$
**Sats 5.5:** Om $X_{1},X_{2},...,X_{n}$ är oberoende s.v. gäller $$E(X_{1}X_{2}...X_{n}) = E(X_{1})E(X_{2})...E(X_{n})$$
