---
aliases: [controllability]
---
# Styrbarhet
What is the requirement for controlling a state?
Vad är kravet för att styra ett tillstånd?

- It is not always possible to place a [[Poles|pole]] (or eigenvalues) of the close-loop system wherever you want. (In example in pdf for state feedback, we place it ourselves).

**Styrbarhet:** En tillståndsvektor $x_0$ är styrbar om det finns en styrsignal som överför tillståndet $x$ från origo (jämviktsläget) till $x_0$ på ändlig tid. 
Ett system är styrbart om samtliga tillstånd är styrbara.

- Hur avgör jag om processen är styrbar?

$$\begin{cases} \dot{x} = Ax + Bu \end{cases}$$
**Styrbarhetsmatrisen:**$$W_s = \begin{pmatrix} B & AB & A^{2}B &  ... & A^{n-1}B \end{pmatrix}$$
n är systemets ordning. $$\text{Systemet styrbart} \Leftrightarrow W_{s} \text{har n linjärt oberoende kolonner} \Leftrightarrow detW_{s} \neq 0$$
### Exempel
$$\begin{align} \dot{x} = \begin{pmatrix} -10 & 0 \\ 1 & 0 \end{pmatrix}x + \begin{pmatrix} 100 \\ 0 \end{pmatrix}u \\ y=\begin{pmatrix} 0 & 1 \end{pmatrix}x  \ \ \ \ \ \ \ \ \ \ 
 \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \  \end{align} $$
 Då blir styrbarhetsmatrisen: $$ \begin{align} W_{s} = \begin{pmatrix} B & AB \end{pmatrix} = \begin{pmatrix} 100 & -1000 \\ 0 & 100 \end{pmatrix} \\ \\ detW_{s}= 1000 \neq 0 \Rightarrow \text{styrbart}\end{align}$$
#regler 