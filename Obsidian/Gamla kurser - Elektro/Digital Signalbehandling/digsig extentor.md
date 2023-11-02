---
tags: [el]
---
# DigSig Extentor 

- [x] [[2022-10]]
- [x] [[2022-08]]
- [x] [[2022-04]]
- [x] [[2021-10]]


## Filters - pole-zero diagram
läs på om hur pole-zero-diagram ser ut för olika filter:
- When z is on the unit circle the frequency response acts like a filter. 
- LP-filter: Pole near unit circle (i.e. 0.9) and zero at -1. (mangitude peak at w=0, lets through low-frequency components, while the zero attenuates at high components...)
- HP-filter: The other way around, zero on unit circle at w=0, and pole at negative side close to the unit circle.


#### Pole-zero diagram
- Zeros will attenuate near unit circle where magnitude gets 0 if it's on the unit circle. (The frequence calculated for zeros will be the lowest point in magnitude) The phase however will increase for a zero where if it's on the unit circle it will be a positive phase jump. 
- Poles will amplify near and be at peak at its closest to the unit circle. The phase will decrease (a negative slope), with higher change the close it is to the unit circle. 
If X(z) we have poles on the unit circle, the unit circle is  
not included in the ROC ... and the DTFT does not exist
**How does these affect the impulse response?**
They determine the frequency response which in turn affect the impulse response. For example, poles near the unit circle can cause oscillations in the impulse response, while zeros at certain frequencies can cause nulls in the frequency response.
The magnitude of freq response can affect the amplitude of the impulse response. 
The phase of the frequency response can affect the timing of the impulse response. For example, a phase shift of 90 degrees at a certain frequency will cause a delay of a quarter of a period in the corresponding component of the impulse response
**How do I find the system diagram?**
Given the graph of the pole-zero plot, frequency response (magnitude and phase separately), and impulse response, it is possible to determine the corresponding system diagram with delays as follows:
1.  Pole-zero plot: From the pole-zero plot, we can determine the order of the system (number of poles and zeros, i.e if 2 zeros and 2 poles, order is 2 or if 4 zeros and 2 poles the order is 2, difference), as well as their locations in the complex plane. If there are poles or zeros on the unit circle, then the system is marginally stable.
2.  Frequency response: The magnitude and phase response of the system can be used to determine the gain and phase shift at different frequencies. This information can be used to construct a block diagram of the system with delay blocks, gain blocks, and summing junctions.
3.  Impulse response: The impulse response of the system can be used to determine the response of the system to an input signal. This information can be used to verify the block diagram and determine the system's time-domain behavior.
Own thought: If either zero or pole is at origin, the system is "one-sided" (not directform II?) where if zeros at origin delay modules are below (see exam 2016)


## Linear phase 
![[Pasted image 20230410154645.png|400]]
![[Pasted image 20230407180132.png]]
![[Pasted image 20230407180516.png|500]]
![[Pasted image 20230407180801.png]]

## Annat
**Stegsvar:**
stegsvar är utsignalen om insignalen är ett steg ($u(n)$), alltså $s(n) = h(n) * u(n)$, här är det nog oftast lättast att Z-transformera båda och sedan multiplicera och inversa.

**Lattice:**
Se slutet av formelsamling. Lika många m som latticeparametrar? där sista är H(z)?
![[Pasted image 20230409161957.png|600]]

**Cirkulär faltning:**
Om ena sekvensen (eller båda) är mindre än vad det är modulo, får man förlänga med nollor (sist) och indexera om så nollor är i mitten (bara sett i en uppgift att man indexerar om, tror ej man ska göra det generellt)??  (zero padding)
Om ena sekvensen (eller båda) är längre än vad det är modulo, måste man trunkera, alltså ta bort från längst till höger. 
- Vi kan få cirkulär $\rightarrow$ linjär faltning genom att zero-padda BÅDA sekvenserna med M+L-1 
- Vi kan också transformera (DFT) först och multiplicera sen inversa

**How to improve DSP implementation**
![[Pasted image 20230410115829.png]]

**Why DFT?**
![[Pasted image 20230410120039.png]]
![[Pasted image 20230410120158.png]]

**Z-transform:**
Kom ihåg att skriva om så det blir korrekt. exempelvis för $x_{1}(n)$ behöver vi skriva om bråket som $\frac{1}{2} \cdot \frac{1}{2^{n-1}}$.
![[Pasted image 20230410143822.png]]