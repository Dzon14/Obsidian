---
tags: [elenergi]
aliases: [asynkronmaskinen]
---
# Asynkronmaskin
- En elektrisk maskin där rotorns varvfrekvens/varvtal varierar med lasten. Till skillnad från [[synkronmaskin]] så roteras fältet runt lindningen (som står still) istället för tvärtom. Slingan är dessutom kortsluten och bara dess egen resistans återstår.
![[Pasted image 20230302110136.png|400]]
![[Pasted image 20230302110010.png|550]]

 [[torque|Vridmomentet]] gör att slingan vill rotera med fältet, och en fri slinga hade därmed roterat _synkront_ med fältet - dvs $\omega_\text{rotor}=\omega_s$. En bromsad slinga kommer rotera **asynkront**: $\omega_\text{rotor}<\omega_s$. Rotorströmmen induceras således av skillnaden mellan fältets och rotorns rotationshastighet.

- Kan likströmsbromsas
		- 
- Kan i motsats till [[synkronmaskin]] direktstartas 
		- Direktstart går alltså bra men ger hög startström
		- Kraftelektronik kan ge mjukstart utan hög ström

## Simulink
- Kan komma en uppgift på detta på tentan
- Simulink-modell av $L \frac{di(t)}{dt}=u(t)=Ri(t)$
![[Pasted image 20230123134932.png]]

## Generisk asynkronmaskin
- Fältet roterar runt lindningen som hålls still $\Rightarrow$ [[torque|vridmomentet]] verkar för att lindningen ska följa det roterande fältet.
- Fältet från magneterna roteras med vinkelhastighet $\omega_{s}$ (t.ex trefaslindning matad med symmetrisk trefasspänning)
- Slingan är kortsluten och bara dess egen (lilla) resistans återstår
- Rotorn är fri att rotera

## Generisk asynkronmaskin - vridmoment
Momentet motverkar induktionen; vill slingan ska följa fältet
Fri slinga roterar synkront med fältet
-  Då är $\omega_{rotor} = \omega_{s} \Leftrightarrow$ synkront
-  Ingen emk, ström eller moment 
- [[tomgång]]
Bromsad slita roteras **asynkront**
- Då blir $\omega_{s} < \omega_{s} \Leftrightarrow$ asynkront
- Emk induceras $\rightarrow$ ström $\rightarrow$ moment
- $\omega_{s}-\omega_{rotor}$ avgör rotorströmmens frekvens

I asynkronmaskinen induceras rotorströmmen av skillnaden mellan fältets och rotorns $\omega$. Vid belastning roterar rotorn **asynkront** med fältet.

## Verkligas AM - idag trefasig
- Tvåfasig förr - första AM var tvåfasig

- Statorn har trefaslindning för trefasspänningar
		- Statorplåtar staplas till cylinder, koppartråd lindas i spåren
- Rotorn har oftast burrotor (många kortslutna slingor)
		- Rotorplåtar stap,as till cylinder, bur gjorts av aluminium

## Ekvivalent schema
![[Pasted image 20230123143816.png]]
- Sinusformad $V_{s}$
- $R_{s}$ - statorlindning, $R_{r}$ - rotorbur
- $X_{m}$ - gemensamt flöde för stator och rotor
- $X_{s \lambda}$ och $X_{r \lambda}$ - läckflöden som inte gör nytta
$$P_{12}= \frac{R_{r}}{s}i_{r}^{2} \Leftrightarrow \text{ mekaniska effekten } T \omega_{s}$$

## Moment-varvtalskarakteristik
![[Pasted image 20230123144752.png]]


## Start av asynkronmotor
![[Pasted image 20230124082152.png]]
Aynkronmotorn kan (t skillnad från synkron) direktstartas (50Hz för stillastående motor).
- Direktstart går alltså bra men ger hög startström
- Kraftelektronik kan ge mjukstart utan hög ström

## Från dugga
$$\text{märkvarvtalet} = n_{n} = (1-s_n)n_{0}$$där $n_{0}$ är varvtalet vid [[tomgång]].

## Se även 
- [[synkront varvtal]]
- [[eftersläpning]]
- [[märkdrift]]
- [[tomgång]]
- [[infasning]]
- [[strömtång]]