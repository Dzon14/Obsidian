---
alias: [interfacet, interfacen]
---
# Interface

Ett interface kan implementeras av flera olika klasser samtidigt. Alla abstrakta metoder i interfacet måste implementeras i klassen. Fungerar lite som en specifikation

En klass kan implementera flera interface
(men bara ärva från en klass)

Ett interface kan innehålla:
- abstrakta metoder
- konstanter (statiska attribut som är final)
- statiska metoder
- default-metoder

![[Pasted image 20211222144145.png]]

## Funktionellt interface
Ett interface med en enda [[abstrakt metod]]. T.ex har interfacet Comparator bara den abstrakta metoden compare. 
Ett funktionellt interface kan däremot använda flera statiska- och default-metoder. 
#prog 

