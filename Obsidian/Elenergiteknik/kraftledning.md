---
tags: [elenergi]
---
# Kraftledning
Olika typer:
- Friledning
- Belagd ledning
- Hängkabel
- Kabel

I städer är det vanligast med nedgrävd kabel, i Europa. I USA kör de fortf med mycket friledningar i städer...

Överföra effekt:
- Ström (ledararea)
- Spänning (isolation)

## Strömhantering
![[Pasted image 20230124092225.png|300]]
Finns generellt två olika fasledare (ström), där tvärsnittsarea spelar roll. Större tvärsnittsarea $\Rightarrow$ mindre förluster. Dock blir det en tyngre ledning med större tvärsnittsarea $\Rightarrow$ dyrare. Optimalt ligger där mellan någonstans.
![[Pasted image 20230124092157.png|300]]
Designfaktorer på fasledaren är strömförträngnin, maxström, uppvärmning, nerhängning, tvärsnittsarea osvosv.

## Spänningshantering 
![[Pasted image 20230124092609.png|300]]
**Isolation:**
Man har oftast keramisk tallriksisolator i isolatorkedja som är fäst i stolpe och bär fasledare. Isolatorkedjan har en längd på ca 4 m per 400 kV. 
- Har man problem med salt och fukt behövs längre isolatorkedjor
**Stolpen:**
- Topplinor för att skydda mot blixtnedslag, så det går genom stolpen istället för ledning.
- Designfaktorer är: E och B fält, Stolphöjd, Utseende, Geometri, Kraftledningsyta.
**Fasledaren:**
VI vill öka ledardiametern så:
Duplex (två ledare per fas) eller triplex, ökar ekvivalent radie.
![[Pasted image 20230124093350.png|200]]

## Fält från trefasig kraftledning
![[Pasted image 20230124093248.png]]
B-fält i en lång rak ledare: $\vec{B}(t,r) = \frac{\mu_{0}i(t)}{2 \pi r}\vec{e}_{B}$
Fält i punkten P = summan av bidragen från de tre faserna
1. Olika avstånd r till P från de tre fasledarna
2. Olika i(t) i de tre fasledarna
3. De tre fältbidragen har olika riktning $e_{B})$
E-fält är $$\vec{E}(t,r) = \frac{\lambda(t)}{2 \pi \varepsilon_{0} r}\vec{e}_{r}$$ där $\lambda(t)$ är laddningar per längdenhet

## Ledningsmodell
Resistans kommer finnas i ledningar.
![[Pasted image 20230124094125.png]]
- Coronaförlust är att det blir varmt typ

## Skruvning av fasledare 
![[Pasted image 20230124094547.png |200]]
Vi byter plats på ledningar så vi får symmetri och de ska "sitta lika mycket i samma position??"
- Kallas för skruvning eller transponering

## Kabel och kabelmodell
Enfaskabel eller trefaskabel.
En bra grej med dessa är att ledare är isolerade från varandra och väder osv.
I städer är de nedgrävda (iaf Euorpa). I USA hänger de..
På landsbygd är det nergrävd, nerplöjd eller hängkabel

För kabelmodellen är C kapacitans viktigast (till skillnad från ledningsmodell med induktans som viktigast).
![[Pasted image 20230124095101.png|400]]

## [[långdistans effektöverföring]]

## Ökad överföringskapacitet
- Höjd spänning
- Fler fasledare (bättre än tjocka ledningar)
- Reaktiv seriekompenseirng