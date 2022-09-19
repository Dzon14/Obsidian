---
aliases: [pole-zero cancellation]
---
# Förkortning av poler och nollställen
Förlust av [[Styrbarhet]] och [[Observerbarhet]] hänger samman med förkornting av poler och nollställen i överföringsfunktionen. Det är inte ovanligt att man förlorar styrbarhet och observerbarhet genom att förkorta dynamiken i systemet (genom regulatorn).

PI-regulatorn har en överföringsfunktion: $$G_{R}(s) = K\left(1 + \frac{1}{sT_{i}} \right) = K \frac{1+sT_{i}}{sT_{i}}$$
K är regulatorförstärkningen och $T_{i}$ är integraltiden.
Processen beskrivs med $$G_{P}(s) = \frac{1}{1+sT}$$
Välj integraltiden lika med processens tidskonstant $T_{i}= T$. 

![[Pasted image 20220919165330.png|500]]

**Efter förkortning får vi:**
![[Pasted image 20220919165413.png]]

$$\begin{align}  Y = \frac{K}{sT}(R-Y) \\ \left(1+\frac{K}{sT}\right)Y=\frac{K}{sT}R = Y = \frac{\frac{K}{sT}}{1+\frac{K}{sT}}R = \frac{K}{sT + K}R\end{align}$$
Vi får $$Y(s) = \frac{K}{K + sT}R(s) + \frac{sT}{(1+sT)(K+sT)}L(s)$$(från pdf)

**Slutsats:** Förkortning av poler och nollställen kan vara farligt då det innebär att att det finns tillstånd som inte är styrbara eller observerbara. 
	Det är alltså säkrast att placera samtliga poler i överföringsfunktion på lämpliga ställen utan att förkorta bort dem mot nollställen. 



#regler