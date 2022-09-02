# Relation between poles and step response

**Initial value theorem:**
$$ f(0) = \lim_{t\to0} f(t) = \lim_{s\to\infty} sF(s)$$
**Final value theorem:**
$$\lim_{t\to\infty} f(t)= \lim_{s\to0} sF(s)$$
- F is the signal being investigated.
- When we have systems with RHP zeroes, the system is going in the "wrong way" before going the right way. Hence, unstable.
- $sF(s)$ must be stable for the **Final value theorem**. 
**(Göra egen sida för dessa?)**


Factorise the denominator of the transfer function, find the poles. Plot poles in the s-plane. The pole will affect the time-plane behaviour. 
Stable if left side of the s-plane.

- Stable if $\zeta > 0$
- Unstable if $\zeta < 0$
- Marginable stable if $\zeta = 0$

![[Pasted image 20220831135452.png]]

#regler