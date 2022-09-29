---
tags: [matte]
aliases: [cirkulär faltning]
---
# Circular convolution
a type of [[Faltning|Convolution]].

When performing circular convolution of length N between two signals/sequences we also time-reverse one of them, shift it relative to the other one, and sum the product of individual elements for each shift, with the difference that we calculate indices mod N, and get a resulting sequence of length N.

## Example 1 (check later)
![[Pasted image 20220928094456.png]]

## Example 2
![[Pasted image 20220928094511.png]]

## Matlab code (same example as before)
- Fast fourier transformation (FFT) command
![[Pasted image 20220928094739.png]]
