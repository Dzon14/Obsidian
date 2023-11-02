---
aliases: [rotort, rotorten]
---
# Root locus
(aliases: rotort, rotorten)
- Shows how the [[Poles]] are translated when a control-loop [[Parameter]] is varied. 
$$Y(s) = \frac{KQ(s)}{P(s)+KQ(s)}R(s)$$
P is a controller with gain K. The close-loop zeros are unaffected by K, the poles will however vary with K.
- The locus for the roots in the characteristic polynom ([[Transfer function]]).
- The close-loop denominator polynom: $$P(s)+KQ(s)$$
- If there are no [[Zeros]], $poles \rightarrow \infty$

### Example - third order system
Transfer function:
$$\frac{Q(s)}{P(s)}= \frac{1}{s(s+1)(s+2)}$$
Closed-loop characteristic equation: $$s(s+1)(s+2)+K = s^{3}+ 3s^{2}+2s + K= 0$$
The pole will lie in different positions depending on K. For example $K = 0$ contributes to poles lying in 0, -1 and 2.
![[Pasted image 20220908154200.png]]
Since two of the poles makes the curve go to the RHP, the [[Stegsvar|step response]] will start to oscillate.
According to
![[Pasted image 20220908154736.png]]
#regler 