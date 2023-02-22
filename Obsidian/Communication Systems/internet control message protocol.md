---
tags: [komsys]
aliases: [ICMP]
---
# Internet Control Message Protocol
- Hjälpprotokoll till IP på nätskiktet.
- Utvecklats i viss mån för att kompensera för [[Internetprotokoll|IP]]s saknande av feldetektering, felkorrigering och hjälpfunktioner.
- ICMP fför IPv4 och ICMP för IPv6
- Består av en header på 8 byte och en datadel som är variabel.

## Typer av meddelanden
Två typer: Felmeddelande och förfrågningar

#### Felmeddelanden
- Skickas av routrar eller värddatorer när ett problemn uppstår med ett IP-datagram. Ett felmeddelande skickas alltid till den ursprungliga sändaren av ett IP-datagram. Skickas till den ursprungliga sändaren.
- ICMP har dock inga funktioner för felhantering utan rapporterar endast när ett fel uppstår. Protokollen som använder IP hanterar felet.
- Felmeddelanden innehåller en datadel med den ursprungliga IP-headern plus 8 byte av data i IP-datagrammet.
- Fyra typer av felmeddelanden:
	- Destination Unreachable
	- Source Quench
	- Time exceeded
	- Parameter problem

#### Förfrågningar
- Kan användas för att upptäcka nätproblem. Meddelandet skickas i ett IP-datagram från en användare, värddator eller router till en mottagande router eller värddator. Mottagaren svarar med ett reply.
- Det finns fyra typer av förfrågningar:
	- Echo request
	- Tiimestamp request
	- Adress-mask request
	- Router solicitation

## ICMPv6
Samma syfte som ICMP för IPv4.
- Har även inkluderat funktionerna hos två protokoll som var stjälvständiga i IPv4, [[adress resolution protocol|ARP]] och IGMP.

