---
aliases: [conditional probability]
tags: [matstat]
---
# Betingad sannolikhet

# Ekonomi
Efter strecket skrivs det "jag vet".
![[Pasted image 20231002113139.png]]
![[Pasted image 20231002113155.png]]

Notera att vi kan skriva om denna formel till allmänna [[Multiplikationsprincipen]] genom att multiplicera upp P(B).
# MatStat
Vi vet redan att vi är i B och vill räkna ut [[Sannolikhet|sannolikheten]] att också hamna i A, så vi behöver vikta om alla [[Utfall]] så att vi får ett nytt [[Utfallsrum]], vilket vi gör genom att dela på [[Sannolikhet|sannolikheten]] att hamna i B.

Antag att vi kastar två tärningar, vad är [[Sannolikhet|sannolikheten]] att vi får en jämn summa **om** minst en är en 5:a. $$\Omega = \{(1,1), (1,2),...,(6,6)\}$$
där $\lvert \Omega \rvert = 36$.  $$\begin{align} B &= \{(1,5),(2,5),(3,5),(4,5),(5,6),(6,5),(5,6),(5,4),(5,3),(5,2),(5,1) \} \\ &= \{ (1,5),(3,5),(5,5),(5,3),(5,1) \}  \end{align}$$
där $\lvert B \rvert = 11$

Svar: $\frac{5}{11}$ 

**Def:**
$$\frac{P(A\cap B)}{P(B)} \equiv P(A|B)$$
Se även [[Bayes formel]]
## Egenskaper
$$\begin{align} P(B^*|A) = 1 - P(B|A) \\ P(B \cup C|A) = P(B|A) + P(C|A) - P(B \cap C|A) \end{align}$$ där C är någon händelse.


## Se också:
- [[lagen om total sannolikhet]]
- [[Bayes formel]]