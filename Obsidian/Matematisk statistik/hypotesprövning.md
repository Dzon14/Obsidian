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

2) ![[Pasted image 20221129163742.png|600]]
