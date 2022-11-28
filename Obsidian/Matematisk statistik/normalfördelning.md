---
tags: [matstat]
aliases: [normalfördelat, normalfördelad, normalfördelningen]
---
# Normalfördelning
Används ofta för beskrivning av variationen hos olika företeelser. 
[[täthetsfunktion|täthetsfunktionen]]: $$f_{X}(x)= \frac{1}{\sigma \sqrt{2 \pi}}e^{-\frac{(x-\mu)^{2}}{2\sigma^{2}}}$$och [[fördelningsfunktion|fördelningsfunktionen]]: $$F_{X}(x) = \frac{1}{\sigma \sqrt{2 \pi}}\int\limits_{-\infty}^{x} e^{-\frac{(t-\mu)^{2}}{2\sigma^{2}}} \ dt$$
Vi erinrar kodbeteckningen $X \in N(\mu, \sigma)$.

## Standardiserad normalfördelning
Ett viktigt specialfall där $X \in N(0,1)$, alltså $\mu = 0$ och $\sigma = 1$.
Vi får då täthetsfunktionen: $$\varphi(x) = \frac{1}{\sqrt{2\pi}}e^\frac{-x^{2}}{2}$$och fördelningsfunktionen: $$\Phi(x) = \frac{1}{\sqrt{2\pi}} \int\limits_{-\infty}^{x} e^{\frac{-t^{2}}{2}} \ dt$$
och funktionerna ser ut enligt
![[Pasted image 20221115163507.png]]

- För en standardiserad normalfördelning gäller $$E(X) =0, \ \ \ \ D(X) = 1$$eftersom [[väntevärden|väntevärdet]] är 0 och [[standardavvikelse|standardavvikelsen]] är 1 så införs $N(0,1)$.

## Allmän normalfördelning
- $X \in N(\mu,\sigma)$
Täthetsfunktion och fördelningsfunktion ges enligt sats nedan.
**Sats 6.1:** $X \in N(\mu,\sigma)$ om och endast om $Y = \frac{X-\mu}{\sigma} \in N(0,1)$. Dessutom gäller att $$\begin{align} f_{X}(x) = \frac{1}{\sigma}\varphi \left(\frac{x-\mu}{\sigma}\right) \ \text{ och } \ F_{X}(x) = \Phi\left(\frac{x-\mu}{\sigma}\right) \end{align}$$
**Sats 6.2:** Om $X \in N(\mu, \sigma)$, så gäller att $$E(X) = \mu, \ \ \ V(X) = \sigma^{2}, \ \ \ D(X) = \sigma$$
**Utseende:**
![[Pasted image 20221115164720.png]]

## Lin