---
alias: [lambdauttrycket, lambdauttrycken]
tags: [prog]
---

# Lambdauttryck
Man skriver innehållet i en metoden direkt i anropet (som argument) och sparar därmed minne och tid. Kompilatorn listar ut vilken metod och alla typer från sammanhanget. 
T.ex:
```java
Arrays.sort(persons, (p1, p2) -> p1.getName().compareTo(p2.getName()));
```
Med detta slipper man skriva en klass för metoden. 
Att använda lambdauttryck funkar endast om det aktuella interfacet är ett funktionellt [[interface]] (endast EN abstrakt metod).
 - Kan även skrivas som ett block, se exempel nedan.
 - Lambdauttryck skapar objekt, d.v.s används istället för new. 

- Att använda lambdauttryck för att skapa objekt fungerar om det aktuella interfacet bara har en abstrakt metod. Alltså ett funktionellt [[interface]] 

## Syntax
![[lambdauttryck1.png|500]]
![[lambdauttryck2.png|500]]

## Multipla attribut i jämförelsen
![[Pasted image 20230809140005.png]]

