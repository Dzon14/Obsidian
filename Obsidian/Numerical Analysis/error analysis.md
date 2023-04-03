---
tags: [num]
---
# Error Analysis
A “numerical solution” is different from a “mathematical (closed) solution.” Numerical solutions are approximations to the exact solution.
What error we are willing to tolerate will determine how good our numerical solution is. 

**Absolute error**: $E_{p} = \lvert p - \hat{p} \rvert = \lvert x_{c}-x \rvert$
**Relative error:** $R_{p}= \frac{\lvert p- \hat{p} \rvert}{\lvert p \rvert}= \frac{\lvert x_{c}-x \rvert}{\lvert x \rvert}$ (may be expressed as a percentage)

**Proposition:** $$\frac{\lvert fl(x) - x \rvert}{\lvert x \rvert} \leq \frac{1}{2}\epsilon_{mach}$$
Computers relative *rounding error*: $$\frac{\lvert x_{c}-x \rvert}{\lvert x \rvert} \leq \epsilon_{mach}$$where $\epsilon_{mach} = 2^{-52} \approx 2 \cdot 10^{-16}$

## Types of errors
In num analysis a goal is assessing the accuracy of the results of calculations.
- [[noise]]
- [[round-off error]]
- [[approximation error]]
- [[cancellation error]]

