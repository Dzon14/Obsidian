---
aliases: [domain, domäner, domains]
tags: [komsys]
---
# Domän
[[Internet]] delas in i ett antal domäner, där varje domän får sin egen kod. Dessa kan ha ett antal underdomäner (subdomain).
- Man kan se det som ett upp o ned vänt [[träd]] där det är en rotdomän högst upp
- Varje nod i trädet har en så kallad label, som är en text med maximalt 63 tecken. 
- Alla underdomäner till en domän måste ha en unik labek för sammanblandning. 
- Varje nod har också ett domännamn som är en sekvens av lablar, separerade med punkter.'

## Rotdomän
- Finns två typer av domäner: Geografiska och organisatoriska. Varje land har en egen (Sverige - se).
- Organisatoriska är t.ex edu, com, org osv

## Från namn till [[addressering|adress]] 
Översättningen fråmn klartextadress till [[Internetprotokoll|IP]]-adress sker i [[domain name system|DNS]]-servrar. Det skall finnas en [[domain name system|DNS]]-server i varje domän som ska kunna svara på förfrågningar från värddatorer och routrar.
- Den kan även översätta åt andra hållet, från [[addressering|adress]] till namn. 

## Dynamic Domain Name Sysytem (DDNS)
- Här sker uppdateringar av adresser och domäner genom att [[dynamic host configuration protocol|DHCP]] i den aktuella domänen skickar ett meddelande till sin primära [[domain name system|DNS]]-server.