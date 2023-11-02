---
tags: [regler]
aliases: [cascaded controllers]
---
# Kaskadkoppling
En av de vanligaste kopplingarna i industrin. Den utnyttjar flera signaler (än mätsignal och styrsignal)

Kaskadreglering är en reglerstrategi som bygger på en kombination av två regulatorer, där utsignalen från den ena regulatorn bildar börvärde till den andra. Detta illustreras i följande exempel.

## Exempel - värmeväxlare
![[Pasted image 20221003151216.png|300]]
Vi vill reglera temperaturen på sekundärsidan genom att styra ångventilen på primärsidan. Temperaturregulatorn arbetar direkt på ångventilen (i figuren).
- Antag att ångtrycket på primärsidan plötsligt minskar (trycksänkning). Då kommer ånglödet minska vilket leder till att vattnet på sekundärsidan inte värms upp lika mycket. Temp.regulatorn kommer då ge order om en större ventilöppning och efter ett tag kommer ångflödet åter vara rätt. Alltså inte den bästa reglerstrategin. 
- Man kan koppla in en flödesregulator enligt bild nedan. En inre reglerkrets som ser till att ångflödet regleras.
- ![[Pasted image 20221003151644.png|300]]
Där den högra är primärregulator och den vänstra sekundär (också master and slave).
- Kaskadregleringen innebär att huvudregulatorn $R_{1}$ får en enklare arbetsuppgift. $R_{2}$ tar en del av arbetet. 

## Allmänna principen för kaskadreglering
![[Pasted image 20221003151823.png|450]]
- Med en inre regulator uppnår vi en effektivare reglering, med två mätsignaler. 
- PID-regulatorn kan göra mer avancerade lösningar med kaskadreglering. Vi kan ta hand om störningar som kommer in på processavsnittet $P_{2}$ snabbare, innan den ger störning till den primära mätsignalen $y_{1}$.
- När man ställer in regulatorerna, börja med $R_{2}$ sedan $R_{1}$.
