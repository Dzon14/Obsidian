---
tags: [komsys]
aliases: [kvantisering]
---
# Quantization
 - Uniform quantization for k bits
- $M=2^{k}$ equidistant levels
- Represent sample with k bits
![[Pasted image 20230117162035.png|300]]

- Varje mätvärde avrundas till en specifik amplitudnivå, så att mätvärden i den [[Sampling|samplade]] signalen ej antar vilket värde som helst. 
- Detta för att sedan kunna representera signalen med ett begränsat antal binära tal.
- När ett värde kvantiseras blir det alltid ett kvantiseringsfel. Det beror på hur stort kvantiseringssteg som används (längd mellan amplitudnivåer).