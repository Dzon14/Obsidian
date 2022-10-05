---
aliases: [kalman filtering]
---
# Kalmanfiltrering
- [[State Feedback|tillståndsåterkoppling]] från F9 byggde på att vi kunde mäta samtliga tillstånd, vilket man normalt **inte** kan.
- Kalmanfiltret är en metod för att filtrera fram en skattning av tillståndsvektorn ur styrsignalen och mätsignalen.
- När systemet är [[Observerbarhet]] går det att skatta tillståndsvektorn genom att studera insignalen u och utsignalen y. 
- Kalmanfiltrering görs i två steg.

### Försök 1: Tillståndsskattning genom simulering (ej kalman)
**Innan kalman**
Simulera processen $$\dot{\hat{x}} = A \hat{x} + Bu$$
där $\hat{x}$ är skattningen av tillståndvsvektorn $x$. 
Skattningsfelet: $$\tilde x = x - \hat{x}$$
Derivatan av skattningsfelet blir $$\dot{\hat{x}} = \dot{x}- \dot{\hat{x}} = Ax + Bu - A \hat{x} - Bu = A \tilde x$$
- Om matrisen A har samtliga egenvärden i vänstra halvplanet, dvs om processen är asymptotiskt [[Stabilitet|stabil]], kommer skattningsfelet gå mot 0. 
- Hastigheten bestäms av egenvärdenas läge.

### Försök 2: Kalmanfilter
Skatta tillståndsvektorn enligt $$\begin{cases} \dot{\hat{x}} = A \hat{x} + Bu + K(y- \hat{y}) \\ \hat{y} = C \hat{x}\end{cases}$$ Slår vi ihop dessa ekv. får vi $$ \begin{align}  \dot{\hat{x}} = A \hat{x} + Bu + KC(x- \hat{x}) \end{align}$$
Rekonstruktionsfelet: $$\dot{\hat{x}} = Ax + Bu - A \hat{x} - Bu - KC(x - \hat{x})= (A-KC) \tilde x$$
**Slutligen:**
Vi kan själva välja hur snabbt felet $\tilde x$ avtar, genom att välja K så att egenvärdena till $(A-KC)$ placeras lämpligt. 

Kalmanfiltret kan även skrivas $$\dot{\hat{x}} = (A-KC) \hat{x} + Bu + Ky$$

#regler