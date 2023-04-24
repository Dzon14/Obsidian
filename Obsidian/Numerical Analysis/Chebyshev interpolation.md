---
tags: [num]
---
# Chebyshev interpolation/nodes
 - A way to optimally choose the nodes
 - We reduce the error by minimizing $\lvert \lvert B_{N+1} \rvert \rvert_\infty$
- Chebyshev interpolation refers to a particular optimal way of spacing the points $x_{i}$
- The motivation for this interpolation is to improve control of the maximum value of the [[interpolation error]] on the interpolatiuon interval. 
- With this we can avoid *Runge phenomenon* which is when a polynomial of 9 x's are spread evenly, the tendency for the polynomial is to be large near the ends of the interval. If we use Chebyshev we choose the points in a way that equalizes the size of the polynomial throughout the interval. 
- *Runge phenomen* is when we get wild spikes when fitting some kind of polynomial. Fixed by Chebyshev nodes, that we find from equally spacing the points on a circle and project them down on the horizontal axis. These are the points we wanna use for our fit! (see in illustrations).
- Chebyshev kind of equalizes the error, it distributes the absolute error equally, while [[Lagrange interpolation]] has bigger [[interpolation error|interpolation errors]] near the boundaries than in the middle. 
## Theorem
![[Pasted image 20230328165933.png]]

![[Pasted image 20230418144346.png]]

## Illustrations
![[Pasted image 20230330155250.png|450]]
![[Pasted image 20230330155317.png]]

## Best approximation
![[Pasted image 20230330152522.png]]
**Error estimate formula:** $$\lvert \lvert P_{n}-f \rvert \rvert_{\infty} \leq \frac{\lvert \lvert f^{(N+1)} \rvert \rvert_\infty}{(N+1)! \cdot 2^{N}}$$
- When we do this error estimation, we need to take into account the stretching of the interval (it will shift?) ???

## Chebyshev
We always use(?): $$cos\left(\frac{2m+1}{2N+2}\pi \right)$$This makes the chebyshev nodes clustered at the endpoints of the interval where the function typically varies the most. 
Can also be written as the roots (book): $$x_{i} = cod \frac{odd \ \pi}{2n}$$

## General interval $[a,b]$
Here we optimmaly choose the nodes: $$x_{m} = \frac{(b+a)}{2} + \frac{(b-a)}{2}cos(\frac{2m+1}{2N+2}\pi), \ \ \ m=0,...,N$$
## Example from book
![[Pasted image 20230418144807.png]]