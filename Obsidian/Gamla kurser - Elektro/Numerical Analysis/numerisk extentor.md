---
tags: [num]
---
# Numerisk extentor

- [[2017-06-03 numerisk]]
- [[2017-08-24 numerisk]]
- [[2018-04-05 numerisk]]
- [[2019-04-24 numerisk]]
- [[2020-08-22 numerisk 1]] (svår)
- [[2021-06-05 numerisk]] (på tavlan)
- [[2021-08-17 numerisk 1]]


## To do
- Se Andreas extrauppgifter - KVAR ATT GÖRA
- Gör alla extentor - klar
- Kolla igenom alla anteckningar - Typ klar
- Gå igenom Andreas tenta igen
		- Förstå den svåra uppgiften??
- Lära mig translation table för [[initial value problems|IVP]] - typ klar
- Gå igenom alla quadratures och lära mig "fusk"formler (PRIO) - klar men se nedan
		  - Repeterat de uppgifterna 
- Power iteration - typ klar?
- [[Gauss-Seidel method]] och [[Jacobi method]] iteration formulas - klar
- Repetera [[Newton's method]] - klar
- Repetera [[numerical differentiation]] - typ klar

## Remember
![[Pasted image 20230522133443.png]]

##### Discretization table for IVP
![[Pasted image 20230522155929.png]]

##### P-norm - another formula
![[Pasted image 20230524140501.png]]

##### Conditioning - to prove it's larger than 1
![[Pasted image 20230524140902.png]]

#### Iterative methods
- For both methods, if $\lvert \lvert B \rvert \rvert < 1$ it converges to the exact solution x of the linear system Ax = b. Inf for gauss-seidel and 1-norm for Jacobi. Apparently we can also take the 2-norm for Jacobi to prove that A converges. 
**Jacobi method:**
Start with $Ax = b$ and,
Separate A as $$A = L + D + U$$
we now get $$Ax = b \Leftrightarrow (L+D+U)x =b$$which can be rewritten to $$\begin{align} D&x = - (L+U)x+b \\ &x= -D^{-1}(L+U)x+D^{-1}b \end{align}$$comparing this to $x=Bx+c$ , Jacobi gives us $$B=-D^{-1}(L+U) \ \ \text{ and } \ \ c=D^{-1}b$$
Set $P = D$ and $N = P-A = -(L+U)$ then we get (using [[splitting]] method): $x_{k+1} = P^{-1}Nx_{k}+P^{-1}b$
we get the *Jacobi method*: $$x_{k+1}= \underbrace{-D^{-1}(L+U)x_{k}}_{B} + \underbrace{D^{-1}b}_{c}$$

**Gauss-seidel**
Note: This formula comes from the same as Jacobi, the only difference is that re-write it so it becomes faster in iterations??? In the twist it's fine to have $x_{i+1}$ on the right side since by the time it comes to the lower part of the matrix, the next iteration has already been produced.
In general:
$$(L+D)x^{(k)} = -Ux^{(k-1)} + b$$
Computational (härledning): $A=L+D+U$ (as for [[Jacobi method]]) gives $(L+D+U)x = b$. This gives $$\begin{align} &(L+D)x = -Ux + b \\ &x= (L+D)^{-1}(-Ux+b) \\ &x_{k+1} = (L+D)^{-1}(b-Ux_{k}) = x_{k+1}=\underbrace{ -(L+D)^{-1}U }_{ =B }x_k+\underbrace{ (L+D)^{-1}b }_{ =c }\end{align}$$ $i=0,1,...$
**Gauss-Seidel with a TWIST:**
From the standard formula above we can write $$\begin{align} &Lx_{k+1} + Dx_{k+1}= b-Ux_{k} \\ &Dx_{k+1}=b-Ux_{k}-Lx_{k+1} \\ &x_{k+1}=D^{-1}(b-Ux_{k}-Lx_{k+1}) \end{align}$$$i=0,1,...$
This formula is equivalent to the "standard" formula, but it looks a bit funny. Could one really have $x_{i+1}$ on the right hand side of an iterative formula? The answer is “yes”. The explanation is that matrix-vector multiplication on the right hand side of this formula is done one row at a time, thereby producing the new entries of $x_{i+1}$ one by one – starting at the top. Thanks to the strictly lower triangular structure of $L$, the individual entries of $x_{i+1}$ on the right hand side are only needed in $Lx_{i+1}$ when they already have been produced.