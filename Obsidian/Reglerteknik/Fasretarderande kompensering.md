---
tags: [regler]
aliases: [lag compensation]
---
# Fasretarderande kompensering
- Lyfter förstärkning vid låga frekvenser
$$G_{K}= \frac{s+a}{s+ \frac{a}{m}} = M \cdot \frac{1+ \frac{s}{a}}{1 + s \frac{M}{a}}$$
där $M > 1$.
Vi har en [[Poles|pol]] vid $\omega = \frac{a}{M}$ som bryter ned frekvensen och sedan ett [[Zeros|nollställe]] vid $\omega = a$ som bryter upp.  **Bodediagrammet** blir 
![[Pasted image 20220926171500.png]]

**Egenskaper:**
- Höjer förstärkningen vid låga frekvenser
- Minskar fasen

**Användning:**
- Minska stationära fel
- $G_{0}$ innehåller integrator $\Rightarrow$ felet minskar $M$ gånger.

**Parametrar:**
- M : Förstärkningen M ges av specifikationerna på hur mycket vi vill minska det stationära felet. Om den ursprungliga kretsöverföringsfunktionen $G_{0}$ innehåller minst en integrator kan man visa att det stationära felet minskar precis en faktor M.
- a : Brytfrekvensen a bestämmer vid vilken frekvens förstärkningen i kompenseringslänken ska brytas ner från M till ett. En vanlig metod är att välja a så att den negativa fasvridningen inte påverkar fasmarginalen alltför mycket. Tumregeln $$a = 0.1 \omega_c$$
## Procedur
1) Bestäm M ur specifikationer på stationära fel.
2) $a = 0.1 \omega_{c} \Rightarrow$ fasmarginalen minskar högst 6 grader.

## Exempel (elmotor)
Kretsöverföringsfunktionen $$G_{0} = \frac{100}{s(s+10)}$$
- Minska stationära rampfelet med en faktor 10.
- Behåll snabbhet och robusthet

1) $G_{0}$ innehåller integrator $\Rightarrow M= 10$.
$$\lvert G_{0}(i \omega_c) \rvert = \frac{100}{w_{c} \sqrt{w_{c}^{2}+100}} = 1$$ Beräkna numeriskt ger $\omega_{c} \approx 8 \ rad/s$.

Med och utan kompenseringslänk nedan
![[Pasted image 20220926173105.png]]
Skärfrekvensen ligger kvar på samma ställe. Fasen kvar på samma ställe med en lite dipp. Sänkt ungefär 6 grader.
