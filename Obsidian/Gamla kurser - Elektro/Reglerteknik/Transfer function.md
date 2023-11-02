---
aliases: [överföringsfunktion, överföringsfunktionen]
tags: [regler]
---
# Transfer function
- Laplace domain

$Y(s) = G(s)U(s)$ , 
where $G(s)$ is the model (transfer function of the system), $Y(s)$ is [[Laplacetransform|Laplace transformation]] of the output ($\mathcal{L}$(y(t)) and $U(s)$ is the laplace transform of the input 

- Poles are found in the denominator of the transfer function. 

**Good:**
- Turns things into complex analysis.
- Good for interconnection. Turns any interconnection you want to do into linear algebra. For instance, when using two process steps, you just multiply them (G1 multiplied by G2, if they are the steps)
- Handles delays

**Bad:**
- MIMO mess
- Computation is hard (should use space-state here instead)

#### One-sided [[Laplacetransform|Laplace transformation]]
![[Pasted image 20220830164036.png]]

$$\mathcal{L}(q(t))(s) = F(s) = \int_{0}^{\infty} q(t)e^{-st} \, dt$$


### The relation between State-space and Transfer function
Often one wants to alternate between working with the state space description and the transfer function. Therefore it is essential to be able to transit between these descriptions.

![[Pasted image 20220830220240.png]]
![[Pasted image 20220830220249.png]]

## Properties
**What can T.F.s tell us?**
- Interconnection
- Capture key behaviour
		- stable vs unstable
		- long vs short term
		- oscillations

Inputs can vary, see [[Impulssvar]] & [[Stegsvar]]

Factorise the denominator of the transfer function, find the poles. Plot poles in the s-plane. The pole will affect the time-plane behaviour. 
Stable if left side of the s-plane

- [[stable]] if $\zeta > 0$
- Unstable if $\zeta < 0$
- Marginable stable if $\zeta = 0$

## Example

Dynamical system, a car. 

$$F = m \frac{d^{2}}{dt^{2}} + k(\frac{d}{dt}q + (\frac{d}{dt}q)^{2})$$
Describes the dynamics of the car (above).

$\begin{cases} \frac{dF}{dt} = F + u \\ y = q \end{cases}$
u is "pressing the pedal", whereas the first eq. is the force dynamics of the engine.
in the lower, $y = q = x_{1}$

![[Pasted image 20220901152506.png|400]]
The car model has a input F and an output q.
We have to linearise before state-space of TF. Find stationary points for the linearisation!

In general, when linearising, put all the derivations of equations = 0.
**Linearise:**
$$\begin{align} \begin{cases}F = 0 \\ x = \begin{pmatrix} q \\ \frac{d}{dt}q \end{pmatrix} = \begin{pmatrix} x_{1}\\ x_2 \end{pmatrix} \end{cases} \\ \\ \\ \begin{cases}\frac{d}{dt}x_{2}= \frac{-k}{m}(x_{2}+ x_{2}^{2)}+ \frac{1}{m}F = f_{2}(x,F)\\ \frac{d}{dt}x_{1}= x_{2} = f_{1}(x, F)\end{cases}\end{align}$$
$$ \begin{align}\frac{d}{dt} \begin{pmatrix} \Delta x_{1}\\ \Delta x_{2} \end{pmatrix} = \begin{pmatrix} all \ derivatives \end{pmatrix} \begin{pmatrix} \Delta x_{1} \\ \Delta x_{2} \end{pmatrix} + (derivative \ of \ f_{1} \ and \ f_{2} \ by \ F) (x_0,u_{0)}\Delta F \\ = \begin{pmatrix} 0 & 1 \\ 0 & \frac{-k}{m}(1+ 2x_{2} \end{pmatrix} (x_0,u_{0)} \Delta x \\ + \begin{pmatrix} 0 \\ \frac{1}{m} \end{pmatrix} \Delta u = \begin{pmatrix} 0 & 1 \\ 0 & \frac{-k}{m} \end{pmatrix} \Delta x \end{align}$$
Where in the last line, the eq in VL ist **B**, and HL is **A**. 
The **C** matrix, we get from derivation and then putting in the stationary points.

We now get:
![[Pasted image 20220901160432.png]]
![[Pasted image 20220901160532.png]]
![[Pasted image 20220901160541.png]]

**State-space:**


**Transfer function:**

