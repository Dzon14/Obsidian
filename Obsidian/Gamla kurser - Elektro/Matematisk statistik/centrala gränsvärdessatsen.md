---
tags: [matstat]
---
# Centrala gränsvärdessatsen
Visar bl.a betydelsen för [[normalfördelning]], där summan av ett stort antal [[oberoende stokastiska variabler]] är approximativt [[normalfördelning|normalfördelad]] under vissa förutsättningar.  

# Ekonomi
$\hat{p}$ är approximativt normalfördelad, $\bar{x}$ är approximativt normalfördelad.

## Exempel med urvalsandel
![[Pasted image 20231025152450.png]]
Vi behöver veta vilken [[sannolikhetsfördelningar|sannolikhetsfördelning]] slumpvariabeln $\hat{p}$ har.
![[Pasted image 20231025153048.png]]

## Urvalsmetoden är normalfördelad (Def.)
**Centrala gänrsvärdessatsen medför att:**
Urvalsandelen $\hat{p}$ är normalfördelad med väntevärde $p$ och standardavvikelse $\sqrt{\frac{pq}{n}}$ om dessa förutsättningar är uppfyllda:
![[Pasted image 20231025153922.png|500]]

**Cetnrala gränsvärdessatsen medför att:**
![[Pasted image 20231025154327.png|600]]
# MatStat
## Satser
**Sats 6.8:** Om $X_{1},X_{2},...$ är en oändligt följd av oneroende likafördelade [[stokastisk variabel|s.v]]. med [[väntevärden|väntevärdet]] $\mu$ och [[standardavvikelse|standardavvikelsen]] $\sigma > 0$, så gäller för $Y_{n} = X_{1}+...+X_{n}$ att $$P \left( a < \frac{Y_{n}-n \mu}{\sigma \sqrt{n}} \leq b \right) \rightarrow \Phi(b) - \Phi(a) \ \ \ \ \text{ då } n \rightarrow \infty$$
**Följdsats 6.8.1:** Om $X_{1},X_{2},...$ är en följd av oberoende likafördelade [[stokastisk variabel|s.v]]. med väntevärdet $\mu$ och standardavvikelsen $\sigma > 0$ så gäller att $\frac{X_{1}+...+X_{n}}{n} \in AsN(\mu, \frac{\sigma}{\sqrt{n}})$.


## Definitioner
**Def 6.2:** Om $Z_{n}, \ \ n=1,2,...,$ är en oändlig följd av s.v. och man kan finna tal $A_{n}$ och $B_{n},$ $n=1,2,...,$ sådana att $$P \left(a < \frac{Z_{n}- A_{n}}{B_{n}} \leq b \right) \rightarrow \Phi(b) - \Phi(a) \ \ \ \ \text{ då } n \rightarrow \infty$$säges $Z_{n}$ vara **asymptotiska normalfördelad** med parametrarna $A_{n}$ och $B_{n}$, eller kortare $$Z_{n} \in AsN(A_{n},B_{n})$$
## Exempel
![[Pasted image 20221117140553.png]]