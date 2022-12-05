---
tags: [matstat]
---
# Hypotesprövning 

## Generell metod
Vi har ett slumpmässigt stickprov från en fördelning (eller flera stickprov från flera fördelningar). Vi har en nollhypotes $H_0$ som ska prövas. (Nollhypotes - specificerar hur fördelningen ser ut). 
- Om $H_{0}$ omfattar ett enda värde på $\theta$ kallas hypotesen **enkel**. Annars **sammansatt**.

För att pröva $H_{0}$ hittar vi en lämplig *testvariabel* eller *teststorhet* $t= t_{obs} = t(x)$. Testvariablen ($t_{obs}$) är en observatiom av en stickprovsvariabel $t(X)$. Vi anger även ett *kritiskt område* C (en del av området som t varierar över). 
	Signifikanstest: $$\begin{align} \text{Om }\  &t_{obs} \in C \ \text{ förkasta } H_{0} \\ &t_{obs} \notin  C \ \text{ förkasta ej } \ H_{0} \end{align}$$Vi avpassar $C$ så att $$P(t(X) \in C) = \alpha \ \ \text{ om } H_{0} \text{ sann }$$
där $\alpha$ är testets *signifikansnivå* (alt. felrisk). $\alpha$ bör vara liten. 
I det övre fallet är resultatet signifikant. I det undre icke-signifikant. 

**Exempel:** Man ser ett djur och ställer upp hypotesen $H_{0}$: Djuret är en häst. Som testvariabel tas $t =$ antalet ben och som kritiskt området $C = \{ 0,1,2,3,5,6,... \}$. Testet blir: Om $t \leq 3$ eller $t \geq 5$ förkasta $H_{0}$, om $t = 4$ förkasta icke $H_{0}$.

## [[styrkefunktionen]]

## Samband mellan hypotesprövning och [[intervallskattning]]

Visas i följande exempel
![[Pasted image 20221129162905.png|650]]

När hypotesprövning utförs enligt detta kallas det för *konfidensmetoden*. 

## Tillämpning på [[normalfördelning|normalfördelningen]]
Istället för att bestämma [[intervallskattning|konfidensintervall]] för [[väntevärden|väntevärdet]] $\mu$, [[standardavvikelse|standardavvikelsen]] $\sigma$ så kan man pröva olika hypoteser röranda den okända parametern. 

Två olika situationer:
1) 
![[Pasted image 20221129163451.png|500]]
![[Pasted image 20221129163502.png|500]]

2) 
   ![[Pasted image 20221129163742.png|600]]

## Användning av normalapproximationen
Tidigare diskussion om användning av normalapproximationen vid [[intervallskattning]] kan nu överföras till hypotesprövning.

Man tar en testavariabel av formen $(\theta^{*} - \theta_{0})/D$ eller, om D inte är helt känt, $(\theta^{*} - \theta_{0})/d$ och kan, om kvoten ifråga kan antas ungefär [[normalfördelning|normalfördelad]], utföra ett test på samma sätt som för intervallskattning. Skillnaden är att *signifikansnivån* nu inte kan bestämmas exakt
![[Pasted image 20221205183626.png|650]]

## Tillämpning på [[binomialfördelning|binomialfördelningen]]
Vi visar detta genom exemplen nedan:
![[Pasted image 20221205190148.png|650]]
![[Pasted image 20221205190253.png|650]]

Nollhypotesen antas $H_{0} : p_{1} = p_{2}
Antag att $H_{0}$ är sann och kalla det gemensamma värdet $p_{1}=p_{2}$ för $p$. Man inser att en skattning av $p$ ges av $$p_{obs}^{*} = \frac{(x_{1} + x_{2})}{(n_{1} + n_{2})}$$([[Maximum-likelihood-metoden|ML-skattningen]]). Med samma beteckningar som för intervallskattning för binomialfördelning, så får vi, om $H_{0}$ är sann, $$D = \sqrt{\frac{pq}{n_{1}}+\frac{pq}{n_{2}}} = \sqrt{pq \left( \frac{1}{n_{1}}+\frac{1}{n_{2}} \right)}$$Som medelfel tar vi $$d = \sqrt{p_{obs}^{*}(1-p_{obs}^{*})\left( \frac{1}{n_{1}} + \frac{1}{n_{2}} \right)}$$och bildar sedan kvoten $$u = \frac{(p_{1})_{obs}^{*} - (p_{2})_{obs}^{*}}{d}$$Därmed är det approximativa testet klart. 
**Exempel:**
![[Pasted image 20221205191802.png|600]]

