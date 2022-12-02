---
tags: [matstat]
---
# Centrala gränsvärdessatsen
Visar bl.a betydelsen för [[normalfördelning]], där summan av ett stort antal [[oberoende stokastiska variabler]] är approximativt [[normalfördelning|normalfördelad]] under vissa förutsättningar.  

## Satser
**Sats 6.8:** Om $X_{1},X_{2},...$ är en oändligt följd av oneroende likafördelade [[stokastisk variabel|s.v]]. med [[väntevärden|väntevärdet]] $\mu$ och [[standardavvikelse|standardavvikelsen]] $\sigma > 0$, så gäller för $Y_{n} = X_{1}+...+X_{n}$ att $$P \left( a < \frac{Y_{n}-n \mu}{\sigma \sqrt{n}} \leq b \right) \rightarrow \Phi(b) - \Phi(a) \ \ \ \ \text{ då } n \rightarrow \infty$$
**Följdsats 6.8.1:** Om $X_{1},X_{2},...$ är en följd av oberoende likafördelade [[stokastisk variabel|s.v]]. med väntevärdet $\mu$ och standardavvikelsen $\sigma > 0$ så gäller att $\frac{X_{1}+...+X_{n}}{n} \in AsN(\mu, \frac{\sigma}{\sqrt{n}})$.


## Definitioner
**Def 6.2:** Om $Z_{n}, \ \ n=1,2,...,$ är en oändlig följd av s.v. och man kan finna tal $A_{n}$ och $B_{n},$ $n=1,2,...,$ sådana att $$P \left(a < \frac{Z_{n}- A_{n}}{B_{n}} \leq b \right) \rightarrow \Phi(b) - \Phi(a) \ \ \ \ \text{ då } n \rightarrow \infty$$säges $Z_{n}$ vara **asymptotiska normalfördelad** med parametrarna $A_{n}$ och $B_{n}$, eller kortare $$Z_{n} \in AsN(A_{n},B_{n})$$
## Exempel
![[Pasted image 20221117140553.png]]