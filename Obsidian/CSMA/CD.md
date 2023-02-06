---
aliases: [carrier sens multiple access with collision detection]
tags: [komsys]
---
# CSMA/CD
- Carrier Sense Multiple Access with Collision Detection
Terminalerna är här kopplade till en buss, där alla har tillgång till länken och kan se den data som skickas. Terminaler "lyssnar" på länkenför att veta vad som skickas, dvs de kommer ej fånga upp [[datapaket|paket]] som ej är till dem. Den terminalen det är till fångar upp det och skickar vidare det till sin applikation. 
Signaler går åt båda hållen så går ej att missa information. På ändarna finns enheter som ser till att signalen försvinner och inte reflekteras.
- Finns ingen turordning utan terminalen skickar så fort länken är ledig. 
- Kollisioner kan ske eftersom flera terminaler kan skicka samtidigt då de känner att länken är ledig. 
		- För att upptäcka kollisioner lyssnar terminalen även när den skickar sin data (collision detection). 
- Fördel med denna teknik: om endast en terminal ska skicka så får den hela länkens kapacitet. Även lätt att koppla in en terminal på länken. 
- Nackdel: finns ingen turordning vilket kan ställa till det om det är mycket att sända.
![[Pasted image 20230130164205.png|500]]