---
aliases: [priorityqueue]
---

# Prioritetskö
En [[Abstrakt datatyp]]. De viktiga först
Borttagning avser alltid med prioriterade (minsta)
Ska innehålla:
	- offer - sätta in element
	- peek - ta reda på det högst prioriterade elementet (minsta)
	- poll - ta bort det högst prioriterade elementet (minsta)

- Elementet innehåller ett eller flera attribut som modellerar elementets prioriter. 
- Dubletter är tillåtna

Kan användas vid [[sortering]] - heapsort

En prioritetskö är stabil om element med lika prioritet plockas ut i samma ordning som de sattes in

![[Pasted image 20211208105230.png|400]]

## Implementering
- Enkellänkad lista
		- sorterad - insättning långsam
		- osorterad - sökning och borttagning långsam
Nackdel: Vissa operationer blir långsamma O(n)
- Heap

Finns specialfall när prioritetskö inte implementeras med [[heap]]. 

### [[Heap]]

### klassen PriorityQueue
Det finns flera konstruktorer, bl.a
1. PriorityQueue()
		- Förutsätter att elementen implementerar Comparable, annars genereras ClassCastException. Inuti PriorityQueue jämförs elementen med compareTo
2. PriorityQueue(Comparator< ? super E> c)
		-Elementen jämförs med hjälp av comparator c
		- Kan använda lambdauttryck här

<<<<<<< Updated upstream
## Sortering med hjälp av en prioritetskö (Heapsort, mha Heapify)
Man kan sortera en vektor med strängar a, med hjälp av en heap. Detta kommer dock ge stor [[Tidskomplexitet]] och mycket arbetskraft.
=======
## [[Sortering]] med hjälp av en prioritetskö (Heapsort, mha Heapify)
Man kan sortera en vektor med strängar a, med hjälp av en heap. Detta kommer dock ge stor tidskomplexitet och mycket arbetskraft.
>>>>>>> Stashed changesO
Därför ska man **sortera direkt i vektorn**:
1. Bygg om den osorterade vektorn till en heap (utan användning av extern prioritetskö).  (maxheap om det ska vara växande ordning)
2. Gör succesiva poll. Utnyttja de lediga platser i vektorn som uppstår vid poll för att lagra det sorterade resultatet. Blir O(logn)
Detta kallas Heapify (eller buildheap), där man bygger om det träd vektorn representerar till en heap, nedifrån och upp.

#prog 
