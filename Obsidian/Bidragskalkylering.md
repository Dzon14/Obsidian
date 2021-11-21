---
aliases: [Bidragskalkyl, bidragskalkylen]
---
# Bidragskalkylering
En metod för (produkt)kalkylering som skiljer sig i åt graden av kostnadsfördelning
- Ofullständiga kostnadsfördelning där endast särkostnader beaktas
- Kortsiktiga beslut
		- Ofta gällande pris och volym
		- lönsamhetsbedömningar

## Grundprinciper
- Används vid beslut på kort sikt.
- Fokus på kalkylobjektets (produkt, vara, tjänst) [[Särkostnader och Samkostnader|Särkostnader]] och Täckningsbidrag(TB)
		- TB = Särintäkt - Särkostnader
		- Särintäkten är vanligtvis pris/st
- De gemensamma [[Särkostnader och Samkostnader|samkostnader]] fördelas ej till de olika kalkylobjekten utan behandlas som en klumpsumma när resultaten beräknas
		- Total TäckningsBidrag (TTB) = (summor av alla täckningsbidrag) * Verksamhets Volym (för alla TB)
		- Resultat = TTB - Samkostnader
![[Pasted image 20211115102513.png]]

**Fördelar:**
- Enkel, snabb att använda
		- Inga komplexa fördelningsnycklar (pålägg kostnadsdrivare) att beakta 
- Ger ett minipris (dock farligt då man kan göra fel vid prissättning)
-  Korrekt att använda vid kortsiktiga beslut då (per definition) endast särkostnaderna påverkas

**Nackdelar:**
- Ofullständig kostnadsfördelning till kostnadsbärarna
- Endast korrekt att använda vid kortsiktiga beslut
		- Då kapacitet och andra ramar för verksamheten är givna

Fokus på särkostnader, övriga (sam)kostnader kan beaktas via krav på täckningsbidragens storlek

## Notation och Uttryck
**Notation**
- TB = TäckningsBidrag
- TTB = Totalt TäckningsBidrag
- TG = TäckningsGrad
![[Pasted image 20211115104804.png|550]]

## Bidragskalkylering i Handelsföretag
- Utgår från Bruttovinsten: Försäljning - Varukostnad
	- Varukostnad = Fakturakostnad + Hemtagningskostnad
	- Bruttovinstmarginal = Bruttovinst / Försäljningspriset
	- Pålägg = Bruttovinst / Varukostnad
	![[Pasted image 20211115110220.png|350]]
	
- De gemensamma kostnaderna benämns Rörelsekostnader
		- Subtraheras för att beräkna Nettovinsten (Nettovinst = TTB - Rörelsekostnader)
![[Pasted image 20211115110356.png|350]]


## Bidragskalkylering i Tjänsteföretag
- Tjänsterna benämns ofta: uppdrag, projekt, ärende osv
- Arbetsintensiva tjänsteföretag beräknar ofta särkostnaden för tjänsten med utgångspunkt i arbetets-/lönekostnaden
		- Särkostnaden för tjänsten = Lönekostnad + tjänstespecifika särkostnader
**Exempel:**
![[Pasted image 20211115110835.png]]

## Bidragskalkylering i Tillverkningsföretag
- Handlar ofta om produktvalsproblem och hur resurser och kapacitet bäst ska utnyttjas på kort sikt
- Tre olika situationer som leder till olika **beslutsregler**
		1. Företaget har ledig kapacitet
		2. Företaget utnyttjar hela sin kapacitet och det finns en trång sektor (flaskhals) som begränasar tillverkning och försäljning
		3. Företaget utnyttjar hela sin kapacitet och det finns flera trånga sektorer (flaskhalsar)
- Eftersom besluten är kortsiktiga (kapaciteten antas given för den tidshorisont som beaktas) är målet för företaget att maximera TTB
![[Pasted image 20211115112404.png|400]]

## Faror vid användning av Bidragskalkyler
- Kapacitetslåsning
		- kan låsa kapacitet i order med låga TB (om t.ex en order kommer på tis o sen ons), blir ett tidsperspektiv
- Upprepningsrisk
		- kunden begära lika lågt pris nästa gång
- Spridningsrisk
		- andra kunder vill också ha det lägre priset
- Undantag blir regel
		- låga TB accepteras generellt
- Missuppfattningsrisk
		- samkostnader glöms bort

### Beslut vid Ledig Kapacitet
Beslutsproblem: produktval vid ledig (obegränsad) kapacitet
![[Pasted image 20211115112546.png|450]]
- Om ledig kapacitet -> lönsamt att tillverka och sälja en produkt i om dess täckningsbidrag är positivt. ($TB_i > 0$)
		- Hjälper att täcka samkostnader
		- Det lägsta acceptabla priser på en produkt är det pris som precis täcker produktens särkostnader (TB = 0)

**Exempel Ledig Kapacitet**:

![[Pasted image 20211115173810.png]]

## Beslut vid en trång sektor
Beslutsproblem: Produktval vid en trång sektor
![[Pasted image 20211115174655.png]]

- En optimallösning till problem (P2) är att producera en av produkterna (kan aldrig vara bättre men möjligtvis lika bra att producera flera av produkterna)
- Om bara produkt "i" produceras $=> X_i = \frac{K}{A_i} => TTB = TB_iX_I = TB_I \frac{K}{A_i}$
![[Pasted image 20211115175118.png]]

**Exempel Trång Sektor**

![[Pasted image 20211115175621.png]]

## Beslut vid flera trånga sektorer
![[Pasted image 20211115180818.png]]
- Optimeringsproblemet (P3) har generellt sett ingen lätt identifierbar lösning utan kräver användning av en matematisk optimeringsmetod
		- Om alla samband är linjära kan Linjärprogrammering användas.
		- Linjärprogrammeringens fundamentalsats garanterar att en begränsad optimallösning finns i en tillåten hörnpunktslösning (där minst två begränsningslinjer skär varandra)
- Om problemet endast gäller två produkter kan problemet lösas grafiskt.
- Ett specialfall med en enkel beslutsregel uppstår då samma produkt har högst TB per förbrukad resursenhet i samtliga m resursvillkor. Då ska endast denna produkt produceras och produktionsvolymen bestäms av det villkor som begränsar hårdast. 

**Exempel flera trånga sektorer**

![[Pasted image 20211115183113.png|550]]
![[Pasted image 20211115183135.png|550]]
![[Pasted image 20211115183230.png|550]]

## Beslutsrelevanta kostnader och intäkter
- När bidragskalkylering används vid beslutsproblem är det viktigt att identifiera de kostnader och intäkter som är relevanta för just detta (kortsiktiga) beslut
- Vid val mellan olika handlingsalternativ är det viktigt att komma ihåg
		1. endast framtida kostnader och intäkter som påverkas av beslutet är relevanta (historiska "sunk costs" ska ej beaktas)
		2. endast kostnader och intäkter som skiljer sig mellan handlingsalternativen är relevanta
		3. relevanta Alternativkostnader måste beaktas
	
**Exempel:**

![[Pasted image 20211115225407.png]]

## Sammanfattning av Beslutsregler
![[Pasted image 20211115225506.png|550]]

#indek 