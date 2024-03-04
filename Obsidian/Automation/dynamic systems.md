---
tags:
  - automation
---
# Dynamic Systems

## Concentration - tanks in series
![[Pasted image 20240124152232.png|400]]

## Mathematical models
$$d \frac{\vec{x}}{dt} = \vec{A} \cdot \vec{x}(t) + \vec{B} \cdot \vec{u}(t)$$Linear. $\vec{x}$ is a row vector??
**Purpose**: Analysis, e.g. stability, robustness, oscillations, control design 
**Tools**: Analytical, e.g. eigenvalues (poles), zeros, observability, controllability, reachability, Bode-plots, etc., etc
$$d \frac{\vec{x}}{dt}= \vec{f}(\vec{x}, \vec{u}) \text{ or } d \frac{\vec{x}}{dt} = \vec{f}(\vec{x}, \vec{u}, \text{ parameters})$$(nonlinear).
**Purpose:** scientific & detailed understanding 
**Tools:** numerical software and computers, e.g. simulation, Monte-Carlo, sensitivity, uncertainty

- The time scale is an important characterization of a *dynamic system*
- Conservation of mass and energy must always be fulfilled!
- A differential equation: $$\begin{flalign} &\text{the rate of change} = \text{(rate of inflow)} - \text{(rate of outflow)} \\ &+ \text{ (rate generated within system)} - \text{(rate consumed within system)} \end{flalign}$$
## A dynamical system
![[Pasted image 20240124153323.png|500]]

## The state equation
Linear model:
$$\begin{flalign} \frac{dx}{dt} = Ax + Bu \\ y = Cx + Du \end{flalign}$$
D is often 0 and C is often 1. The size of the A and C matrices are the same, same goes for B and D (traditionally).
Non-linear model: 
$$\begin{flalign} \frac{dx}{dt} = f(x,u) \\ y = g(x,u) \end{flalign}$$

## General example
![[Pasted image 20240125154527.png]]
![[Pasted image 20240125154850.png]]
## Example: two systems
![[Pasted image 20240125154945.png]]
## Example: the biochemical reactor (b=0)
![[Pasted image 20240125155241.png]]
![[Pasted image 20240124153650.png]]
This cannot be solved by hand, program is needed
## Linear mechanical spring
$$m \frac{d^{2}z}{dt^{2}} + 2 \sigma \omega \cdot \frac{dz}{dt}+ \omega^{2}z = F$$
$$\begin{flalign} \Rightarrow \frac{dx}{dt} = &Ax + Bu \\ y = &Cx + Du \end{flalign}$$
![[Pasted image 20240125155642.png|700]]
![[Pasted image 20240125155831.png|700]]

## The meaning of eigenvalues
![[Pasted image 20240124161959.png|500]]

## Frequency domain description
- Based on [[Laplacetransform|laplace]] transformations
- External mode description
- Advantage: The $s$ variable can be manipulated by algebraic methods - good for analysi
Transfer function: $$G(s) = \frac{Y(s)}{U(s)} = \vec{C} \cdot (s \vec{I}- \vec{A})^{-1} \cdot \vec{B} + \vec{D}$$
Popular in automatic control theory, system identification etc. $s^{n} = \frac{d^{n}}{dt^{n}}$

## Why does controllers work?
![[Pasted image 20240125160245.png|700]]

## Nonlinear mechanical spring
![[Pasted image 20240124164009.png|500]]
![[Pasted image 20240125160506.png|500]]

## Nonlinearities
![[Pasted image 20240124164036.png]]

## Important non-linearities
- relays
- valves
- friction
- aerodynamics
- alternatic current (ac) motors
- biological systems
How to recognize a non-linear system?
- The **superposition** principle: $$\begin{flalign} u_{1} &= y_{1} \\ u_{2} &= y_{2} \\ u_{1}+u_{2}&= y_{1}+y_{2} \end{flalign}$$

## Non-linear system
![[Pasted image 20240124164344.png|500]]

## Linearisation
![[Pasted image 20240124164402.png|550]]

## Non-linear - unstable solutions
$$\begin{flalign} &\frac{dx_{1}}{dt} = x_{2} + x_{1}^{3} \\ &\frac{dx_{2}}{dt} = - x_{1}+x_{2}^{3} \end{flalign}$$
Equilibrium points 
Stable for **small** deviations from stationarity?
Stable for **large** deviations from stationarity?

## Non-linear - stable solutions
$$\begin{flalign} &\frac{dx_{1}}{dt} = x_{2} - x_{1}^{3} \\ &\frac{dx_{2}}{dt} = - x_{1}-x_{2}^{3} \end{flalign}$$
Equilibrium points 
Stable for **small** deviations from stationarity? 
Stable for **large** deviations from stationarity?

## Time discrete systems
![[Pasted image 20240124164844.png|500]]
![[Pasted image 20240124164907.png|500]]
![[Pasted image 20240124164917.png|500]]

## Summary
- Model examples 
- Linear systems 
	- Superposition principle
	- Meaning of eigenvalues 
	- Laplace transform 
- Nonlinear systems 
	- Stability 
	- Linearisation 
- Time discrete systems
