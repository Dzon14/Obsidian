---
aliases: [observability, observerbara, observerbar]
---
## Observerbarhet
Man kan inte alltid mäta samtliga tillstånd i processen, utan de måste vara "vettiga".
Om man kan beräkna tillståndsvektorn genom att studera styrsignalen och mätsignalen kan man använda de skattade tillstånden i återkopplingen.

**Definition:** 
- En Tillståndsvektor $x_{0} \neq 0$ är icke observerbar (tyst tillståndsvektor) om mätsignalen $y=0$ då initialtillståndet är $x_{0} \ \text{och} \ u=0$. 
- Ett system är oberserverbart om det saknar tysta tillstånd. 

**Observerbarhetsmatrisen:**
Om vi har en tillståndsbeskrivning $$\begin{cases} \dot{x} = Ax \\ y = Cx \end{cases}$$
där $x(0) = x_0$ , så får vi observerbarhetsmatrisen

$$W_{0}=\begin{pmatrix} C \\ CA \\ ... \\ CA^{n-1} \end{pmatrix}$$
$$\text{Observerbart} \Leftrightarrow W_{0} \ \text{har n linjärt oberoende rader} \Leftrightarrow det(W_{0}) \neq 0$$
$$x_{0} \ tyst \Leftrightarrow W_{0}x_{0} = 0$$
### Exempel
$$\begin{align} \dot{x} = \begin{pmatrix} -1  & 0 \\ 0 & -1 \end{pmatrix}x \\ y = \begin{pmatrix} 1 & -1 \end{pmatrix}x \end{align}$$
där $\dot{x_{1}} = -x_{1}$ och $\dot{x_{2}}= -x_{2}$
Ekvationerna beskriver processen
![[Pasted image 20220915113734.png|300]]
Mätsignalen bildas av differensen mellan de två nivåerna. 
$$W_{0}= \begin{pmatrix} C \\ CA \end{pmatrix} = \begin{pmatrix} 1 & -1 \\ -1 & 1 \end{pmatrix}$$
Raderna är linjärt beroende rader och $$det(W_{0}) = 0$$alltså **EJ** observerbart. 

Ur ekv. $$W_0x_{0}= 0$$ så kan vi skriva $$\begin{align} \begin{pmatrix} 1 & -1 \\ -1 & 1 \end{pmatrix} \begin{pmatrix} a \\ b \end{pmatrix}= \begin{pmatrix} a-b\\-a+b \end{pmatrix} = \begin{pmatrix} 0\\0 \end{pmatrix} \Rightarrow a = b \ \text{och vi får} \\x_{0}= \begin{pmatrix} a\\a \end{pmatrix}\end{align}$$
#regler