---
tags: [regler]
aliases: [discretization of the PID controller]
---
# Diskretisering av en [[PID-controller|PID-regulator]]
För att implementera en kontinuerlig regulator i en dator måste man approximera deriveringar och integreringar med differenser och summeringar.

Laplacetransform för [[PID-controller|PID-regulatorn]]: $$U = K \left( (bR-Y) + \frac{1}{sT_{i}}E - \frac{sT_{d}}{1+\frac{sT_{d}}{N}} Y\right)$$
Notera filtret framför Y. Den diskreta styrsignalen kan skrivas som $$u(kh) = P(kh) + I(kh) + D(kh)$$
#### Diskretisering av [[Proportional control strategy|P-delen]]
Den kontinuerliga delen är
$$u_{P}(t) = K(br(t)-y(t))$$
och den diskreta delen blir $$P(kh)=K(br(kh)-y(kh))$$
#### Diskretisering av [[Integral control strategy|I-delen]]
Den kontinuerliga integraldelen ges av $$u_{I}(t) = \frac{K}{T_{i}} \int\limits_{0}^{t} e(t) \ dt$$
och vi approximerar integralen med en summa $$I(kh) = \frac{K}{T_{i}} \cdot h \sum_{i=1}^{k}e(ih)$$
där en mer användbar form är den rekursiva formen $$I(kh) = I(kh-h) + \frac{Kh}{T_{i}}e(kh)$$
#### Diskretisering av [[Derivative control strategy|D-delen]]
Från regulatorns överföringsfunktion får vi följande derivatatermen: $$\left(1+\frac{sT_{d}}{N} U_{D}\right) = -KT_{d}sY$$
genom att inverstransformera får vi $$u_{d}(t)+ \frac{T_{d}}{N}\frac{du_{d}(t)}{dt} = -KT_{d} \frac{dy(t)}{dt}$$
sedan approximerar vi derivatorna och ersätter med differenser $$D(kh) + \frac{T_{d}}{N}\frac{D(kh)-D(kh-h)}{h} = -KT_{d}\frac{y(kh)-y(kh-h)}{h}$$
Derivatatermen blir $$D(kh) = \frac{T_{d}}{T_{d}+Nh}D(kh-h)-\frac{KT_{d}N}{T_{d}+Nh}(y(kh)-y(kh-h))$$