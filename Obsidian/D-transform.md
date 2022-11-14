---
tags: [el]
---
En periodisk sekvens har D-transformen 

$$S(D) = \frac{P(D)}{1 + D^T}$$

där [[P(D)]] är D-transformen av de T första symbolerna. (plus ska vara XOR). Varje D motsvarar en tidsförskjutning med en tidsenhet. 

![[Pasted image 20211028110634.png]]
exponenten säger hur många time-instances den har blivit delayed


 # Givet ett S(D) som en division mellan två D-transformer, hur härleda sekvensen?
 
 1. Hitta GCD genom att dividera nämnaren med täljaren (C(D) / P(D)). 
 2. Om GCD != 1
	 1. Dela både täljare och nämnare med GCD
 3. Utför polynomdivisionen 1/C(D), stanna när det endast finns en D-term kvar. Exponenten anger perioden
 4. Dividera täljaren med nämnaren, stanna innan kvoten får högre grad än perioden (tänk på att det börjar på 0, så en period på 8 ger maxterm $D^{7}$)
 5. Kvoten anger nu sekvensen! 
