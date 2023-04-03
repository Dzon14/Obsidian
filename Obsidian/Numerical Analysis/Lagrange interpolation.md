---
tags: [num]
---
# Lagrange interpolation
- A form of [[polynomial interpolation]]
- Most important as a theoretical tool (since it has a high cost)

## Lagrange interpolation formula
$$\begin{align}  P_{2}(x) = y_{1}\frac{(x-x_{2})(x-x_{3})}{(x_{1}-x_{2})(x_{1}-x_{3})} + y_{2}\frac{(x-x_{1})(x-x_{3})}{(x_{2}-x_{1})(x_{2}-x_{3})} + y_{3}\frac{(x-x_{1})(x-x_{2})}{(x_{3}-x_{1})(x_{3}-x_{2})}\end{align}$$
This is for three points $\Rightarrow n=2$ .

## Polynomial interpolation with Lagrange basis functions
$$\phi_{i}(x) = \prod\limits_{\begin{align} k&=0 \\ k &\neq i \end{align}}^{n}\frac{x-x_{k}}{x_{i}-x_{k}}, \ \ \ i = 0,1,...,n$$
![[Pasted image 20230328144359.png|500]]

As an example we write out $\phi_{2}(x)$ for n=4; $$\phi_{2}(x) = \frac{(x-x_{0})(x-x_{1})(x-x_{3})(x-x_4)}{(x_{2}-x_{0})(x_{2}-x_{1})(x_{2}-x_{3})(x_{2}-x_{4})}$$All the Lagrange basis functions $\phi_{i}(x)$ are the nth-degree polynomials. Furthermore they have the special property $$\begin{align}  &\phi_{i}(x_{i}) = 1 \\ &\phi_{i}(x_{j}) = 0, \ \ \ j \neq i \end{align}$$The Lagrange basis functions make the system matrix: $$\begin{bmatrix} 1 & 0 & 0 & 0 & 0 \\ 0 & 1 & 0 & 0 & 0 \\ 0 & 0 & 1 & 0 & 0 \\ 0 & 0 & 0 & 1 & 0 \\ 0 & 0 & 0 & 0 & 1 \end{bmatrix} \begin{bmatrix} c_0 \\ c_1 \\ c_2 \\ c_3 \\ c_4 \end{bmatrix} = \begin{bmatrix} f_0 \\ f_1 \\ f_2 \\ f_3 \\ f_4 \end{bmatrix}$$

## Advantages of Lagrange
- Simplicity

## Downsides of Lagrange
The marginal cost of evaluating $P_{n}(x)$ at a new point $x$ with Lagrange basis functions is more than twice as large as with monomial basis functions. 
- P needs around $2N^{2}$ operations (2N multiplication and one division for each Lagrange basis function)
- If a data point is added all Lagrange polynomials need to be computed again

## Example
- Three data points (n=2):
![[Pasted image 20230328144734.png]]
From this we get $c_{0}=-27, c_{1}=-1$ and $c_{2}= 0$
We get $$\begin{align*} &\phi_0(x) = x(x-1) \ = -\frac{2}{(-3)}\cdot (x(x-1)) \ = -\frac{1}{6}(x(x-1)) \\ &\phi_1(x) = (x+2)(x-1) \ = \frac{2}{(-1)}\cdot ((x+2)(x-1)) \ = -\frac{1}{2}((x+2)(x-1)) \\ &\phi_2(x) = (x+2)x \ = \frac{3}{1}\cdot ((x+2)x) \ = \frac{1}{3}((x+2)x) \end{align*}$$
From $$P_{n}(x) = \sum\limits_{i=0}^{n}c_{i}\phi_{i}(x) = \sum\limits_{i=0}^{n}c_{i}L_{i}(x_{n})=f_{n}$$(L for Lagrange), we now get $$P_{2}(x) = -\frac{27}{6}x(x-1) + \frac{1}{2}(x+2)(x-1)$$we verify that $P_{2}(-2) = -27, P_{2}(0)=-1$ and $P_{2}(1) = 0$