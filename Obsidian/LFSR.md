---
aliases:
  - "linear-feedback shift register"
  - "linear feedback shift register"
  - "linjärt återkopplat skiftregister"
---

Ett linjärt återkopplat skiftregister är en kaskad av [[Minneselement]] vars input är en linjär kombination (ges av [[återkopplingspolynom]])

The input of a Linear-feedback Shift Register is a [[linear function]] of it's previous state. 

![[Pasted image 20211026154648.png|400]]

Ett LFSR med [[återkopplingspolynom]] [[återkopplingspolynom|C(D)]] kan generera sekvensen $s$ endast om den kan skrivas
$$S(D) = \frac{P(D)}{C(D)}$$
där [[P(D)]] har **lägre** grad än [[återkopplingspolynom|C(D)]]. 