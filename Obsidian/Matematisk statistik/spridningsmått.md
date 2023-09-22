---
tags: [matstat]
aliases: [spridningsmåttet, spridningsmåtten]
---
# Spridningsmått
Mäter hur utspridda observationerna är:
- Variationsbredd (Range)
- Kvartilavstånd (IQR)
- [[varians]]
- [[standardavvikelse]]


## Matstat
Det är inte alltid tillräckligt med att känna till [[lägesmått|lägesmåttet]]. T.ex kan en tvåpunktsfördelad [[stokastisk variabel|s.v]]. med olika värden och väntevärden få en olika utspridd fördelning.

## Definitioner
**Def 5.2:** [[varians]] $V(X)$ för en s.v. X med $\mu = E(X)$ är $$V(X) = E ((X-\mu)^{2})$$Variansen är alltså [[väntevärden|väntevärdet]] för den s.v. $Y=(X-\mu)^{2}$.

**Def 5.3:** [[standardavvikelse|standardavvikelsen]] $D(X)$ för en s.v. X är kvadratroten ur variansen $$D(X) = \sqrt{V(X)}$$
**Def 5.4:** Kvoten $$R(X) = \frac{D(X)}{E(X)}$$kallas **varianskoefficienten**.

**Def 5.5:** Om X är en [[stokastisk variabel|s.v]]. med [[väntevärden|väntevärdet]] $\mu$ och [[standardavvikelse|standardavvikelsen]] $\sigma$, kallas $Y = \frac{(X- \mu)}{\sigma}$ en **standardiserad** s.v.

**Def 5.6:** Med *systematiskt* fel menas differensen mellan mätvärdets väntevärde och det korrekta värdet. Med *slumpmässigt* fel menas differensen mellan mätvärdet och dess [[väntevärden|väntevärde]].

## Satser
**Sats 5.6:** $$V(X) = E(X^{2})-(E(X))^{2}$$
**Sats 5.7:** Vid linjärtransformation gäller: $$\begin{align}  &E(aX+b) = aE(X)+b, \\ &V(aX +b) = a^{2}V(X), \\ &D(aX+b) = \lvert a \rvert D(X) \end{align}$$