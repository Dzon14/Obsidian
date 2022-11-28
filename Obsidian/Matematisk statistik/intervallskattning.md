---
tags: [matstat]
aliases: [konfidensintervall]
---
# Intervallskattning
Oftast lämpligare än en [[punktskattning]].

## Allmänt
**Konfidensintervall:** Ett intervall $I_\theta$ som med sannolikheten $1-\alpha$ täcker över $\theta$. $1 - \alpha$ kallas för konfidensgraden. Intervallets vänstra och högra ändpunkter (konfidensgränser) betecknas allmänt $a_{1}(x)$ och $a_{2}(x)$. Funktioner av värdena i stickprovet. $$P(a_{1}(X) < \theta < a_{2}(X)) = 1- \alpha$$
"Vi använder en metod som med sannolikheten $1- \alpha$ leder till ettt korrekt påstående".
Ett konfidensintervall kan sägas vara en observation av ett intervall med stokastiska gränser. 
![[Pasted image 20221128154811.png]]

## Tillämpning på [[normalfördelning|normalfördelningen]]

1) Ett stickprov. Konfidensintervall för [[väntevärden|väntevärdet]]
**Sats 12.1:** Låt $x_{1},...,x_{n}$ vara ett slumpmässigt stickprov från N($\mu,\sigma$) där $\mu$ är okänt. Då är $$\begin{align} &I_{\mu} = \left(\bar{x}- \lambda_\frac{\alpha}{2 }D, \bar{x}+ \lambda_\frac{\alpha}{2}D\right) \ \ \ \ \text{ om }\sigma \text{ är känt }\left(D=\frac{\sigma}{\sqrt{n}}\right) \text{ samt } \\ &I_{\mu}= \left(\bar{x}- t_\frac{\alpha}{2}(f)d, \bar{x}+t_{\frac{\alpha}{2}}(f)d\right) \ \ \ \ \text{ om } \sigma \text{ är okänt }(d=\frac{s}{\sqrt{n}},f=n-1 )\end{align}$$ett tvåsidigt konfidensintervall för $\mu$ med konfidensgraden $1- \alpha$.

2) Ett stickprov. Konfidensintervall för standardavvikelsen
**Sats 12.2:** Låt $x_{1},...,x_{n}$ vara ett slumpmässigt stickprov från $N(\mu, \sigma)$. Då är $$I_{\sigma}= (k_{1}s, k_{2}s)$$där $$k_{1} = \sqrt{\frac{f}{\mathcal{X^{2}_\frac{\alpha}{2}}}(f)} \ \ \ \ \text{ och } \ \ \ \ k_{2} = \sqrt{\frac{f}{\mathcal{X^{2}}_{1-\frac{\alpha}{2}}}} \ \ \ \ (f=n-1 )$$ett konfidensintervall för $\sigma$ med konfidensgraden $1-\alpha$.
Där $\left(\mathcal{X}^{2}(f) = \sum\limits_{i=1}^{f}X^{2}_{i}\right)$ 

3) Två stickprov. Konfidendsintervall för differens mellan [[väntevärden]]
**Sats 12.3:** Låt $x_{1},...,x_{n}$ och $y_{1},...,y_{n}$ vara slumpmässiga, av varandra oberoende stickprov från $N(\mu_{1},\sigma_{1})$ respektive $N(\mu_{2}, \sigma_{2})$
Om $\sigma_{1}$ och $\sigma_{2}$ är kända så är $$I_{\mu_{1}-\mu_{2}}= \left(\bar{x} - \bar{y} - \lambda_{\frac{\alpha}{2}}D,\bar{x}-y + \lambda_\frac{\lambda}{2}D\right)$$ett tvåsidigt konfidensintervall för $\mu_{1}- \mu_{2}$ med konfidensgraden $1-\alpha$; här är $D = \sqrt{\frac{\sigma^{2}_{1}}{n_{1}}+ \frac{\sigma_{2}^{2}}{n_{2}}}$. 
Om $\sigma_{1}= \sigma_{2} = \sigma$ där $\sigma$ är okänt så är $$I_{\mu_{1}-\mu_{2}}= \left(\bar{x}-\bar{y}-t_\frac{\alpha}{2}(f)d,\bar{x}-\bar{y}+t_\frac{\alpha}{2}(f)d\right)$$ett tvåsidigt konfidensintervall för $\mu_{1} - \mu_{2}$ med konfidensgraden $1- \alpha$; här är $d= s \sqrt{\frac{1}{n_{1}}+\frac{1}{n_{2}}}$ där $s = \sqrt{\frac{Q_{1}+ Q_{2}}{(n_{1}-1)+(n_{2}-1)}}$ medan $f=(n_{1}-1)+(n_{2}-1)$.

4) Stickprov i par.
Se boken s.301.


#### Exemplen (för tillämpning)
Ett stickprov:
![[Pasted image 20221128161645.png]]
Ett stickprov:
![[Pasted image 20221128162852.png]]
Två stickprov:
![[Pasted image 20221128164300.png]]

## Användning på normalapproximationen
I praktiken förekommer ofta fördelningar som inte alls liknar den normala. Dessa kan hanteras med ungefär samma teknik. 
Vi betraktar ett slumpmässigt stickprov. Fördelningen beror av en okänd parameter $\theta$. Antag att man hittat på en [[punktskattning]] $\theta^{*}$ som är ungefär [[normalfördelning|normalfördelad]] med [[väntevärden|väntevärdet]] $\theta$ och [[standardavvikelse|standardavvikelsen]] $D=D(\theta^{*})$. Då gäller att $$\frac{\theta^{*}-\theta}{D} \in N(0,1)$$
**Sats 12.4:** Antag att man på grundval av ett eller flera slumpmässiga stickprov har beräknat en punktskattning $\theta^{*}$ av en okänd parameter $\theta$. Antag vidare att denna skattning är ungefär normalfördelad med väntervärdet $\theta$ och standardavvikelsen $D$. Då är $$\begin{align} &I_{\theta } =\left(\theta^{*}_{obs}- \lambda_\frac{\alpha}{2}D,\theta_{obs}^{*}+ \lambda_\frac{\alpha}{2}D\right) \ \ \ \ \text{om D ej beror av }\theta \\ &I_{\theta} =\left(\theta_{obs}^{*}- \lambda_\frac{\alpha}{2}d, \theta_{obs}^{*} + \lambda_\frac{\alpha}{2}d\right) \ \ \ \ \text{ om D beror av } \theta \end{align}$$(och d väljs lämpligt) ett konfidensintervall för $\theta$ med den approximativa konfidensgraden $1- \alpha$.

**Följdsats 12.4.1:** Låt $x_{1},...,x_{n}$ vara ett stort slumpmässigt stickprov från en fördelning, där väntevärdet är $\mu$ och standardavvikelsen $\sigma$. Då är $$\begin{align} &I_{\mu} = \left(\bar{x}- \lambda_\frac{\alpha}{2}D,\bar{x}+ \lambda_\frac{\alpha}{2}D\right) \ \ \ \ \text{ om } \sigma \text{ känt } \left(D= \frac{\sigma}{\sqrt{n}} \right)\\ &I_{\mu}= \left(\bar{x}-\lambda_\frac{\alpha}{2}d, \bar{x}+ \lambda_\frac{\alpha}{2}d\right) \ \ \ \ \text{ om  } \sigma 
\text{ okänt } \left(d=\frac{s}{\sqrt{n}} \right) \end{align}$$
**Följdsats 12.4.2:** Låt $x_{1},...,x_{n1}$  och $y_{1},...,y_{n2}$ vara slumpmässiga och av varandra oberoende stickprov från fördelningar med väntevärdern $\mu_{1}$ respektive $\mu_{2}$ och standardavvikelserna $\sigma_{1}$ respektive $\sigma_{2}$.
Om $\sigma_{1}$ och $\sigma_{2}$ är kända så är $$I_{\mu_{1}-\mu_{2}}= \left(\bar{x}-\bar{y}-\lambda_\frac{\alpha}{2}D, \bar{x}-\bar{y}+ \lambda_\frac{\alpha}{2}D\right)$$ett tvåsidigt konfidensintervall för $mu_{1} - \mu_2$ med den approximativa konfidensgrade $1- \alpha$; här är $D = \sqrt{\frac{\sigma_{1}^{2}}{n_{1}}+\frac{\sigma_{2}^{2}}{n_{2}}}$.
Om $\sigma_{1}$ och $\sigma_{2}$ okända tar man istället $$I_{\mu_{1}-\mu_{2}}= \left(\bar{x }-\bar{y }- \lambda_\frac{\alpha}{2}d, \bar{x}-\bar{y}+ \lambda_\frac{\alpha}{2}d\right)$$där $$d = \sqrt{\frac{s_{1}^{2}}{n_{1}}+\frac{s_{2}^{2}}{n_{2}}}$$
De i satsen nämnda $s_{1}$ och $s_{2}$ är respektive stickprovs standardavvikelse. 

## Tillämpning på binomialfördelningen och dess släktingar

1) [[binomialfördelning]]
![[Pasted image 20221128171443.png]]

2) **Hypergeometriska fördelningen**
![[Pasted image 20221128171536.png]]

3) [[Poisson-fördelning]]
![[Pasted image 20221128171612.png|500]]