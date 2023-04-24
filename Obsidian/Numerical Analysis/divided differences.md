---
tags: [num]
---
# Divided differences

## Newton's divided differences
- Alternative to [[forward substitution]] (mainly in the case of [[Newton interpolation]])

The basis of the divided difference scheme is the *recursion*: $$f[x_{i},...,x_{i+k}] = \frac{f[x_{i+1},...,x_{i+k}] - f[x_{i},...,x_{i+k-1}]}{x_{i+k} - x_{i}}$$where $k=1,...,n$ and $i=0,...,n-k$. The recursion is initiated with $$f[x_{i}]=f_{i}, \ \ \ i=0,...,n$$When the first equation is completed the $c_{i}:s$ are obtained as $$c_{i}=f[x_{0},...,x_{i}], \ \ \ i=0,...,n$$
![[Pasted image 20230328153638.png]]

## Table of divided difference (from book)
![[Pasted image 20230328154125.png]]

## From slides
![[Pasted image 20230328154243.png]]

## Example with Newton basis
![[Pasted image 20230328154322.png]]
- Use [[nested multiplication|Horners method]]!
- If we add a fourth data point to the data we only have to add a new row and a new column.
- The diagonal gives the coefficient
![[Pasted image 20230328155305.png|450]]

## Numerical example
![[Pasted image 20230329155351.png|550]]

## Example from book
![[SmartSelect_20230418_140150_Samsung Notes.jpg]]
If we want to add new data points, it's easy to do:
- Add (1,0) to the list.
![[Pasted image 20230418140357.png]]