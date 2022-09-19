---
aliases: [output feedback]
---
# Utsignalåterkoppling
Koppling mellan [[State Feedback|tillståndsåterkoppling]] och [[Kalmanfiltrering]], så att tillståndsåterkopplingen sker från de skattade tillstånden istället för de verkliga. 

(Vi väljer att inte ha med integraltermen nedan)
![[Pasted image 20220919153404.png|600]]

Processen beskrivs på tillståndsformen
$$ \begin{cases}  \dot{x} = Ax + Bu \\ y = Cx \end{cases}$$
Regulatorn blir nu en kombination av [[Kalmanfiltrering]] och [[State Feedback|tillståndsåterkoppling]] enligt $$\begin{cases}  \dot{\hat{x}} = A \hat{x} +Bu + L(y-\hat{y}) \\ \hat{y} = C \hat{x} \\ u = k_{r}r - K \hat{x}\end{cases}$$
Vid undersökning av det slutna systemet, så börjar vi med tillståndsbeskrivning. 
Välj tillståndsvektorn $$x_{e}= \begin{pmatrix} x \\ \tilde{x}=x- \hat{x} \end{pmatrix}$$
Tillståndsekvationer blir $$\dot{x} = Ax + Bu = Ax - BK \hat{x} + Bl_{r}\cdot r = ... = (A-BK)x + BK \tilde{x} + Bk_{r} \cdot r$$
och vi får $$\dot{\tilde{x}} = \dot{x}- \dot{\hat{x}} = Ax + Bu - A \hat{x}- Bu - KC(x-\hat{x}) = (A-KC)\tilde{x}$$
Vi vill dock ha detta på matrisform och får då $$\begin{align} \begin{pmatrix} \dot{x} \\ \dot{\tilde{x}} \end{pmatrix} = \begin{pmatrix} A-BK  & BK \\ 0  & A-KC \end{pmatrix} \begin{pmatrix} x \\ \tilde{x} \end{pmatrix} + \begin{pmatrix} Bk_{r} \\ 0  \end{pmatrix}r = A_{e}\begin{pmatrix} x \\ \tilde{x} \end{pmatrix} + B_{e}r \\ y = \begin{pmatrix} C & 0 \end{pmatrix} \begin{pmatrix} x \\ \tilde{x} \end{pmatrix} = C_{e} \begin{pmatrix} x \\ \tilde{x} \end{pmatrix}\end{align}$$
$A_e$ är blocktriangulär och dess karak. polynom är $$det(sI-A) = det(sI-(A-LK)) \cdot det(sI - (A-LC))$$
**Alltså** produkten av karak. polynom vid tillståndsåterkoppling och kalmanfiltret. 

**Överföringsfunktionen** blir $$\begin{align} G_{e}(s) = C_{e}(sI-A)^{-1}B_{e} = \begin{pmatrix} C & 0 \end{pmatrix} \begin{pmatrix} E \\ F \end{pmatrix} \end{align}$$
där $$\begin{pmatrix} E \\ F \end{pmatrix} = \begin{pmatrix} sI-(A-BK) & -BK \\ 0 & sI - (A-LC) \end{pmatrix}^{-1} \begin{pmatrix} Bk_{r} \\ 0 \end{pmatrix} = C(sI - (A-BK))^{-1} Bk_{r}$$
Kalman filtret har alltså försvunnit. Överföringsfunktioen blir alltså $$G_{e}(s) = C(sI - (A-BK))^{-1} Bk_{r}$$
**Notera:**
Med en n:te ordningens överföringsfunktion svarar mot n [[Styrbarhet|styrbara]] och [[Observerbarhet|observerbara]] tillstånd. Eventuellt övriga tillstånd är inte styrbara och observerbara.

#regler 