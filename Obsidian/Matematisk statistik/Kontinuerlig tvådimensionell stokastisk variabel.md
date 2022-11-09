---
tags: [matstat]
---
# Kontinuerlig tvådimensionell stokastisk variabel

**Def:** Om det finns en funktion $f_{X,Y}(x,y)$ sådan att $$P((X,Y) \in A) = \int\limits_{}^{} \int\limits_{A}^{} f_{X,Y}(x,y) \ dx \ dy$$för alla A säges den tvådimensionella [[stokastisk variabel|s.v]] (X,Y) vara kontinuerlig. Funktionen $f_{X,Y}(x,y)$ kallas [[täthetsfunktion|täthetsfunktionen]] för (X,Y).

[[täthetsfunktion|täthetsfunktionen]], även kallas den **simultana** täthetsfunktionen, är den andra partiella derivatan av fördelningsgunktionen enligt $$f_{X,Y}(x,y) = \frac{\partial^{2}F_{X,Y}(x,y)}{\partial x \partial y}$$Den grafiska bilden kan påminna om den övre begränsningsytan hos en sandhög.
![[Pasted image 20221107180713.png|200]]

Om man i täthetsfunktionen integrerar bort den ena variabeln får man marginalfördelningen för den andra. Vi får då [[marginell täthetsfunktion|marginella täthetsfunktionen]] och [[marginell fördelningsfunktion|marginella fördelningsfunktionen]].

**Def:** En tvådimensionell [[stokastisk variabel|s.v]] (X,Y) är likformigt fördelad på området B, om för varje del A av detta område gäller att $$P((X,Y)\in A) = \frac{\text{arean av A}}{\text{arean av B}}$$
### Exempel
![[Pasted image 20221107180909.png]]