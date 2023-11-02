---
aliases: [BMS]
tags: [lfs]
---

# Battery Management System
The BMS is responsible for ensuring the safety and reliability of the battery pack. 
- Monitor voltages, temperature and current
- Protect cells from deep discharge and overcharge 
- Balances the cells to keep voltage and a healthy state of charge. 
- Protects the inverter and intermediate high voltage components by controlling the pre-charge and discharge circuitry.
- Able to open shutdown circuit to shut down the car if inconsistencies are detected. **Important** for not destroying anything.
		- Isolation monitoring device
		- Voltage/temperature/current

## Begrepp
Airs - koppling mellan batteri och bil.
Relä - 

## [[Architecture of a BMS]] 

## Inherited issues 
- Slave board instability
		- Bad position of connectors and not very reliable
		- Board too long and flexible

## Möte med Gustav

### Tips
- Ladda ur +sidan först och sedan -, mellan batteri och TS. 
- Octopart (hemsida)
- JLC PCB (Kommer med fastlödda standardkomponenter/delmontering)
- Tillverkning ca 1 månad
- Organisera väl
- Beställa innan jul om det går? (MMAB inte så glad på det)
- Ca 2 veckor för tillverkning av kort
- Lägg fokus på regler tidigt, för att ej göra fel på kortet. 
- Raspberry Pi kan ej jobba i realtid - så kanske inte lämpligt? 
- Mest kraft/tid på slavkorten - då de är opålitliga? Ta bort regioner som ej behövs och möjligtvis göra de mindre. 
- Bättre interface
- Använda datalog
- Koppla en Pi till arduinon? 
- Prioritera testning - gör den **pålitlig**
- Få feedback på varje steg (av professor, eller typ Johannes?)

### Altium
- Bli bekväm med programmet, göra något annat litet projekt först kanske?
- Lära sig shortcuts
- Phil Selman? på yt
- Synca workspace (som git)
- Boka tid med en professor (Christoffer?) för att få feedback på kortet osv. 

### Länkar


## Möte med Johannes

#### Problem
1. Voltage indicator (active light) - se till att komponenter klarar strömregulatorn ba..
2. Byta ut slavkorten, kan rätt lätt gå sönder och instabila. Vid byte kommer även kontaktbekymret för de gamla slavkorten elimineras. Där är kontakterna dåliga och skulle behövas nya (Molex microfit). Byta  connectors till sensorkorten
- Implementera DC/DC (Joel)
- Dålig algoritm. Letar t.ex upp för höga spänningar, låter ej ladda ur två celler bredvid varandra samtidigt vid balansering
- Balansering allmänt dålig, tar för lång tid, borde fixas.
- Balanseringen atm består av resistanser som laddar ut batteriet - dessa är troligtvis för stora. 
- Koden dålig generellt. Väldigt rörig och oläsbar. Många onödiga uppdelningar i filer. 
- En fil för varje "state"?
- Laddningsström är hårdkodad - borde nog ändras xD 
- Laddning körs med konstant ström tills spänningen blir för stor, blir alltså aldrig fullt laddat.
- **OM** optokopplare ska användas, fixa den. 
- Designa om segmenten (så man ej får stötar och det blir mindre) - Beslut som tas tillsammans med Powertrain
- Byta ut USB-kabel i accupacket - tillsammans med Robert (accumulator electronics)
- "Städa" i CAD

#### Tips
- Använd ej kondensator på CAN
- Skicka kretskort till tillverkare rätt tidigt i december
- Kolla löpande att saker funkar (Altium osv)
- Kolla i dokumentet "necessary compromise fixes"

#### Annat
- Om shutdown circuit triggas utanför BMSen så kommer det gå till "standby" istället för "shutdown"-läge.

## Martin
- Alla sladdar på samma sida (can kontakten som går under)
- Fästa sladdar (ISOspi) bättre? sitter rätt löst. Ha något slags lås (crimplock) (Joel har koll på detta). Ha samma kontakter (typ molex)
Se: Compilation of problems/improvment potensials from HV22

