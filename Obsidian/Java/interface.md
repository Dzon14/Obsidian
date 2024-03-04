---
alias: [interfacet, interfacen]
tags: [prog]
---
# Interface

Ett interface kan implementeras av flera olika klasser samtidigt. Alla abstrakta metoder i interfacet måste implementeras i klassen. Fungerar lite som en specifikation

En klass kan implementera flera interface (men bara ärva från en klass):
![[Pasted image 20230808210429.png]]

- Interface betyder gränssnitt.
- Interfacet fungerar som kontrakt eller specifikation. 
- En klass som implementerar interfacet måste implementera alla abstrakta metoder i interfacet. 
- Annars går klassen inte att kompilera. 
- Flera olika klasser kan implementera samma interface.

Ett interface kan innehålla:
- abstrakta metoder
- konstanter (statiska attribut som är final)
- statiska metoder
- default-metoder - innehåller metodkropp

![[Pasted image 20211222144145.png]]

## Funktionellt interface
Ett interface med en enda [[abstrakt metod]]. T.ex har interfacet Comparator bara den abstrakta metoden compare. Därför kan man använda [[Lambdauttryck]] för comparator.
Ett funktionellt interface kan däremot använda flera statiska- och default-metoder. 

## Några interface
![[Pasted image 20230808204003.png]] 

![[Pasted image 20231228130838.png]]