---
aliases: [DFT]
tags: [el]
---
# Discrete Fourier Transform (DFT)
Many [[Communication Systems]] today are based on DFT.

- Other transformations in this couse are functions of a continous-valued variable or a continous frequency variable, however this is less suitable for efficient digital implementation
- A transform where we only need samples of the frequency function at certain points on the continous frequency axis. We can implement frequency-domain processing our signals. 

## Definition
- We define the N-point discrete [[Fourier transform]] (DFT) as $$X(k) = \sum_{n=0}^{N-1}x(n)e^{-j2 \pi kn/  N} , \ \ \ \ k= 0,1,..,N-1$$
and the corresponding N-point inverse discrete Fourier transform (IDFT) as $$x(n) = \frac{1}{N}\sum_{k=0}^{N-1}X(k)e^{j2 \pi kn /N } , \ \ \ \ k=0,1,...,N-1$$
**Note:** is x(n) is time-limited to the period N, we avoid [[Aliasing]] in the time-domain.....
If it is not time-limited, the sampling of $X(f)$ is not dense enough and we get [[Aliasing]] in the time-domain. 
- Zero-padding: adding 4 zeros to a frequency and taking the DFT of that. If we have a signal length L we select $N > L$, with $N-L$ additional zeros.
  - Adding more zeros does not change its [[Discrete-time Fourier Transform|DTFT]] $X(f)$, but the larger N means that we sample $X(f)$ more densely in frequency.
    ![[Pasted image 20220928085700.png]]

## DFT as a linear transformation
The DFT and its inverse can be written as
$$\begin{flalign}  X(k) = \sum_{n=0}^{N-1}x(n)W_{N}^{kn} \\ x(n) \frac{1}{N} \sum_{k=0}^{N-1} 
X(k)W_{N}^{-kn}  \end{flalign}$$
where $W_{N}= e^{-j2 \pi /N}$, is an $N^{th}$ root of unity
Using this notations we can define the transform matrix
![[Pasted image 20220928090433.png]]
and then write the DFT and its inverse as a linear transformation on a convenient matrix form $$\begin{align}  \vec{X}_{N}= \vec{W}_{N}\vec{x}_{N} \\ \vec{x}_{N}= \vec{W}_{N}^{-1} \vec{X}_N \end{align}$$
with signal and transform coefficients $\vec{x}_N$ and $\vec{X}_{N}$ stacked in vectors.
Due to properties of the DFT, the inverse transform matrix can be written as $$\vec{W}_{N}^{-1} = \frac{1}{N}\vec{W}_{N}^{*}$$
where $\vec{W}_{N}^{*}$ denotes the complex conjugate of $\vec{W}_N$. In other words, we don't have to do an inverse matrix.


## Relationship between DFT and other transforms
![[Pasted image 20220928092849.png]]

## Properties of the DFT
![[Pasted image 20220928093049.png|400]]

## Multiplication of two DFTs
Just like other transforms, multiplication is equal to a linear [[Faltning|convolution]] in time domain.
Due to periodicity in the time-d
omain of the DFT, its corresponding relation is
![[Pasted image 20220928093922.png]]
Using [[circular convolution]]


