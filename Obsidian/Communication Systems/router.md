---
aliases: [routing, routern]
tags: [komsys]
---
# Router
- Finner den bästa väg från sändaren till mottagaren för varje enskilt datagram. 

## Uppbyggnad
- Ingångar, utgångar, buffertminnen och en [[vägväljare|vägväljar]]modul (kopplar samman ingångar och utgångar).
- Ingångar och utgångar kallas för interface (gränsnitt) eller port. 

## Forwarding
- Att förflytta datagrammen genom nätet till mottagare på det sätt som för ögonblicket är det bästa. 
- Data ankommer till router och tas emot som ramar enlingt [[länkprotokoll]]. Ramens kontrollinfo skalas bort och datan skickas vidare till vägväljarmodulen som beräknad bästa väg. Vid utgången får den en ny ram med kontrollinfo och sckickas vidare.

## Routing
Routern måste veta vilken väg som leder till datagrammets destination. Finns ofta flera vägar, så gäller att välja bästa. Routern behöver info om hur nätet ser ut och vilka tillgängliga vägar som finns (även status på dessa) - detta kallas för routing. 
- Processen routing är global och gemensamm för alla routrar i ett nät.

## Prestanda
Flödet av datagram beror på processorderrns last. I köer drabbas fördröjning (delay, latency). Jitter kan även ett problem, som är variation i fördröjning. 

## Grundprinciper för routing
Routing kan implementeras på två sätt: centraliserat och distribuerat.
**Centraliserad routing**:
Alla routrar rapporterar status på länkar de är anslutna till och vilka grannar de har till en central enhet. Centralenheten beräknar sedan bästa väg.
**Distribuerad routing**:
Varje router räknar ut själv bästa väg från sig själv till alla destinationer i routingdomänet.

- Routing och forwardtabeller:
		  - varje routingprocess har en uppsättning routingtabeller och en router kand delta i flera routingprocesser samtidigt

##### [[routingprotokoll]]

## Grafteori för routing-algoritmer
- [[Bellman-Ford]]
- [[Dikjstras algoritm]]