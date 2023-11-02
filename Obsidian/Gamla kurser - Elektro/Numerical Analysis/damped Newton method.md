---
tags: [num]
---
# Damped Newton Method
- A [[modified Newton's method]]
- Advantage: Converges to the root even if the initial guess is far from the true root or the function is poorly conditioned. 
- Disadvantage: The convergence rate might be slower than the standard method, especially if $\lambda$ is small. 

Uses a step size control (line search)
1. Determine "search direction" $\Delta x_{k} = f'(x_{k})^{-1}f(x_{k})$
2. Choose $s_{k} \in \{ 1, \frac{1}{2}, \frac{1}{4}, ... \}$ such that $$\lvert f(x_{k}-s_{k}\Delta x_{k}) \rvert \leq \left(1- \frac{s_{k}}{2}  \right) \lvert f(x_{k}) \rvert$$
- In general the convergence area is enlargened
- If $s_{k} < 1$, then the method only converges *linearly*
- If $x_{k}$ is close to $x^{*}$, then in general $s_{k} = 1$

## Iteration formula
$$x_{n+1} = x_n - \lambda \cdot \frac{f(x_n)}{f'(x_n)} $$where $\lambda$ is a damping factor between 0 and 1 that controls the step size. A value of close to 1 corresponds to the standard [[Newton's method]]. Smaller $\lambda$ results in smaller step size and more cautios [[convergence]].

## Comparison to [[Newton's method]] (standard)
![[Pasted image 20230403171643.png]]
