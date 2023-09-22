---
tags: [prog]
---
# Stream
- Man kan använda strömmar för att behandla alla element i en samling eller en vektor.

Streams är ofta användbara när du vill utföra operationer på en samling av data, till exempel en lista eller en uppsättning, och du vill inte ändra den ursprungliga datan. Istället skapar du en ström från den ursprungliga datan och tillämpar de olika operationerna på strömmen för att producera önskat resultat.

Här är några vanliga operationer som kan utföras med Streams:

1. `filter`: Väljer element som uppfyller ett visst kriterium.
2. `distinct`: It filters out duplicate elements from the stream 
3. `map`: Omvandlar varje element till ett annat format.
4. `sorted`: Sorterar elementen enligt en viss ordning.
5. `collect`: Samlar resultatet av strömmen till en samling.
6. `reduce`: Utför en binär operation på elementen i strömmen för att producera en aggregatvärde.

Streams gör det möjligt att skriva kod som är mer koncis, lättläst och parallellt behandlingsbar, vilket kan leda till mer effektiv och underhållbar kod.

## Exempel
![[Pasted image 20230813123446.png]]
.forEach - loopar över elementen och utför en operation på dem. 
Detta motsvarar:
![[Pasted image 20230813123904.png|450]]
Men vi abstraherar bort loopen med en ström. 
## Skapa strömmar
![[Pasted image 20230813123538.png]]

## Struktur
![[Pasted image 20230813123613.png]]

## Tentauppgift
![[Pasted image 20230813123059.png|650]]
![[Pasted image 20230813123117.png]]

## Ett annat exempel
![[Pasted image 20230813123947.png]]
