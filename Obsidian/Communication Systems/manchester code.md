---
tags: [komsys]
---
# Manchester Code
To get a zero passing in each signal time, split the pulse shape $g(t)$ in two parts and use +/- as amplitude
![[Pasted image 20230117164304.png]]
(0 på nedre flanken)

## Differential Manchester coding
- Use a zero transition at the start to indicate the data.
- For a transmitted 0 the same pulse as previous slot is used, while for a transmitted 1 the inverted pulse is used, i.e. $a_{n-1}(-1)^{x_{n}}$
![[Pasted image 20230117164528.png|500]]
(Changes flank for every transmitted 1 ??)