---
tags: [prog]
---
# Heap
Ett komplett binärt träd där varje nod innehåller ett element som är <= barnens element
Trådet är fyllt på alla nivåer utom ev. den sista där noderna är samlade till vänsterter
![[Pasted image 20211207132106.png]]

En heap är inte stabil.

## Implementering
![[Pasted image 20211207132146.png]]

### Insättning (offer)
Nya elementet placeras på första lediga plats i vektorn.
- Detta ger rätt form på trädet
- Sedan byten uppåt tills rätt ordning
- Kallas percolate up eller addleaf
- [[Tidskomplexitet]] i värsta fall är O(logn) och i medelfall O(1)

### Hitta minsta (peek)
- Minsta elementet finns på position 0 i vektorn
- [[Tidskomplexitet]] blir O(1)

### Tag bort minsta (poll)
elementet på position 0 ska tas bort
- Ersätt med den som finns på sista plats
- Ger rätt form men roten blir fel i förhållande till barn
- Byt med minsta av barnen tills ordningen är ok.
- Percolate down / addroot
[[Tidskomplexitet]]:
Värstafall för poll är O(log n)
Medelfall O(log n) också



