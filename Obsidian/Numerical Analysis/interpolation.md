---
tags: [num]
---
# Interpolation
If  $P(x)$ is intended for evaluation only at points x in the interval $[x_{0},x_{n}]$ then we talk about *regular* interpolation. If it's intended for evaluation at points x lying outside of $[x_{0}, x_{n}]$ we talk about *extrapolation* which are the different types.
![[Pasted image 20230327163344.png]]
**Reasons for Interpolating**:
- graph a curve that passes through some discrete number of points: computer graphics
- evaluate a mathematical function easily and quickly, sine, cosine, log, exponential ...
- Substitute a "difficult" function by an "easy" one: simplifying a mathematical model for the weather report, integrating numerically. 
- Extract information from a table of values: predict what data would be at points where it wasn't measured, or analyse the growth pattern of the data.

**How to choose the form of interpolating function:**
- are there relevant mathematical or physical considerations? 
- how should the function behave between the data points? 
- should the function have some properties like periodicity? 
- should the graph be pleasant to the eye? 
- do we need the mathematical description of the interpolating function or do we only need its graph?

**Types of interpolating functions:**
- [[polynomial interpolation]]
- Piecewise linear
- [[piecewise polynomial interpolation]] ([[spline]])
- Trigonometric functions (Fourier series)
- Exponential functions
- Rational functions

## Piecewise linear interpolation
data points are connected with straight lines. It produces kinks in the measuring point and hence is not *smooth*.
Alternative: [[polynomial interpolation]].


