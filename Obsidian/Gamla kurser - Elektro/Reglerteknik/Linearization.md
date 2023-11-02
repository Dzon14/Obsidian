---
aliases: [linearize]
---

# Linearization
Is an approximation about a point.
To Approximate, we need to Linearize:
- First we need an equilibrium
		- Eqm. point: Solutions to our Diff.Eq. with all derivatives = 0.
- Then use Taylor series.

To linearize a system 
$\begin{cases} \dot{x} = f(x,u) \\ y = g(x,u) \end{cases}$
where f and g are nonlinear functions of x and u we need to follow four steps:

1) Determine a stationary point ($x_0$, $u_0$) around which we shall approximate the system. For a stationary point it holds that $$\dot{x}=0 \Leftrightarrow f(x_{0},u_0)= 0$$
2) Make Taylor series expansions of f and g around $(x_0,u_0)$. Keep only the first order terms. ![[Pasted image 20220830213209.png]]
Note that $f(x_0,u_{0}) = 0$ and introduce the notion $y_{0}= g(x_0,u_0)$.

3) Introduce the new variables $$ \begin{align}\Delta x = x - x_{0} \\ \Delta u = u - u_{0} \\ \Delta y = y - y_{0} \end{align}$$
4) The state space equations in the new variables are given by![[Pasted image 20220830214104.png]]

Note that f and x are vectors. For ex. a second order system, with the two states $x_1$ and $x_2$, a measurement signal y and a control signal u it holds that
![[Pasted image 20220830214726.png]]
Se the forel-pdf for an example of a nonlinear tank.

## Example
![[Pasted image 20220830152834.png|500]]
$u - mgsin \theta = m \frac{d^2}{dt^2} \theta$
Here the eqm.point is when:
 $u - mgsin \theta = 0$

$u = 0$, $\theta = 0$
- introduce new variables:
		$\Delta \theta = \theta - \theta_0$, where $\theta_{0}$ is the eqm. $\theta$
		$\Delta u = u - u_{0}$

$\Delta u + u_{0} - mgsin(\Delta \theta + \theta_{0}) = m$
$\frac{d^2}{dt^2}\Delta\theta = \frac{d^2}{dt^2}\theta$
![[Pasted image 20220830160410.png|500]]

Creating new variables, for each dot..?

$x_1 = \Delta \theta$
$x_{2} = \Delta \dot{\theta}$
$x_{3}= \Delta \ddot{\theta}$

$\Rightarrow$  $\frac{d}{dt}x_{1} = x_{2}$, 
$\frac{d}{dt}x_{2} = x_{3}$ 
and $\frac{d}{dt}x_{2} = x_{3}$

$\Delta u - mgx_{1} = m \frac{d}{dt}x_{2}$
![[Pasted image 20220830163110.png|400]]
Now we get
![[Pasted image 20220830163246.png|400]]

#regler 