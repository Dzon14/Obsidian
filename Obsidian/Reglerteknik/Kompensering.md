---
tags: [Regler]
aliases: [lead-lag compensation]
---
# Kompensering
**Kompensering av Bodediagram:**
Om man redan har en regulator men når ej önskad prestenda, då kan man lägga till ytterligare dynamik - kompensera Bodediagrammet. 

**Kompensering:**
![[Pasted image 20220926165812.png]]
där $G_{K}$ är en koompenseringslänk. 
- Då får vi en ny kretsöverföringsfunktion: $$\begin{align} G_{0}^{ny} = G_{K }G_{0}  \end{align}$$
- Välj $G_{K}$ så att $G_{0}^{ny}$ uppfyller specifikationer i Bodediagrammet. 
$$\begin{cases}   log \lvert G_{0}^{ny} \rvert = log \lvert G_{0} \rvert+log \lvert G_{K} \rvert \\ argG_{0}^{ny} = argG_{0}+argG_{K}\end{cases}$$
Med detta ovan kan vi bestämma kompenseringslänken som differensen mellan den nya/önskade kretsöverföringen med den ursprungliga.
![[Pasted image 20220926170615.png|500]]

## Två kompenseringslänkar
- [[Fasretarderande kompensering]]
- [[Fasavancerande kompensering]]