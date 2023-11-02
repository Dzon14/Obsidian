---
tags: [num]
---
# Spline
- See [[partition]]
- A type of [[piecewise polynomial interpolation]] where the polynomial equations are joined together to form a smooth curve.
- The simplest example is a linear spline where we connect the dots with straight-line segments.
- The idea behind splines is to divide a given range into smaller subintervals and approximate the function with a polynomial function within each subinterval. The resulting function is then piecewise defined over the entire range.
- One of the main advantages of using splines over other interpolation methods is that they can approximate complex functions with a high degree of accuracy, while maintaining smoothness and continuity. Additionally, spline functions can be easily differentiated and integrated, making them useful for a wide range of numerical analysis applications.


## Definition
Let $m \geq1$. With such a partition we consider now functions $P \in C^{m-1}(I)$ of the following type: $$P \in [x_{0},x_{N}] \rightarrow \mathbb{R} \ \ \text{ with } \ \ P_{|I_{n}} \in \mathbb{P}_{m} $$Function with these properties are called *splines* (m=1 linear splines, m=3 cubic splines) 

![[Pasted image 20230328163119.png|600]]

## For Linear piecewise polynomials
![[Pasted image 20230328162907.png|500]]