---
tags: [dator]
---
# Maskininstruktioner
![[Pasted image 20230124133138.png|350]]

- Den ska bestämma
		- Typ av instruktioner (operander och operationer)
		- Antal adresser
		- Instruktionsformat

- Typer av instruktioner:
		- Aritmetiska och logiska (ALU)
		- Dataöverföring(adresseringsformat)
		- Hopp
		- In- och utmatning

# Typer av instruktioner

## Aritmetiska och logiska (ALU)

Aritmetiska operationer:
- Addition och subraktion. Två källor och en destination
add a, b, c (a = b+c)
- Alla aritmetiska funktioner följer detta mönster
- C kod: a=b+c+d; kompileras till:
  ADD a, b, c
  ADD a, a, d
![[Pasted image 20230124134211.png|250]]
- [[Register]] kan användas för att minska minnesaccesser i en operation (ADD r1, b, c .....)

## Dataöverföring ([[adressering]])
- Flytta data från ett ställe till ett annat

## Hopp och subrutiner/Hoppinstruktion
- Nästa instruktion är normalt nästa i programmet: PC=PC+1
- För att göra hopp till annan del av kod, ladda programräknare med nytt värde: PC = dit hopp ska sek.
Två typer av hopp
- Ovillkorliga hopp:
		- Programräknaren får nytt värde och hämtar nästa instruktion på nytt ställe
- Villkorliga hopp
		- Villkor bestäms av flaggor i statusregister. 
		- Flaggor: N,Z,V,C

## Inmatning/utmatning (I/O)
- Minnesmappad och isolerad I/O. 
- lkdcx,vdvfx

# Instruktionsformat
Fixed eller flexibelt
- Alla instruktioner är lika långa $\rightarrow$ enklare kontrollenhet
- Instruktioner olika längd $\rightarrow$ flexibilitet, adressrymd
