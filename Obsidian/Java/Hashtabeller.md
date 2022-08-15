---
aliases: [hashtabell]
---

# Hashtabell
- En [[Datastruktur]] som är snabb att söka i
- [[Tidskomplexitet]] för sökning, insättning och borttagning är O(1) i medelfall
- I praktiken är en hashtabell snabbare än ett balanserat binärt sökträd
- Passar bra för att implementera [[Set|mängd]] och [[Map|mappar]]
- Använder [[nyckel]]

SE [[HashSet]] och [[HashMap]]

## Implementering
- Elementen sprids ut i en vektor
- Söknyckeln måste översättas till ett index i vektorn. Sker i två steg:
1. Hashfunktionen avbildar nyckeln på heltal (hashkod)
2. Hashkoden måste skalas ned så att den passar som index i vektorn (t.ex hashkod mod vektorns storlek)

Hashfunktionen ska översätta nyckeln till ett heltal
		- Om nyckeln är ett heltal kan hashkoden vara talet själv.
		- 
![[Pasted image 20220809135409.png]]

## Metoden hashCode i Java
- I klassen Object finns metoden hashCode som översätter ett objekt till ett heltal. 
- Metoden hashCode är skuggad i Javas klass String, Integer så att lika objekt ej avbildas på samma heltal.
- Man måste [[Skuggning|skugga]] hashCode och equals i den klass vars objekt ska fungera som nyckel i Javas hashtabellsklasser
- hashCode och equals anropas inuti hashtabellsklassen

## Kollisioner
- Kollisioner (olika nycklar får samma index) är oundvikligt men kan hanteras.
1. Metoden hashcode kan returnera samma värde för två olika nycklar.
2. Och även om hashcode returnerat olika värde kan flera element hamna på samma index (key.hashCode() % table.length, ger index i en vektor tabell)

En bra hashfunktion:
- Välj en bra hashfunktion som påverkas av alla delar av nyckeln och sprider elementen över hela tabellen
- Vektorn får inte vara för liten

## Sluten hashtabell
En vektor används.
Linjär teknik: 
		- man sätter in ett element som kolliderar med ett annat första lediga plats efter den där det skulle ha hamnat om ingen kollision inträffat
		- Tabellen betraktas som cirkulär, index 0 kommer alltså efter tableSize - 1.
		- Sökning efter ett element börjar på den plats elementets framräknade index anger och fortsätter sen framåt.
		
Ett problem vid sluten hashtabell med linjär kollisiontsteknik är borttagningar. Det kan leda till problem vid sökningar om nyckeln tagits bort på en plats innan den sökta. Lösning är att markera det borttagna elementet ( med en bokstav eller liknande)
**Fler problem med linjär teknik:**
- primär klustring, om fler objekt kolldierar kommer de att ligga i ett kluster kring platsen
- Stora kluster ger långsam sökning
		
Kvadratisk teknik:
- Bättre teknik för hantering av kollisioner
- Först provas nästa plats, sedan platsen 4 steg fram, sedan 9 osv.  (tabellen används även här cirkulärt)
- Undiker primär klustring.
**Problem vid kvadratisk kollisionsteknik:**
- Inte alltid säkert att man hittar ledig plats även om det finns

## Öppen hashtabell
Elementen i tabellen är listor
Ex:
![[Pasted image 20211125121546.png|500]]
Notera att talet som är sist i följen ska vara längst till vänster i listan.

[[HashSet]] och [[HashMap]] använder öppen hashtabell.

## [[Tidskomplexitet]]
- Sökning (och instättn. och borttagn.) i en hashtabell innebär
		-  beräkning av index
		-  Sökning bland kolliderande nycklar
- I värsta fall är det O(n), där n är antalet element som finns insatta i tabellen.
- Medelfall: O(1)

## Fyllnadsgrad
- Ett mått på hur fylld tabellen är.
- Fyllnadsgrad = antal insatta element / vektorns storlek
- Ett lämpligt val är 0.75, man vill inte fylla den för mke.

### Rehashing
Om tabellen blir för fylld.
Då måste man bygga om tabellen:
	- Skapa en dubbelt så stor tabell
	Sätt in alla element i den nya tabellen
	
	
## [[Skuggning]] av hashCode och equals
![[Pasted image 20220809140055.png|600]]



#prog 