---
aliases: [klasser, klassen]
---
# Klass
- En **klass** är en gruppering av element med lika eller olika sorters datatyper, t ex enkla, arrayer eller andra klasser. Programmeraren bestämmer själv klassens operationer genom att skriva speciella funktioner för klassen.

# C++
## Kod i C++
![[Pasted image 20220815212657.png]]

### Användandet av en metod
När ett objekt skapat i **main** vill använda en av sina metoder så används s k punktnotation:
**objektnamn.metodnamn(ev. parametrar)**

## Kodstruktur
![[Pasted image 20220815212901.png]]

![[Pasted image 20220815212914.png]]

## Uppdelning i flera filer
Datorprogram delas normalt upp i flera filer, s k källkodsfiler. Detta kan göras i program som består av en eller flera funktioner eller i program som består av en eller flera klasser.

Det finns olika skäl för detta:

-   Källkodsfilerna blir återanvändbara, flera filer kan använda samma funktion eller klass.
-   Källkodsfilerna blir mindre och lättare att hantera.
-   Med hjälp av **include**-filer kan man skilja på gränssnitt (= funktionsdeklaration, det som den som använder en funktion behöver veta, dvs hur den anropas) och implementation (själva koden, algoritmen).

### Ex
Om vi delar upp filen **Vara2.cpp** i flera filer blir det såhär:

1.  **Vara.h**  
    innehåller klassdefinition, kallas **header**-fil eller h-fil.
2.  **Vara.cpp**  
    innehåller implementation av metoder.
3.  **testaVara.cpp**  
    innehåller själva huvudprogrammet.
![[Pasted image 20220815213049.png]]
#prog 