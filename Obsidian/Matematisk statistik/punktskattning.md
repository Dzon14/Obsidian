---
tags: [matstat]
---
# Punktskattning
Välkänd från det dagliga livet, att t.ex se en person och skatta åldern med ledning av utseendet. Eller att mäta längden av en sträcka och få en skattning av dess verkliga längd. 

## Allmänt om punktskattningar
En parameter $\theta$ kan ta värden i ett parameterrum $\theta_\Theta$ (t.ex $\theta_{\Theta} = (0,\infty$)) om vi vet att $\theta > 0$
![[Pasted image 20221125140406.png|550]]

$\theta^{*}_{obs}$ där obs står för att värdet beräknats ur mätdata (observationerna).
- För $\theta^{*}$ och $\hat{\theta}$, blir motsvarande stickprovsvariabler med obs i subindex. 
- Punktskattningar ändrar sig om ett nytt stickprov insamlas. 

#### Definitioner
**11.1:** En punktskattning $\theta^{*}_{obs} = \theta^{*}(x_{1},x_{1},...,x_{n})$ av en parameter $\theta$ är en funktion av mätdata $x_{1},...,x_{n}$. Dessa mätdata ses som utfall avv [[stokastisk variabel|stokastiska variabler]] $X_{1},X_{2},...,X_{n}$ vilkas fördelning beror av parameter $\theta$. Punktskattningen $\theta^{*}_{obs}$ är ett utfall av stickprovsvariabeln $\theta^{*}=\theta^{*}(X_{1},X_{2},...,X_{n})$.

**11.2:** en punktskattning $\theta^{*}_{obs}$ säges vara en [[väntevärden|väntevärde]]s riktig om tillhörande stickprovsvariabel $\theta^{*}$ har väntevärdet $\theta$, dvs om $$E(\theta^{*})=0$$för varje $\theta \in \Omega_{\Theta}$.

**11.3:** Om för varje fixt $\theta \in \Omega_{\Theta}$ och för varje givet $\varepsilon > 0$ $$P(\lvert \theta^{*}_{n} - \theta \rvert > \varepsilon) \rightarrow 0$$då stickprovsstorleken $n \rightarrow \infty$, säges $\theta^{*}_{obs}$ vara **konsistent**.

**11.4:** Medelkvadratfelet MSE för en punktskattning $\theta^{*}_{obs}$ är $$MSE = E((\theta^{*}-\theta)^{2}),$$där $\theta^{*}$ är motsvarande stickprovsvariabel
- anm: $$MSE = E((\theta^{*}-\theta)^{2}) = V(\theta^{*})+(E(\theta^{*})-\theta)^{2}$$där den sista termen kallas för systematiskt fel (bias).

**11.5:** Om två skattningar $\theta^{*}_{obs}$ och $\hat{\theta}_{obs}$ är vändevärdesriktiga och motsvartade stickprovsvariabler uppfyller $$V(\theta^{*}) \leq V(\hat{\theta})$$för alla $\theta \in \Omega_\Theta$ så är $\theta^{*}_{obs}$ **effektivare** än $\hat{\theta}_{obs}$.
- En väntevärdesriktig skattning med mindre [[betingade variansen|varians]] är bättre.

**11.9:** En skattning av $D(\theta^{*})$ kallas **medelfelet** för $\theta^{*}$ och betecknas $d(\theta^{*})$.
- Där $D(\theta^{*})$ är [[standardavvikelse|standardavvikelsen]]

#### Exemplen
![[Pasted image 20221125143610.png|500]]
![[Pasted image 20221125143647.png|500]]

## Tillämpning på [[normalfördelning|normalfördelningen]]

1) Ett stickprov 
[[Maximum-likelihood-metoden|ML-skattningen]] blir:$$s^{2}= \frac{1}{n-1}\sum\limits_{i=1}^{n}(x_{i}-\bar{x})^{2}$$
2) Två stickprov
[[Maximum-likelihood-metoden|ML-skattningen]] blir$$s^{2} = \frac{\sum\limits_{i=1}^{n_{1}}(x_{i}-\bar{x})^{2}+\sum\limits_{i=1}^{n_{2}}(y_{i}-\bar{y})^{2}}{(n_{1}-1)+(n_{2}-1)}$$

3) Flera stickprov 
[[Maximum-likelihood-metoden|ML-skattningen]] blir $$\frac{Q_{1}+...+Q_{k}}{(n_{1}-1)+...+(n_{k}-1)}$$där $Q_{1}$ är kvadratsumman kring stickprovsmedelvärdet för det i:te stickprovet, dvs $$Q_{i}= \sum\limits_{j=1}^{n_{i}}(x_{ij}-\bar{x_{i}})^{2}$$där $\bar{x}_{i} = \sum\limits_{j=1}^{n_{i}}\frac{x_{ij}}{n_{i}}$
##### Exempel på flera stickprov
![[Pasted image 20221125153435.png]]

## Tillämpning på [[binomialfördelning]] och dess släktingar

1) binomialfördelningen
![[Pasted image 20221125153543.png]]
![[Pasted image 20221125153552.png]]

2) **Hypergeometriska fördelningen**
![[Pasted image 20221125153628.png]]

3) [[Poisson-fördelning]]
![[Pasted image 20221125153655.png]]
