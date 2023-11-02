---
tags: [num]
---
# Floating point representation
When we compute something by a computer, then the calculation may be affected by round-off (rounding) errors. Computers only use a finite set of approx. $10^{19}$ distinct *floating-point numbers*.
We will need [[error analysis]]

We want to represent a **real number**.

$$x_{\beta}= (-1)^{s}d_{0}.d_{1}...d_{k-1} \cdot \beta^{e}$$![[Pasted image 20230320162431.png]]

There are three commonly used levels of precision for floating-point number ($\beta=2$)
![[Pasted image 20230320162509.png|500]]

## IEEE Arithmetic
![[Pasted image 20230320162611.png]]
where b is 0 or 1. e is an M-bit binary number representing the exponent. **Normalization** $\rightarrow$ leftmost bit must be 1.
##### Example
![[Pasted image 20230320162804.png]]
This gives $\epsilon_{mach} = 2^{-52}$ whic is the IEEE point standard for [[machine epsilon]]

## Representation of infinite (binary numbers)
There are different methods to represent it as finite. 

#### Method 1: Chopping
Throw away the bits that falls off in the end. 
- biased in that it always moves the result towards zero. 

#### Method 2: Rounding
Base 10: 
- if next digit is $\geq 5$ , then round up
- if next digit is < 5, then round down
- If bit 53 is 1, then add 1 to bit 52 (round up)
- If bit 53 is 0, then do nothing to bit 52 (round down)
- If the bits following 52 are 100...0...0... (halfway between up and down, all numbers after the 1 is 0) we round up or down according to which choice makes the final bit 52 equal to 0. 
  from book: If the 53rd bit is 1, then round up (add 1 to the 52 bit), unless all known bits to the right of the 1 are 0’s, in which case 1 is added to bit 52 if and only if bit 52 is 1
$\Rightarrow$ *Rounding to Nearest Rule*

## IEEE floating-point number
We denote the IEEE double precision floating point number associated to $x \in \mathbb{R}$ using Rounding to Nearest rule, by $fl(x)$
![[Pasted image 20230320164413.png|500]]
52 bits comes from double precision (mantissa). $2^{-52}$ means 52 places to the decimal point. 
0.0110 = 0.4 is explained in [[decimal point to binary point]]

## With [[condition number]]
In the floating point arithmetic, the relative backward error cannot be expected to be less than $\epsilon_{mach}$, as storing the entries of b will already cause errors of that size.
![[Pasted image 20230322165240.png]]

