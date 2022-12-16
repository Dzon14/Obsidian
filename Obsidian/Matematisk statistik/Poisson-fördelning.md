---
tags: [matstat]
---
# Poisson-fördelningen
[[sannolikhetsfunktionen|sannolikhetsfunktion]]: $$p_{X}(k) = \frac{\mu^{k}}{k!}e^{-\mu}, \ \ k=0,1,2,...$$Med kodbeteckningen $X \in Po(\mu)$

## Förekomst
Uppträder då man studerar företeelse som inträffar slumpmässigt i tiden eller rummet. 

##### Exempel
![[Pasted image 20221121183207.png]]

- Poisson uppträder även som approximation till [[binomialfördelning|binomialfördelningen]] och hyoergeometriska fördelningen.

## Exakta egenskaper

**Sats 7.7:** Om $X$ är $Po(\mu)$ gäller att $$E(X) = \mu, \ \ V(X) = \mu, \ \ D(X) = \sqrt{\mu}$$Notera att [[betingade variansen]] är lika med [[väntevärden|väntevärdet]].

**Sats 7.8:** Om $X \in Po(\mu_{1})$ och $Y \in Po(\mu_{2})$, där $X$ och $Y$ är [[oberoende stokastiska variabler]], gäller att $X + Y \in Po(\mu_{1}+\mu_{2})$.

##### Exempel
![[Pasted image 20221121183838.png]]

## Approximativ egenskap 
Poisson-fördelningen är, eftersom den innehåller en enda parameter, lättare att hantera än [[binomialfördelning|binomialfördelningen]] och hypergeometriska fördelningen , och man har inte lika ofta behov av approximationer. Följande approximation är dock nyttig. För stora $\mu$ gäller ugefär att $X \in N(\mu,\sqrt{\mu})$.

**Exempel:**
![[Pasted image 20221121184141.png]]
