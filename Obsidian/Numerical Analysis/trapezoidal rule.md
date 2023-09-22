---
aliases: [trapezoidal quadrature]
tags: [num]
---
# The trapezoidal rule
- A form of [[Newton-Cotes quadrature]], where the area under the curve is approximated by the area of a trapezoid that connects the endpoints of the interval.
- Linear - $Q^{1}$
- A closed [[Newton-Cotes quadrature|Newton-Cotes rule]] defined $n=N=1, x_{0}=a, x_{1}=b$

$$Q^{1}(f) = \frac{b-a}{2}(f(a)+f(b))$$The trapezoidal rule is exact for polynomial $P \in \mathbb{P}_{1}$ (degree of precision = 1)
We calculate
![[Pasted image 20230404162501.png]]

## Trapezoid Rule
$$I_{app} = \int\limits_{x_{0}}^{x_{1}} f(x) \ dx = \frac{h}{2}(y_{0}+y_{1})- \frac{h^{3}}{12}f''(c)$$where $h=x_{1}-x_{0}$ and $c$ is between $x_{0}$ and $x_{1}$.

## Error formula
![[Pasted image 20230404162625.png]]
(remember for exam)

## Illustration
![[Pasted image 20230404173257.png]]

## Example from book 
![[Pasted image 20230421150832.png]]![[Pasted image 20230421150846.png]]