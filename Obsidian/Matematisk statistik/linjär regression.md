---
tags: [matstat]
---
# Linjär regression 

## Modell för enkel linjär regression
![[Pasted image 20221206162710.png|650]]

Detta exempel är en enkel linjär regression och linjen $$y = \alpha + \beta x$$kallas den *teoretiska regressionslinjen*. Den visar hur [[väntevärden|väntevärdet]] beror av regressionsvariablen x. y kan ses som väntevärdet.
- $\beta$ anger hur mycket väntevärdet ökar, då x ökas med en enhet. Om $\beta$ är noll så är väntevärdet konstant. 
- Ju mindre $\sigma$ är desto bättre ansluter sig punkterna till linjen. (Kommer fråm observartioner från $N(0, \sigma$) - [[normalfördelning]].

Ofta använder man följande metod: $$ \mu_{i} = \alpha + \beta x_{i}$$ där $\mu_{i}$  är väntevärden och $x_{i}$ är givna storheter. 

## Punktskattningar
Regression med [[punktskattning|punktskattningar]].

Man kan skatta linjens läge genom att dra en rät linje genom de inprickade pinkterna. Om $\sigma$ är litet kan man då uppnå hyggliga resultat. 

Ännu bättre är att använda en numerisk metod, som [[minsta-kvadrat-metoden|MK-metoden]], för att bestämma punktskattningar av $\alpha$ och $\beta$. Då får vi följande $$\beta^{*} = \frac{S_{xy}}{S_{xx}} \ \  \text{ och } \ \ \alpha^{*} = \bar{y} - \beta^{*} \bar{x}$$där $S_{xy} = \sum\limits_{i=1}^{n}(x_{i}- \bar{x})(y_{i}- \bar{y})$ och $S_{xx}= \sum\limits_{i=1}^{n}(x_{i} - \bar{x})^{2}$.

$S_{xy}$ kan även skrivas som $$S_{xy} = \sum\limits_{i=1 }^{n}x_{i}y_{i} - n \bar{x}\bar{y}$$samma gäller $S_{xx}$.

Båda skattningarna är linjära uttryck. Vi har $$\beta^{*} = \sum\limits_{i=1 }^{n}c_{i}y_{i} \ \ \text{ och } \ \ \alpha^{*}= \sum\limits_{i=1}^{n}d_{i}y_{i}$$där $$c_{i}= \frac{(x_{i} - \bar{x})}{S_{xx}} \ \ \text{ och } \ \ d_{i} = \frac{1}{n} - c_{i}\bar{x}$$
Genom att sätta in dessa får vi den **skattade regressionslinjen** $$y = \alpha^{*} + \beta^{*}x$$och denna procedur kallas *skattning på väntevärde* (eller skattning av punkt på den teoretiska regressionslinjen). Detta är mycket betydelsefullt. 

För [[väntevärden|väntevärde]] och [[varians]] har vi även: $$\begin{align} &E(\beta^{*}) = \beta \\ &E(\mu_{0}^{*}) = \mu_{0} \\ &V(\beta^{*}) = \frac{\sigma^{2}}{S_{xx}} \\ &V(\mu_{0}^{*}) = \sigma^{2}\left( \frac{1}{n} + \frac{(x_{0} - \bar{x})^{2}}{S_{xx}}
 \right) \end{align}$$

Minimivärdet för $Q(\alpha, \beta)$ är $$Q_{0}= \sum\limits_{}^{}(y_{i} - \alpha^{*} - \beta^{*}x_{i})^{2}$$ och kallas **residualkvadratsumma**

Skattning av $\sigma$ är $$s = \sqrt{\frac{Q_{0}}{n-2}}$$

## Intervallskattningar
[[intervallskattning|intervallskattningar]] kompletterar punktskattningar. 
Om [[standardavvikelse|standardavvikelsen]] $\sigma$ är känd finner man konfidensintervallet $$\begin{align} &I_{\beta} = (\beta^{*} - \lambda_\frac{p}{2}D, \beta^{*} + \lambda_\frac{p}{2}D)  \ \  \text{ där } \ \  D = \frac{\sigma}{\sqrt{\sum\limits_{}^{}(x_{i} - \bar{x})}^{2}} \\ &I_{\mu_{0}} = \left(\mu_{0}^{*} - \lambda_\frac{p}{2}D, \mu_{0}^{*} + \lambda_\frac{p}{2}D\right)\ \ \text{ där } \ \ D = \frac{\sigma}{\sqrt{\frac{1}{n} + \frac{(x_{0}- \bar{x})^{2}}{S_{xx}}}} \end{align}$$med konfidensgraden $1-p$.
Skattning av $\sigma$ ges av $$s = \sqrt{\frac{Q_{0}}{n-2}}$$
##### Exempel
![[Pasted image 20221206172454.png|600]]

## [[multipel regression]]
