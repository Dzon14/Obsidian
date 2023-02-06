---
tags: [komsys]
aliases: [adresseringen, adress]
---
# Adressering
Varje terminal i nätet har en unik adress. Varje [[datapaket|paket]] som skickas innehåller mottagaradressen, och den noden med rätt adress skickar den vidare till sin applikation.

## Kommunikation över flera nät
Inom ett nät kan varje dator ha en unik adress osm lagras i alla [[vägväljare]] i nätet, ex [[MAC]]-adress. Denna säger dock inget om till vilket nät datorn är ansluten, så det går inte att använda den för att hitta en dator i ett annat nät. För det behöver vi en ytterligare adress, en **nätadress**.
- Nätadressen är global och måste fungera på många olika slags länkar.

# Datorteknik
- Flytta data från ett ställe till ett annat

## Immediate adressering
```c
ADD R4,#3  //R4<-R4+3
```
Operanden finns direkt i instruktionen
![[Pasted image 20230124134750.png|500]]

## Direkt adressering
```C
ADD R4,3  //R4<-R4+[3]
```
Adressen till operanden ligger i instruktionen
![[Pasted image 20230124134804.png|500]]

## Register adressering
```C
ADD R4,R3  //R4<-R4+R3
```
Liknar direkt adressering men istället för att peka ut i minnet så pekas ett register ut.
![[Pasted image 20230124135010.png]]

## Relativ adressering
- Använd t.ex PC för att skapa [[addressering|adress]]. Enbart liten bit finns i instruktion
![[Pasted image 20230124135127.png|500]]