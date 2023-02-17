---
tags: [elenergi]
aliases: [elnätet]
---
# Elnät

Se frekvensens betydelse i [[kraftverk]]

## Stor serieimpedans ger svagt nät
- Seriereaktans överallt (Generator, Ledning, Transformator)
- Pp lågspänning dominerar serie**resistans**.
- Serieimpedansen (tänk Thevenin-impedans) begränsar kortslutningsström
- $\Rightarrow$ Ström genom serieimpedansen i nätet ger spänningsfall $\rightarrow$ Spänningen påverkas av belastningen.

## Spänningsreglering
- Förbrukningsvariation under dygnet $\rightarrow$ spänningsvariation
- Spänningsreglering håller spänningen kring nominellt värde

## Kortslutning i elnätet
- Spänningen nära noll i område runt felet
- Felströmmen (överström) detekteras
- Felet kopplas snabbt bort, så att feldrabbat område minimeras
- Felet (i stad oftast grävskopa) avlägsnas
- Bortkopplat nätdel återinkopplas. Manuellt om säkring kopplats bort. Automatiskt efter <1 s (bra vid blixtnedslag) om brytare kopplat bort
Vi kan använda [[överströmsskydd]]

## Elkvalitet
Typer av ofullkomlighet
- Frekvensvariation
- Spänningsdipp
		  - Tillfälligt låg spänning
- Flicker
		- Om spänningsdipp upprepas snabbt. Orsak: svetsning, ljusbågsugn osv
- Transienter
		- Korta avvikelser i spänning. Inte så mycket energi eller skada, ju kortade desto bättre. Halvledaretillverkning kanske känsligast.
- Avbrott
- Övertoner
		- Använder någon elektronisk komponent som bara släpper förbi en bit av sinusvågen/spänningen. T.ex Dimmer, datornätdel osv. 

## Smarta Elnät
- Storskalig, planerbar produktion på transmissionsnivå ersätts av småskaligt variabelt förnybart på distributionsnivå.
- Smarta elnätslösningar = mer automatik
		- styr effektbalansen - var som helst
		- styr ledningsflöden - vid flaskhalsar i nätet

#### Effektbalans och flaskhalsar för smarta elnät
- Effektbalans 
  Förr: låt produktion följa snällt varierande förbrukning Framtid: styr aktiv produktion, förbrukning och batterier för att följa kraftigt varierande förnybar produktion (flexibilitet)
- Flaskhalsar
  Förr: reglera spänning men (över)dimensionera efter worst case för att slippa tänka på andra kapacitetsgränser Framtid: styr (aktiv/reaktiv) produktion, förbrukning och batterier för att gå till men inte överskrida kapacitetsgränser