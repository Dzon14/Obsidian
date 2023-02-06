---
tags: [dator]
---
# Pipeline

## Fetch-Execute
![[Pasted image 20230131172911.png]]

## MIPS pipeline
Fem steg:
- IF: Instruction fetch från minne
- ID: Instruction decode & register read
- EX: Execute operation eller beräkna adress
- MEM: Access memory operand
- WB: Write result back till register

Det behövs register mellan pipeline steg

## Pipeline diagram vid en viss tidpunkt
![[Pasted image 20230131173316.png]]

## Pipelining
- Fler pipeline steg ger bättre prestanda, men 
		  - Mer overhea att hålla koll på pipeline
		  - Komplexare processorer
		  - Svårt att hålla pipelinen full
- 80486 och Pentium
		- Fem-stegs pipeline för heltal instruktioner
		- Åtta-stegs pipeline för flyttals instruktioner
- PowerPC
		- Fyra-stegs pipeline för heltal
		- Sex-stegs pipeline för flyttal

## Pipeline hazards
- Pipeline hazards är problem som förhindrar att nästa instruktion i programmet (strömmen av instruktioner) exekveras direkt. Man säger att instruktionen fördröjs (stall)
- Typer av pipeline hazards
		- Strukturella hazards
		- Data hazards
		- Kontroll hazards

## Fallgropar
- Pipeline är enkelt, problemen finns i detaljer: t.ex detektera kontroll hazards
- Pipelining är teknologiberoende
- Dålig design av instruktionsuppsättning (ISA) kan göra pipelining svårare
	  - Komplex instruktionsuppsättning
	  - Komplexa adresseringsmöjligheter

## Sammanfattning
- Instruktioner exekveras som en sekvens av steg; t ex Fetch instruction (FI), Decode instruction (DI), Calculate operand address (CO), Fetch operand (FO), Execute instruction (EI) och Write operand (WO) 
- En pipeline består av N steg. Vid ett visst ögonblick kan N instruktioner vara aktiva. Om 6-steg används (FI, DI, CO, FO, EI, WO) kan 6 instruktioner vara aktiva 
- Att hålla piplinen full med instruktioner är svårt pga pipeline hazards. 
	 – Strukturella hazards beror på resurskonflikter. 
	 – Data hazards beror på databeroende mellan instruktioner 
	 – Control hazards beror på hoppinstruktioner
- Hoppinstruktioner påverkar pipelinen mycket. Viktigt att minska penalties 
- Instruktion fetch unit kan känna igen hoppinstruktioner och ta fram vart hoppet går. Genom att snabbt hämta från instruktions cachen och hålla instruktionskön full så kan penalties för ovillkorliga hopp reduceras till noll. För villkorliga hopp är det svårare då man måste veta om hoppet ska tas eller ej 
- Delayed branching är en kompilator-baserad teknik för att minska branch penalty genom att flytta instruktioner till branch delay slot 
- Viktigt för att minska branch penalty är att ha bra branch prediction teknik. Statiska tekniker tar inte hänsyn till exekverings historik, vilket dynamiska tekniker gör 
- Branch history tables används för att lagra utfall av ett hopp och target adress (vart hoppet går