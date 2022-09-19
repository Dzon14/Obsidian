---
aliases: [BMS]
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

## [[Architecture of a BMS]] 

## Inherited issues 
- Slave board instability
		- Bad position of connectors and not very reliable
		- Board too long and flexible

## Möte med Gustav
Airs - koppling mellan batteri och bil.
Relä - 

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



