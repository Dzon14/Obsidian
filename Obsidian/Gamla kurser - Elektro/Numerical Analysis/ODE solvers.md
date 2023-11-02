---
tags: [prog]
---
# ODE Solvers
(ordinary differential equations)

- Exact solutions
- Numerical solutions

## Exact solution

- dsolve will not accept equations as strings in a future release. Use expressions instead. 
```python
syms y(t)
dsolve(diff(y) == t*y)
```

##### First order - symbolic solver
![[Pasted image 20230323162440.png|500]]

##### Symbolic solver for initial value problems
![[Pasted image 20230323162513.png|500]]

##### Symbolic solver for high order ODEs
![[Pasted image 20230323162851.png|550]]

## Exact solution for systems

##### Symbolic solve for systems of ODEs
![[Pasted image 20230323162959.png|500]]

##### Symbolic solvers for IVPs for systems of ODEs
![[Pasted image 20230323163037.png|550]]

## Numerical solvers
There are two available numerical solvers:
- non-stiff problems (solved efficiently by explicit methods)
- stiff problems (difficult to solve with explicit methods, require small step size).

#### Solvers for non-stiff problems
- ode45 - one-step solver
- ode23 - one-step solver but more efficient ode45
- ode113 - multistep solver, more efficient than ode45
If these are slow try stiff solvers

#### Solvers for stiff problems
- ode15s - multistep, try if ode45 fails or is very inefficient. variable-order
- ode23s - one-step solver, more efficient than ode 15s
- ode23t - use for moderately stiff problems
- ode234b - more efficient than ode15s at crude tolerance

##### Example
![[Pasted image 20230323163756.png]]

## Solver configuration
![[Pasted image 20230323163951.png|550]]

## Passing parameters
![[Pasted image 20230323164032.png]]