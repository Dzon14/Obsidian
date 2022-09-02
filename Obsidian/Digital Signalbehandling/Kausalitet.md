---
aliases: [kasual, kausalt, causality, casual]
---
# Kausalitet
A system is said to be causal if the output at any time only depends on the current and past inputs

### Discrete
Assume we have an LTI system with impulse reponse h(n) and $y(n) = x(n) \ast h(n)$,
What is the requirement on the impulse response for such an LTI system to be casual?

$$y(n) \ast h(n) = \sum_{k = - \infty}^{\infty} x(k) h(n-k)$$
for causality h(n-k) must be zero for all k > n (which is the same as n - k < 0) or equivalently

**Def:**
An LTI system is only causal if its impulse response $h(n)$ fulfilts $$h(n) = 0, \ for \ all \ n < 0$$ ![[Pasted image 20220831092636.png|300]]

#el 