---
tags: [komsys]
---
# CSMA/CA
- Carrier Sens Multiple Access with Collision Avoidance
Utvecklats för trådlösa nätverk, då CSMA/CD ger många kollisioner för trådlöst. CA har funktioner för att undvika kollisioner. 
- Om länken är ledig, väntar terminalen en tid  (Interframe space). Om fortfarande ledig så går terminalen in i Contention Window där det är indelat i tidsluckor och terminalen väljer slumpmässigt några av dessa som den väntar. Om ledig efter CW skickar terminalen sin data annars starta om CW. 
- Algoritmen brukar även innehålla ett ACK från mottagaren.