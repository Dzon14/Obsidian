---
aliases: [integral action]
---
# Integralverkan
- Integralverkan ger en pol i $s=0$ vilket eliminerar [[Stationary Errors|stationära fel]].

![[Pasted image 20220915105020.png]]
e - reglerfelet (differensen mellan referensvärdet r och mätsignalen y)
$k_i$ - någon förstärkning
Slutligen adderas bidraget från integraltermen till styrsignalen u.

Utgå från processen $$\begin{cases} \dot{x} = Ax + Bu \\ y = Cx \end{cases}$$Inför ett extra tillstånd $$x_{i}= \int_{}^{} (r-y) \ dt \ \ \Rightarrow \ \ \dot{x} = r-y = r-Cx$$
utvidga tillståndsvektorn x med integraltillståndet $x_i$ $$\begin{align} x_{e} = \begin{pmatrix} x \\ x_{i} \end{pmatrix}\end{align}$$
Så får vi $$\begin{align} \dot{x_{e}}= \begin{pmatrix} \dot{x} \\ \dot{x_{i}} \end{pmatrix} = \begin{pmatrix} A & 0 \\ -C & 0 \end{pmatrix} x_{e}+ \begin{pmatrix} B \\ 0 \end{pmatrix} u +\begin{pmatrix} 0 \\ 1 \end{pmatrix}r = A_{e}x_{e} + B_{e}u + B_{r}r \\ y = \begin{pmatrix} C & 0 \end{pmatrix} x_{e}=C_{e}x_{e}\end{align}$$
Eliminera styrsignalen u från ekvation ovan så vi får fram det slutna systemets tillståndsbeskrivning $$u = k_{r}r - Kx - k_{i}x_{i} = k_{r}r-K_{e}x_{e}$$
där $K_{e} = \begin{pmatrix} K & k_{i} \end{pmatrix}$
Stoppa in detta i ekvationen för $\dot{x_{e}}$ så får vi $$\begin{cases}  \dot{x_{e}}= (A_{e}-B_eK_{e})x_{e} + (B_{e}k_{r}+B_{r})r \\ y = C_ex_{e}\end{cases}$$
**Vi har nu fått en regulator med integralverkan!** Notera att formen är lik formen för det slutna systemet i [[State Feedback|tillståndsåterkoppling]].
Slutligen:
1) Bestäm $K_e$ så att egenvärdena till $(A_{e}-B_{e}K_{e})$ placeras lämpligt.
2) Bestäm $k_{r}$ så att transienter vid ändringar i $r$ får önskade egenskaper. 

#regler