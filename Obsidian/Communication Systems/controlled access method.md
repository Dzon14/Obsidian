---
tags: [komsys]
aliases: [controlled, controlled accessmetod]
---
# Controlled access method
- en fördefinierad turordning som alla terminaler måste följa. Alla terminaler kommer överens om hur de skickar data $\Rightarrow$ inga kollisioner.
- Polling, Token Ring, Reservation
		  - TDMA/FDMA/CDMA kan ses som controlled eller channelization protocols.

## Polling
- master - slave / primary - secondary
Primär styr accessen till länken och sekundärdatorerna får skicka data endast på begäran från primärdatorn.
Primär skickar POLL och sekundär svarar med att skicka tillbaka data till primärdatorn. Om inget finns att skicka svaras NO POLL och primär går vidare till nästa sekundär

- I polling sker inga kollisioner. Däremot är det en mer komplicerad metod då vi måste ha en primärdator.
![[Pasted image 20230130161220.png]]

## Token ring
Finns en turordning och varje ansluten enhet får en rättvids del av kapaciteten. Terminalerna är kopplade i en ring och fungerar som sändare och mottagare. Terminalen med token får skicka ett [[datapaket|paket]].

## Reservation
Grundprincipen är att en terminal måste reservera kanalen på något sätt innan den får skicka. Sedan skickar terminalen under den tiden den har reserverat kanalen. 
- OM det finns basstation eller annan central enhet som styr över nätet kan det se ut så som att terminalen förs skickar en Request-To-Send till basstation. Stationen svarar med ett Clear-To-Send om kanalen kan reserveras och datan kan skickas. 
- Om det ej finns central enhet: tiden är indelad i ramar och tidsluckor (intervaller). Först i varje intervall kommer en reservations[[datapaket|ram]] där varje terminal kan få flagga i sin tidslucka för att reservera kapacitet. Om flaggan är satt kommer terminalen skicka i sin data i en efterföljande ram. 
![[Pasted image 20230130162049.png|600]]
