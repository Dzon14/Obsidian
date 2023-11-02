---
tags: [num]
aliases: [pivot]
---
# Pivoting
- A pivot cannot be 0
- A small pivot can introduce large numerical errors
- Multipliers should be less than 1 (in magnitude)


## For [[Gauss elimination]]
If during the process a pivot element is *zero*, then *exchange rows*. 
If not possible because the elements below are also zero, then we have a singular system (not uniquely solvable). 

## Swamping
- In numerical analysis, swamping is a phenomenon that occurs in floating-point arithmetic when the result of a computation is too small to be accurately represented. When a floating-point number is too small, it is said to underflow, and the result of the computation may be replaced by zero or a very small value that does not accurately represent the true result. Swamping can lead to loss of precision and numerical instability in subsequent calculations. Swamping is the opposite of overflow, which occurs when a floating-point number is too large to be represented accurately.

**Exact solution:**
$$\begin{bmatrix} 10^{-20} & 1 \\ 1 & 2 \end{bmatrix} \begin{bmatrix} x \\ y \end{bmatrix} = \begin{bmatrix} 1 \\ 4 \end{bmatrix} \Rightarrow x = \frac{2 \cdot 10^{20}}{10^{20}-2}; \ \ y = \frac{4-10^{20}}{2-10^{20}}$$where $x \approx 1$ and $x \approx2$
**With double precision:**
$$\begin{bmatrix} 10^{-20} & 1 \\ 1 & 2 \end{bmatrix} \begin{bmatrix} x \\ y \end{bmatrix} = \begin{bmatrix} 1 \\ 4 \end{bmatrix} \Rightarrow y = 1; \ \ x=0$$
**After row exchange:**
$$\begin{bmatrix} 1 & 2 \\ 10^{-20} & 1 \end{bmatrix} \begin{bmatrix} x \\ y \end{bmatrix}= \begin{bmatrix} 4 \\ 1 \end{bmatrix} \Rightarrow y = 1, \ x=2 $$Multipliers should be small (pivots should be large)

## [[partial pivoting]]


## See [[LU factorization]] for LU with pivoting



