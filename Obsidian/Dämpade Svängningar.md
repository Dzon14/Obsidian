---
tags: [fysik]
---
# Dämpade Svängningar


En fjäder som oscillerar dämpas av luftmotståndet. För varje svängning försvinner en del av [[Energi|energin]]. Det är alltså inte ett system utan förluster. Den dämpande kraften ges av
$$F_d = -bv$$
där b är en konstant. Rörelseekvationen dämpat är (kan härledas med newtons andra lag?)
$$\frac{d^2 x}{dt^2} + \frac{b}{m} \cdot \frac{dx}{dt} + \omega_0 ^2 \cdot x = 0$$


Genom att lösa denna differentialekvation allmänt får man 

$$x(t) = Ce^{rt}(r^2 + \frac{b}{m} \cdot r + \omega_0 ^2) = 0$$

där C är en konstant, och 

$$    r = - \frac{b}{2m} \pm \sqrt{\left(\frac{b}{2m}\right)^2\omega_0^2}$$

där $\frac{b}{2m}$ är "dämpningen".  

### Överdämpad

Ett överdämpat system svänger inte alls, utan är så pass dämpat att dess hastighet går mot noll medan den närmar sig sitt jämvitksläge. 

Ett system är överdämpat om $\frac{b}{2m} > \omega_0$. Det leder till att $r_1$ och $r_2$ blir reella och mindre än 0 (rötterna till ekvationen för r ovan), titta på vad som händer i rotuttrycket).

Ekvationen för x får även följande lösning:
$$    x(t) = C_1 e^{-r_1 t} + C_2 e^{-r_2 t}$$

### Kritiskt dämpad

Ett system är kritiskt dämpat om $\frac{b}{2m} = \omega_0$. Det är även då x går fortast mot 0. Det ger följande lösning
$$    x(t) = (C_1 t + C_2)e^{-\frac{b}{2m}t}$$

### Underdämpad

Ett system är underdämpat om $\frac{b}{2m} < \omega_0$. Ekvationen får följande lösning
$$x(t) = A_0e^{-\frac{b}{2m}t} cos(\omega't + \delta)$$ där $A_0$ är den
ursprungliga amplituden och $\omega'$ är
$$\omega' = \sqrt{\omega_0^2 - (\frac{b}{2m})^2}$$

[[Energi|Energin]] i ett underdämpat system avtar exponentiellt med tiden. [[Energi|Energin]] ges av
$$E = \frac{1}{2}m\omega^2A^2 = \frac{1}{2}mw^2(A_0e^{-(\frac{b}{2m})t})^2 = \frac{1}{2}mw^2A_0^2e^{-(\frac{b}{2m})t} = E_0e^{-\frac{t}{\tau}}$$
där $E_0 = \frac{1}{2}m\omega^2A_0^2$ och $\tau = \frac{m}{b}$

Q-faktorn, även kallad [[Kvalitetsfaktor|kvalitetsfaktorn]] är ett mått på ett systems
energiförlust per period, alltså ett mått på hur underdämpat en
svängning är. Kan också definieras som förhållandet mellan
resonansfrekvensen och bandbredden för ett drivet system.

$$Q = \omega_0 \tau$$

där $\tau = m/b$ är tidskonstanten (tiden det tar för [[Energi|energin]] att
förändras med en faktor $e^{-1}$. Bredden på resonanskurvan
$\Delta \omega$ ges av $$\Delta \omega = \frac{\omega_0}{Q}$$