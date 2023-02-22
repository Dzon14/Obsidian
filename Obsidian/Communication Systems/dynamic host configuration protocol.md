---
aliases: [DHCP]
tags: [komsys]
---
# Dynamic Host Configuration Protocol
Används av en dator för att få en IP-adress. samt information om närmaste router som kopplar ut mot Internet och DNS-server.

## Process
- Dator startas upp och går igenom bootstrap-process
- Skickar ut ett DHCP DISCOVEr meddelande med broadcast.
- Ansvarig DHCP-server svarar med DHCP OFFER som bland annat innehåller en [[Internetprotokoll|IP]]-adress. 
- Datorn skickar en DHCP REQUEST och begär tillstånd att få använda den adressen
- DHCP-servern svarar med DHCP ACKNOWLEDGEMENT
- Den tilldelade adressen får användas under en begränsad tid - lease time
- När halva lease-tiden löpt ut måste datorn begära en re-lease

## DHCPv6
- Används i IPv6-nät
- Typ samma funktion som DHCP
- Två sätt för en dator att få en IP-adress. 
- Se mer på s.148

