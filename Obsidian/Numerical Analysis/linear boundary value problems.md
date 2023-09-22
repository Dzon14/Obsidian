---
tags: [num]
aliases: [BVP]
---
# Linear boundary value problems
- A finite difference method
- A type of differential equation problem where the solution is sought in a specified interval and the values of the solution and its derivative(s) are prescribed at the boundary points of the interval. The term "linear" refers to the fact that the differential equation is linear in the unknown function and its derivatives.
- Boundary value problems are a general class of differential equations that involve finding a solution to a differential equation subject to boundary conditions, which are specified at the endpoints of the interval on which the solution is defined. Linear BVPs are a specific type of boundary value problem where the differential equation is linear.

## [[numerical treatment of ODE]]

- Two-point [[linear boundary value problems]] (BVPs): find $y(x)$ that satisfies $$\begin{cases} \begin{align} &y''(x) = f(x,y(x),y'(x)), \ \ \ a < x < b, \\ &\text{conditions for } y(x) \text{ at } x=a \text{ and } x=b, \end{align} \end{cases}$$where $f$ is a known function and a and b specify the boundary. Problems that are modelled in this way can, for ex, relation to diffusion, conduction and elastic beams.

## Boundary conditions for BVPs
Using equation above, there are at least three common types of of boundary conditions (BCs) that can hold at a and/or at b.
- **Dirichlets BCs**, in which the value of the solution $y$ is specified.
- **Neumann BCs**, in which the value of the derivative $y'$ is specified
- **Robin BCs**, in which a linear combination of $y$ and $y'$ is specified.
Combinations of these BCs, so-called *mixed* BCs, are also possible. It can be illustrated in the figure below that relates to stationary diffusion. 
![[Pasted image 20230504164658.png|500]]
A water pipe along x-axis is connected at $x=a$ to a big mixing tank with clean water. There is polluted water flowing with constant negative velocity $v$ in the pipe and the pollutant cocentration $c(x)$ varies with $x$. 
![[Pasted image 20230504165314.png]]

## The pin fin
- Another example that leads to two-point BVPs.
A pin fin is a cooling device that experiences energy transfer by conduction within its boundaries and by convection between its boundaries and the surrounding air. We seek the temperature $T(x)$ in the pin fin shown in Figure 2, and start with deriving an ODE. Input quantities to this problem are: the length $L$ and the cross section radius $r(x)$ of the fin, the temperature $T_{0}$ of the surface where the fin is attached, the temperature $T_{out}$ of the surrounding air, the thermal conductivity $k$ of the fin, and the convection heat transfer coefficient $h_{c}$
![[Pasted image 20230504165515.png|500]]
![[Pasted image 20230504165707.png]]

## Translation table - discretization
The basic idea is to replace derivatives with discrete approximations and to evaluate on a grid to get a system of equations. For this, we return to [[num F10]] to translate continous quantities to discrete counterparts
![[Pasted image 20230504171125.png]]
- h är avstånd mellan punkterna
## Example 
![[Pasted image 20230504172103.png]]
![[Pasted image 20230504172120.png]]
