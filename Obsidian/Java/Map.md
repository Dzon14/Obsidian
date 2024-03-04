---
aliases: [mappar, mappen]
tags: [prog]
---
# Datatypen Map
[[TreeMap]] och [[HashMap]]

nyckel-värde tabell
- nyckeln avbildas (maps) på sitt värde
- Nycklar är unika, men inte värden
![[Pasted image 20211120142113.png|400]]



## Implementering
- Vid implementering ska man lagra nyckel och värde tillsammans.
- En nästlad klass kan användas för att representera ett nyckel-värde-par. Vid sökningar är det nycklarna som jämförs.
- Interfacet Map ärver inte interfacet Collection eller Iterable. Det går alltså inte att iterera direkt över mappen. Däremot kan man iterera över nycklarna, värdena och nyckel-värde-paren.

## Map.Entry
- Ett inre interface som är nästlad i interfacet Map. 
![[Pasted image 20230810112307.png]]
- Operationen map.entrySet returnerar en mängd (Set) av Entry-objekt. D.v.s. en mängd med objekt av en klass som implementerar interfacet Map.Entry.

## Iterering i Map
- Med metoden forEach kan man iterera över alla nyckel-värde-par och ange vad som ska göras i ett lambdauttryck.
![[Pasted image 20230810112515.png|500]]

##### Alternativ iterering
![[Pasted image 20230810113722.png]]
![[Pasted image 20231228131018.png]]

## Interfacet Map i Java
![[Pasted image 20240102124823.png]]

## Använda Map för att räkna frekvenser
![[Pasted image 20240102125209.png]]