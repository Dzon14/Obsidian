---
tags: [komsys]
aliases: [Internet protocol, IP]
---
# Internetprotokoll
- Kan bestå av tre skikt: nät, transport och applikation. 
- På nätnivå finns endast IP, två versioner - 4 och 6.
- På transportnivå finns TCPv4 och TCPv6 och UDP
- På applikationsnivå finns massa olika, t.ex http, SMTP och ftp.config

Ett Internet Protocol (IP) är en standard som används för att skicka och ta emot datapaket över nätverk, inklusive Internet. Varje enhet som är ansluten till Internet eller annat nätverk har en IP-adress som används för att identifiera enheten och möjliggöra kommunikation med andra enheter på nätverket. IP används för att rikta datapaket till rätt mottagare genom att lägga till rätt avsändar- och mottagaradress i pakethuvudet. Det finns olika versioner av IP, inklusive IPv4 och IPv6.

Varje enhet på nätvärket behöver ha en unik IP-adress för att kunna kommunicera med andra enheter på nätverket och utanför nätverket. I ett privat wifi-nätverk tilldelas enheter automatiskt IP adresser genom [[dynamic host configuration protocol|DHCP]].

## IPv4
Består av 34 bitar, skrivs ofta med fyra tal med punkter emellan.  t.ex 128.11.3.31
- Se s. 136 - 141
- Kan fragmenteras

## IPv6
- Fler adresser, består av 128 bitar. 
- Bättre header-format
- funktioner för realtidsdata
- säkerhetsfunktioner
- möjlighet till utökning av protokollet
- Tillåter INTE fragmentering hos en router(dvs routrar kan ej minska storleken), därför viktigt att man inte överstrider [[maximum transmission unit|MTU]]
	- Däremot kan den fragmentera sig själv
Se s.142 - 146

