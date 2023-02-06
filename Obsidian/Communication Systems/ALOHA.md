---
tags: [komsys]
aliases: [ALOHANET]
---
# ALOHA
- 1970
- En enkel [[accessmetod]]. 
En terminal börjar sända så fort den har data att skicka. Sedan väntar den på att få en ACK (bekräftelse) från centraldatorn på den andra radiokanalen. Kollisioner kan ske iom ingen kontroll sker innan de skickar data. En terminal vet att det har blivit kollision om den ej får en ACK inom en viss tid $\Rightarrow$ den skickar datan igen. Att det lätt blir kollisioner är dock en brist med ALOHA då utnyttjandet av länken blir låg.

## Slotted ALOHA
En ny version (1975) av ALOHA för att förbättra prestandan.
Tiden delas in i intervaller som motsvarar transmissionstiden för ett [[datapaket]]. En central klocka används sedan för att synkronisera alla terminaler. Terminalen får endast skicka ett paket i början av varje tidsintervall. 
$\Rightarrow$ I varje tidsinterball är det antingen tyst, skickas paket eller kollision. Detta ökar det maximala uttnytjandet av länken med en fördubbling.


