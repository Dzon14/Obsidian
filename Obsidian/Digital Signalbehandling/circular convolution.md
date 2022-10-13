---
tags: [el]
aliases: [cirkulär faltning]
---
# Circular [[Faltning|convolution]]
a type of [[Faltning|Convolution]].

When performing circular [[Faltning|convolution]] of length N between two signals/sequences we also time-reverse one of them, shift it relative to the other one, and sum the product of individual elements for each shift, with the difference that we calculate indices mod N, and get a resulting sequence of length N.
$$\circledast$$


## Example 1 (check later)
![[Pasted image 20220928094456.png]]

## Example 2
![[Pasted image 20220928094511.png]]

## Matlab code (same example as before)
- Fast fourier transformation (FFT) command
![[Pasted image 20220928094739.png]]

## Circular $\longrightarrow$ linear [[Faltning|Convolution]]
Using the [[Discrete Fourier transform|DFT]] on a computer is a very efficient way of calculating the circular [[Faltning|convolution]].
Can we use DFT to calculate linear as well?
- One problem is that the result of the circular [[Faltning|convolution]] is of the same length as the sequence involved. However, linear conv. produces an output that is longer than the sequence.
- If we zero-pad two sequences and perform a circular [[Faltning|convolution]] we get:
![[Pasted image 20221003133113.png]]
- we get the same result as a linear [[Faltning|Convolution]]

## [[Faltning|linear convolution]] $\longrightarrow$ circular convolution
if we have an [[Linear and time-invariant (LTI) systems|LTI]] system with a linear convolution $$y(n) = h(n)*x(n) = \sum_{k=0}^{K-1}h(k)x(n-k)$$
![[Pasted image 20221003141744.png|450]]

This is used in communication systems. One of the most clever applications of the [[Discrete Fourier transform|DFT]].