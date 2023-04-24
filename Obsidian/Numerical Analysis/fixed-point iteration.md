---
tags: [num]
---
# Fixed-point iteration
- An iterative method to solve a nonlinear equation in one variable. The method consists of repeatedly applying a fixed-point formula to an initial guess to obtain a sequence of approximations that converges to the exact solution.
- The fixed-point formula is obtained by rearranging the original nonlinear equation such that the solution can be obtained by iterating a function that maps the solution to itself. The iteration is said to have converged when the difference between successive approximations falls below a specified tolerance level.
- All numerical methos [[nonlinear equation|nonlinear equations]] are *iterative* ([[num F4]]) and hopefully inte converges to a true solution $x^{*}$.  (star means limit point of the sequence, it is a fixed point (fixed IF the fixed point iteration is convergent)).
- If a fixed point exists (for continous functions), there might also exist a fixed-point for non-continous functions. 
- We can use [[Lipschitz continous]] function (see this node for contraction .. often comes in exams)

#### Example
consider the [[nonlinear equation]]:
![[Pasted image 20230330144517.png|500]]
(2) : $x=g(x)$
- this fixed point $x^{*}$ gives the equations which is called a *fixed-point iteration*.

## [[convergence]] - Banach's fixed-point theorem
- Conditions for the fixed-point iteration above to converge to a unique $x^{*}$.
- Suppose $g(x)$ is a continous function on some bounded closed interval I
1. If $g(x) \in I$ for all $x \in I$ , then $x^{*} \in I$ exists but may not be unique.
2. If, in addition, $g(x)$ is continously differentiable and $\lvert g'(x) \rvert < 1$ for all $x \in I$, then $x^{*} \in I$ is unique and $x_{n} \rightarrow x^{*}$ as $n \rightarrow \infty$ for all $x_{0} \in I$.

#### How fast does it converge? - Convergence order
**Mean Value Theorem:**
Let f be a continuously differentiable function on the interval $[a,b]$. Then there exists a number c between a and b such that $f'(c) = \frac{(f(b)-f(a))}{(b-a)}$.
OR:
Let g(x) be a continuously differentiable function on an interval $[a, b]$. Then there exists a number $ξ ∈ (a, b)$ such that $$g(b) - g(a) = g'(\xi)(b-a)$$See rest in lecture notes 5.

## Example - fixed-point iteration
![[Pasted image 20230330165002.png]]
as we clearly see - $\phi_{2}$ works but not $\phi_{1}$ - why is this?
- The reason is the *derivative*
![[Pasted image 20230330165138.png]]

## Local convergence / Linear convergence
![[Pasted image 20230330170233.png]]
In other words:
If $$\lim_{i\to \infty}\frac{e_{i+1}}{e_{i}} = S < 1$$where $e_{i}$ is the error at step $i$ and S is the rate.
**Theorem:**
Assume that g is continously differentiable, that $g(r)= r$, and that $S= \lvert g'(r) \rvert < 1$. Then FPI converges linearly with rate S to the fixed point r for initial guesses sufficiently close to r. 

## Example from book 
Using [[bracketing method]]:
![[Pasted image 20230419133557.png]]
![[Pasted image 20230419133609.png]]
![[Pasted image 20230419133618.png]]