---
tags: [num]
aliases: [Newton-Raphson method]
---
# Newton's method
- A numerical for finding the roots of a differentiable function. It is an iterative method that starts with an initial guess and then successively refines the guess by using the tangent line of the function at the current guess to find the next approximation. The method is based on the idea that a good approximation to a root of the function can be obtained by following the tangent line of the function at a nearby point.
- The most famous method for solving [[nonlinear equation|nonlinear systems]].
- It requires that the equation solved to be cast in the form $f(x) = 0$.
- Fast in terms of [[convergence]]
- See [[modified Newton's method]]
![[Pasted image 20230403141854.png]]

## Formula
The iteration for the method is $$x_{k+1}=x_{k} + dx_{k}=x_{k}-\frac{f(x_{k})}{f'(x_{k})}$$
#### Newton's method as [[fixed-point iteration]]
Donate Newton's method $x_{k+1}... = \Phi(x)$
Let $x^{*}$ be a root of f, then clearly $\Phi(x) = x^{*}$
If $x^{*}$ is a single root, i.e., $f'(x^{*}) \neq 0$, then $\Phi'(x^{*}) =0$, as $$\Phi'(x) = \frac{f(x)f''(x)}{(f'(x))^{2}}$$
## Error analysis
$$\lim_{k\to \infty}\frac{e_{k+1}}{e_{k}^{2}} = M >0$$gives **quadratic** [[convergence]].
##### Convergence of the method
![[Pasted image 20230403153517.png]]

## Initial guess
- A drawback with this methos is that it is sensitive to the initial guess $x_{0}$. If $x_{0}$ is too far away from $x^{*}$ the method might fail.
![[Pasted image 20230403153550.png|500]]

## Example
Find the largest root of $16x^{2}-32x+15 = 0$. $$x_{k+1}=\frac{16x^{2}_{k}-32x_{k}+15}{32x_{k}-32} = \frac{16x_{k}^{2}-15}{32x_{k}-32s}$$
![[Pasted image 20230403154018.png|300]]

## Multiple roots 
**Example:**
Find the largest root of $64x^{3}-208x^{2}+220x-75=0$. $$x_{k+1}=x_{k}-\frac{64x_{k}^{3}-208x_{k}^{2}+220x_{k}-75}{192x_{k}^{2}-416x_{k}+220}$$![[Pasted image 20230403154343.png|300]]
No quadratic [[convergence]], because 1.25 is a double root: $f'(1.25)= 0$

##### Multiple roots - definition
![[Pasted image 20230403154447.png]]

## [[Newton's method for systems]]