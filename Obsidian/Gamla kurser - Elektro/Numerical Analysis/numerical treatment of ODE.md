---
tags: [num]
---
# Numerical treatment of ODEs
- A big part of the last lectures in num course.
We will look at two basic problem types:
- Two-point [[linear boundary value problems]] (BVPs): find $y(x)$ that satisfies $$\begin{cases} \begin{align} &y''(x) = f(x,y(x),y'(x)), \ \ \ a < x < b, \\ &\text{conditions for } y(x) \text{ at } x=a \text{ and } x=b, \end{align} \end{cases}$$where $f$ is a known function and a and b specify the boundary. Problems that are modelled in this way can, for ex, relation to diffusion, conduction and elastic beams.
- [[initial value problems]] (IVPs): find $y(t)$ that satisfies $$\begin{cases} \begin{align} &y'(t) = f(t,y(t)), \ \ a < t, \\ &y(a) = \alpha, \end{align} \end{cases}$$where $f$ is a known function, $\alpha$ is the initial value at time $t=a$, and $t$ has no upper limit. Problems that are modelled in this way can, for ex, relate to mechanical systems and population dynamics. 