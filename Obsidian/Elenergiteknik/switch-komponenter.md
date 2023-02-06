---
tags: [elenergi]
---
# Switch-komponenter
Istället för att styra manuellt använder vi komponenter!

- Transistor - IGBT (eller MOSFET)
		- $u_{GE}$ styr $i_{c}$
		- vid användning som switch används bara extremlägena bottnad (till) och strypt (från). Bara på och av
- Diod
		- Icke styrbar: leder när $u>0$, annars inte. 
		- backventil
Diod och transistor antas i kraftelektronik ofta ideala: som kortslutning (u=0) eller avbrott (i=0).

**Switchfrekvens:** $$f_{sw}=\frac{1}{T_{sw}}=\frac{1}{T}$$
Vid användning av endast transistor är det lätt att spränga den iom spänning över den går mot oändlig. Därför använder man en **frihjulsdiod** som ger strömväg när transistorn är "från".

Transistor TILL: (diod = avbrott) Positiv strömderivata, induktansen upptar energi - $L \frac{di_{L}}{dt}=U_{dc}-u_{ut} > 0$
Transistor FRÅN: (diod leder): Negativ strömderivata, induktansen avger energi - $L \frac{di_{L}}{dt} = 0-u_{ut} <0$ 

## Switch-förluster
- Låga förluster vid switchning
![[Pasted image 20230206144453.png]]

- Förluster = effekt = $u_{T}i_{T}$ eller $U_{D}i_{D} =$ hela tiden (nära) noll i både T och D!
- Låga förluster $\rightarrow$ lite värme $\rightarrow$ litet kylbehov $\rightarrow$ hög verkningsgrad $\eta > 95\%$

- Varje switchning ger förlust $\rightarrow$ lågt $f_{sw}$
- Switchfrekvensen ska inte märkas i utspänningen $\rightarrow$ högt $f_{sw}$
- Fyrkvadrantbrygga med triangelvåg och $v_{b,ref} = -v_{a,ref}$
		- förluster som $f_{sw}$
		- Utspänning med $2f_{sw}$ - alltid något!
