---
tags: [matstat]
---
# Linjärkombination

## Matstat - [[stokastisk variabel|stokastiska variabler]]
![[Pasted image 20221114150122.png]]
![[Pasted image 20221114150139.png]]

## Linjärkombinationer av oberoende normalfördelade stokastiska variabler

#### Satser
**Sats 6.3:** Om $X \in N(\mu, \sigma)$, så gäller att $$Y = aX +b \in N(a \mu + b, \lvert a \rvert \sigma)$$

**Sats 6.4:** Om $X \in N(\mu_{X}, \sigma_{X})$, $Y \in N(\mu_{Y},\sigma_{Y})$, där X och Y är oberoende, så gäller att $$\begin{align} &X + Y \in N \left( \mu_{X} + \mu_{Y},\  \sqrt{\sigma_{X}^{2}+ \sigma_{Y}^{2}} \right), \\ &X-Y \in N \left( \mu_{X}- \mu_{Y}, \ \sqrt{\sigma_{X}^{2} + \sigma_{Y}^{2}}\right) \end{align}$$
**Sats 6.5:** Om $X_{1}, X_{2}, ..., X_{n}$ är oberoende och respektive $N(\mu_{1}, \sigma_{1}),...,N(\mu_{n}, \sigma_{n})$ och talen $a_{1},a_{2},...,a_{n}$ och $b$ är givna, så gäller att $$\sum\limits_{1}^{n}a_{i}X_{i} + b \in N\left( \sum\limits_{1}^{n}a_{i}\mu_{i}+b \sqrt{\sum\limits_{1}^{n}a_{i}^{2}\sigma_{i}^{2}} \right)$$
**Följdsats 6.5.1:** Om $X_{1}, X_{2},...,X_{n}$ är oberoende $N(\mu,\sigma)$ och $\bar{X} = \sum\limits_{1}^{n}\frac{X_{i}}{n}$ är deras aritmetiska medelvärde, så gäller att $$\bar{X} \in N \left(\mu, \frac{\sigma}{\sqrt{n}} \right)$$
**Följdsats 6.5.2:** Om $X_{1},X_{2},...,X_{n1}$ är $N(\mu_{1}, \sigma_{1})$ och $Y_{1},Y_{2},...,Y_{n2}$ är $N(\mu_{2}, \sigma_{2})$ och alla variabler är oberoende, så gäller att $$\bar{X}-\bar{Y} \in \left( 
\mu_{1}-\mu_{2}, \sqrt{\frac{\sigma_{1}^{2}}{n_{1}}+ \frac{\sigma_{2}^{2}}{n_{2}}} \right)$$
**Sats 6.6:** Om $X_{1},X_{2},...,X_{f}$ är oberoende och $N(0,1)$, så gäller att $$\sum\limits_{i=1}^{f}X_{i}^{2} \in \chi^{2}(f)$$
#### Definitioner
**Def 6.1:** Om den [[stokastisk variabel|s.v]]. X har [[täthetsfunktion|täthetsfunktionen]] $$f_{X}(x) = \begin{cases} \frac{x^{\frac{f}{2}-1}e^{\frac{-x}{2}}}{\Gamma(\frac{f}{2})2^{\frac{f}{2}}}, \ \ \ \ \text{ om } X > 0 \\ 0, \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \text{ om } x \leq 0 \end{cases}$$säges $X$ vara $\chi^{2}$-fördelad med f [[Frihetsgrader]].