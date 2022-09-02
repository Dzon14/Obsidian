---
aliases: [state-space form, state-space]
---
# State-space model
With a balance equation, the process can be described by means of a differential equation. In some cases these equations are linear but they are mostly non-linear. 


- First step in this model is to [[Linearization|linearize]]

x and f are vectors which allows us to write the equation system in the compaft form:
$\dot{x} = f(x,u)$
$y = g(x,u)$

state space description:
$\begin{cases} \dot{x} = Ax + Bu \\ y = Cx + Du \end{cases}$
where,
A - nxn matrix
B - nx1 matrix
C - 1xn matrix
D - 1x1 matrix

- Eg. if we have a second order diff.eq. we have n = 2 and we need two state variables to write the equation in space form as following:
$\begin{cases} x_1 = y \\ x_{2} = \dot{y} \end{cases}$

**Good:**
- Turns things into linear algebra. 
		- computations
		- MIMO (Multiple Input Multiple Output)
**Bad:**
- Interconnection is messy (at least by hand, computer doesn't care xD)
- No delays

#regler 