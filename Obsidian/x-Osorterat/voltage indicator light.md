---
tags: [lfs]
aliases: [VIL]
---
# Voltage Indicator Light
[[Battery Management System|BMS]]

Ska lysa om 60V $\rightarrow$ därför zenerdiod i kretsen

LED Driver (doesn’t work by itself):
- [AL5890-20P1-13 Diodes Incorporated | Mouser Sverige](https://www.mouser.se/ProductDetail/Diodes-Incorporated/AL5890-20P1-13?qs=W0yvOO0ixfFCSjYJtC119A%3D%3D)

LED:
-  [55733.qxd (farnell.com)](https://www.farnell.com/datasheets/1498852.pdf) 
- (En standard från typ electrokitet)
- Använd samma som förra året.

Lösning
- Mergea ideerna, göra så robust som möjligt
- Viastor?
- [Constant Current Source: Transistor Active Source » Electronics Notes (electronics-notes.com)](https://www.electronics-notes.com/articles/analogue_circuits/transistor/active-constant-current-source.php)

## Komponenter

#### Transistorer
- High voltage npn transistor: BUL216 (or TO-220) (har denna)
- Den andra?

#### Dioder
- LED - MARL 508 series, panel indicator light
**Zenerdioder:**
- (Mot LED)
- (För backström) - [BZD27C180P-M3-08 Vishay Semiconductors | Mouser Sverige](https://www.mouser.se/ProductDetail/Vishay-Semiconductors/BZD27C180P-M3-08?qs=asPD7ZL2j3U9gZNWQ6BPQg%3D%3D)  (3 st i serie? blir 540 V i zenerspänning) (CAD-modell finns)

#### Resistorer (& Varistor)
- 35$\Omega$ Resistor ($20 \Omega + 15 \Omega$):
		  - [ERJ-6ENF20R0V Panasonic | Mouser Sverige](https://www.mouser.se/ProductDetail/Panasonic/ERJ-6ENF20R0V?qs=50QC8w71jAvNk%252BIpCu3Iyw%3D%3D)
		  - [ERJ-2RKF15R0X Panasonic | Mouser Sverige](https://www.mouser.se/ProductDetail/Panasonic/ERJ-2RKF15R0X?qs=MVjVSMjNRMow7ysSTxlC%252Bw%3D%3D)
- Resistor innan zenerdiod:
- Resistor innan transistor (1 $M \Omega$)
- 


