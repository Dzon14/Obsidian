---
tags: [num]
aliases: [IVP]
---
# Initial value problems for ODEs
- The other problem in [[numerical treatment of ODE]]

Find $y(t)$ that satisfies $$\begin{cases} \begin{align} &y'(t) = f(t,y(t)), \ \ \ 0 < t, \\ &y(0) = \alpha \end{align} \end{cases}$$,where $f$ is a known function, $\alpha$ is the initial value at time $t=0$, and $t$ has no upper limit. 

- A famous instantiation is radioactive decay where $y(t)$ is the radioactive substance  at time $t$ $$\begin{cases} \begin{align} &y'(t) = - \lambda_{d}y(t), \ \ \ 0 < t \\ &y(0) = \alpha \end{align}  \end{cases}$$It has the solution $y(t) = \alpha e^{-\alpha_{d}t}$

## Higher-order IVPs
![[Pasted image 20230511140716.png]]
- Methods of first-order IVPs are applicable to high-order. The trick is to transform the high-order into systems of the first-order. 
Example for high-order above:
We have $y_{1}(t) =v(t)$ and $y_{2}(t) = v'(t)$
And the case above gives $$\begin{align}  &\begin{bmatrix} y'(t) \\ y_{2}'(t) \end{bmatrix} = \begin{bmatrix} y_{2}(t) \\ g(t,y_{1}(t), y_{2}(t)) \end{bmatrix} \\ &\begin{bmatrix} y_{1}(0) \\ y_{2}(0) \end{bmatrix} = \begin{bmatrix} \alpha \\ \beta \end{bmatrix}  \end{align}$$which can be thought as a vector-valued version $$\begin{cases} \begin{align} &\vec{y}'(t) = \vec{f}(t,\vec{y}(t)), \ \ \ 0 < t, \\ &\vec{y}(0) = \vec{\alpha} \end{align} \end{cases}$$
## Discretization of IVPs
- [[Euler's method]]

## Higher-order methods
We have seen that the two [[Euler's method|Euler methods]] both have local truncation errors $\mathcal{O}(h^{2})$ and, so far only experimentally, global truncation errors O(h). Now we display three methods with potentially higher-order truncation errors.
- The implicit trapezoid method
- The implicit midpoint method
- The explicit trapezoid method = the Heun method
![[Pasted image 20230511173107.png]]

#### Example
![[Pasted image 20230511175104.png]]

## Summary
![[Pasted image 20230511173215.png]]

## Example - explicit trapezoid
![[Pasted image 20230511174556.png]]
![[Pasted image 20230511174616.png]]

## The global truncation error
$$G_{i}= \lvert w_{i} - y_{i} \rvert$$
$$\lvert G_{n} \rvert < hcT$$if $\lvert 1+ h \lambda \rvert < 1$
## Local truncation error
$$e_{i+1} = \lvert w_{i+1}-z(t_{i+1}) \rvert$$

## Stability and step-size restriction
Stable if $\lvert 1+ h \lambda \rvert < 1$ otherwise unstable.

## [[stability analysis]]

## Stiff problems
Stiff problems are IVPs for which explicit methods require excessively small step sizes h in relation to the smoothness of the solution. Another way to explain stiffness is to say that attracting solutions are surrounded by fast-changing nearby solutions whose slopes change greatly and cause overshoot for explicit methods with reasonably sized h:s. 
We illustrate with an example:
![[Pasted image 20230512102858.png]]
![[Pasted image 20230512102926.png]]
![[Pasted image 20230512103038.png|500]]

## Methods for nonlinear, stiff, IVPs
A somewhat more difficult IVP of the type $$\begin{cases} \begin{align} &y'(t) = f(t,y(t)), \ \ \ 0 < t \leq T, \\ &y(0) = \alpha \end{align} \end{cases}$$where $f(t,y(t))$ is a nonlinear function and the IVP is mildly stiff. For this, we shall consider IVP methods with iterative methods for nonlinear equations. 

#### Dealing with the nonlinearity in $f$
Still referring to the case equation above, if we use an explicit IVP method, then the nonlinearity in $f(t,y(t))$ is not a problem. We simply evaluate $f(t,u)$ at the points prescribed by the method. The forward [[Euler's method|Euler methods]] $$u_{i+1}= u_{i}+ hf(t_{i},u_{i}), \ \ \ i=0,1,..$$is an example. If we use implicit methods which may be better for computational economy since the IVP is stiff, then a nonlinear equation has to be solved for $u_{i+1}$ at each step. For example, with the backward Euler we need to solve $$u_{i+1}=u_{i}+hf(t_{i+1},u_{i+1}), \ \ \ i=0,1,..$$![[Pasted image 20230516135419.png]]

## [[Runge-Kutta methods]]