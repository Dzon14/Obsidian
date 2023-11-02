---
aliases: [tillståndsåterkoppling]
---
# State Feedback
**Begränsningar:**
- Vi kan normalt inte mäta samtliga tillstånd
- Regulatorn saknar [[Integralverkan]], riskerar att få kvarstående stationära reglerfel.
#### Process
(In state space form)
$$\begin{cases} \dot{x} = Ax + Bu \\ y = Cx \end{cases}$$
A tell if it's stable or not (the eigenvalues)
The characteristic polynom $$det(sI-A)$$
#### Regulator (controller)
![[Pasted image 20220914110748.png||550]]

Regulatorn kan skrivas enligt 
![[Pasted image 20220914110958.png|550]]
Kan också skrivas (från förel.): $$u = l_{r}\cdot r - Lx$$
### Slutna systemet (Closed-loop system)
Med ekv från process och regulator så får vi $$\begin{cases} \dot{x} = (A-BL)x + Bl_{r} \cdot r \\ y = Cx \end{cases}$$
**Kar.polynom:** $$det(sI-(A-BL))$$
- Bestäm L så att egenvärdena till $(A-BL)$ placeras lämpligt.
		- Välj $l_r$ så att $y=r$ blir stationärt

**Se pdf för exempel (s.69)**

**Open-loop:**
Överföringsfunktionen ges av $$G(s)=C(sI-A)^{-1}B+D$$
**Closed-loop:** $$G(s) = C(sI-(A-BK))^{-1}Bk_{r}R(s)$$
**Stationary gain:** $$G(0) = C(-A + BK)^{-1}Bk_{r}$$
#regler