---
tags: [dator]
aliases: [OS]
---
# Operativsystem

- Ett program som exekveras på datorn
- Mål för OS
		- hantera hårdvaruresurser i datorsystemet
		- Erhålla tjänster för exekvering av appar (t.ex facebook)
- I princip alla system har någon form av OS.

## Exekvera flera program/Byta program
![[Pasted image 20230117144504.png]]

## Vad gör ett OS?
- Processhantering
- Minneshanterin
- Filsystem
- Drivrutiner
- Nätverk
- Säkerhet
- In och utmatning (I/O)

## Schemaläggare
- Långtidsschemaläggaren (Long-term scheduler)
		- Bestämmer vilka jobb som ska läggas i readykön (queue)
- Mellantidsschemaläggaren (Mid-term scheduler)
		- Bestämmer vilka jobb som ska vara i primärminnet (main) och vilka som ska vara i sekundärminnet
- Korttidsschemaläggaren (Short-term scheduler)
		- Bestämmer vilket jobb som ska exekvera
- Algoritmer:
		- First In First Out, Shortest Hob First, Priority base scheduling......

## Processer och trådar
- En process består av en eller flera trådar (threads) där en tråd är en sekventiell kod som kan exekvera parallellt med andra trådar
- Alla trådar i en process delar data och stack, vilket gör att byte av tråd är mindre kostsamt än byte av process
- Hårdvarustöd:
		- Programräknare och register per tråd
		- Instruktionshämtning (fetch) på trådbasis
		- Kontextbyte (byte av tråd)
- Effektiv exekvering av program med flera trådar (multithreading)
- Effektivt utnyttjande av processorns resurser

## Minneshantering
- Vid multiprogrammering kommer fler olika program finnas i primärminnet. Kostar för mycket tid att flytta program till hårddisk vid kontext byte. 
- Relocation
		- Flytta program och placera dem på andra ställen i minnet. Kunna hantera minnesreferenser och adresser vid omflyttningar.
- Minneskydd (Memory protection)
		- Processer ska inte kunna komma åt minnesarea som tilldelats andra processer utan lov
- Delning 
		- Ibland ska processer kunna dela information och därför komma åt samma delar av minnet.