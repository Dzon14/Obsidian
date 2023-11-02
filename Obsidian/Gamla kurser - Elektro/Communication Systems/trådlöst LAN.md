---
tags: [komsys]
aliases: [wireless LAN, WLAN]
---
# Trådlöst LAN 
De flesta hushåll har detta. Uppbyggt kring en basstation som kontrollerar nätet.

## MAC-protokoll
Finns två olika.

#### Distributed Coordination Function (DCF)
Använder [[CSMACA]] kombinerat med en reservationsmetod. Det sistnämnda löser "Hidden Terminal Problem" som finns i alla WLAN. Problemet är att både terminal A och B kan höra basstation, men A kan inte höra B och tvärtom. Därmed kan både A och B råka skicka data till basstationen samtidigt. 
- Att lösa detta finns på s. 103.

#### Point Coordination Function (PCF)
Centraliserad [[accessmetod]], där basstationen styr accessen till mediet. Basstationen skickar polls till varje station i tur och ordning om de har data att skicka. 