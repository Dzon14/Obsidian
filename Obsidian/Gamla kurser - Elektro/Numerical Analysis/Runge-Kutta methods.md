---
tags: [num]
---
# Runge-Kutta methods
- The Runge–Kutta Methods are a family of ODE solvers that include the [[Euler's method|Euler methods]] and Trapezoid Methods, and also more sophisticated methods of higher order.
- Runge-Kutta methods work by approximating the solution of an ODE at discrete time steps. They use a weighted average of function evaluations at different points within each time step to estimate the change in the solution over that interval. The accuracy and order of a Runge-Kutta method depend on the number of function evaluations and the weights assigned to them.

## RK4
The most famous member (fourth-order explicit method) $$u_{i+1}=u_{i} + \frac{h}{6}(k_{1}+2k_{2}+2k_{3}+k_{4})$$where $$\begin{align} &k_{1}= f(t_{i},u_{i}) \\ &k_{2}=f\left(t_{i}+ \frac{h}{2}, u_{i}+ \frac{h}{2}k_{1}\right)\\ &k_{3}= f\left(t_{i}+ \frac{h}{2}, u_{i}+ \frac{h}{2} k_{2}\right)\\ &k_{4}=f(t_{i}+h, u_{i}+hk_{3}) \end{align}$$