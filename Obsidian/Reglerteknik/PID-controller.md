---
tags: [regler, PID control, PID-reglering]
---
# PID-controller
Proportional integral derivative controller
- control loop employing feedback. 
- The most common regulator/controller

Uses different [[Control strategies]] (See all).

![[Pasted image 20220830143654.png]]

- The proportional part ([[Proportional control strategy|P-delen]]) contributes with the controlling signal (styrsignal) which is proportional to the actual controlling error. 
- The Integral part ([[Integral control strategy|I-delen]]) is the memory of the PID. 
- The derivation part ([[Proportional control strategy|P-delen]]) predicts future errors. 

### Serieformen av PID-regulatorn
PID-regulatorn kan beskrivas med **Parallellformen:**$$u = K \left(e + \frac{1}{T_{i}} \int\limits_{}^{} e(t) \ dt + Td \ \frac{de}{dt} \right)$$
Med överföringsfunktionen $$G_{R}(s) = K \left(1 + \frac{1}{sT_{i}} + sT_{d}\right)$$
Eller med **Serieformen:** $$G_{R}'(s) = K' \left(1+ \frac{1}{sT_{i}'}\right)(1+sT_{d}') = K' \left( 1 + \frac{T_{d}'}{T_{i}'} + \frac{1}{sT_{i}'} + sT_{d}' \right)$$
Namn kommer från seriekoppling aven PI- och en PD-regulator. Skillnaden i formen är att parametrarna betyder olika saker. 

## [[PID-regulatorns Bodediagram]]

## [[PID-regulatorns parametrar]]

## Praktiska modifieringar av PID-regulatorn

#### Modifiering av [[Proportional control strategy|P-delen]]
$$u_{p}= Ke$$
$0 \leq b \leq 1$ , **börvärdesviktning** 

- Anledningen till att man ibland vill reducera referensvärdet i [[Proportional control strategy|P-delen]] är dels att man på det sättet kan reducera överslängen vid stegändringar i r, dels att man undviker alltför snabba ändringar i styrsignalen och därmed slitage på utrustningen vid snabba börvärdesändringar.

#### Modifiering av [[Integral control strategy|I-delen]]
 Integraltermen ges av $$u_{I}= \frac{K}{T_{i}} \int\limits_{}^{} e(t) \ dt = \frac{K}{T_{i}} \int\limits_{}^{} (r-y) \ dt$$
 ![[Pasted image 20220927165527.png]]
- Integratoruppvridning sker (windup) . Integratordelen kommer ej sluta om det fortfarande finns ett fel. Det kan bli en dålig loop enligt bild. 
- Lösning är att sluta uppdater integraldelen när styrsignalen mättar (vid max-strecket) - **anti-windup**
 
#### Modifiering av [[Derivative control strategy|D-delen]]
$$u_{D}= KT_{d}\frac{de}{dt} = KT_{d} \left( \frac{dr}{dt} - \frac{dy}{dt}\right)$$
Detta sätt att derivera glr dock så man får stora ändringar i snabba varioationer i e. Därför:
1) Derivera inte r. $$u_{D} = -KT_{d} \frac{dy}{dt}$$
2) Lågpassfiltrera y
$$KT_{d}s \longrightarrow \frac{KT_{d}s}{1+sT_{f}}$$
där $T_{f} = \frac{T_{d}}{N}$

- Den pol lågpassfiltret bidrar med medför att högfrekvensförstärkningen blir $K(1+N)$.



