---
tags: [num]
aliases: [Euler methods]
---
# Euler's method

## Discretization table
![[Pasted image 20230522155837.png]]
This leads to the following formulas....:

## Forward Euler/Explicit Euler
$$\begin{cases} u_{i+1} = u_{i}+hf(t_{i},u_{i})\ \ \ \  i=0,1,2,..., \\ u_{0}= \alpha \end{cases}$$

##### Local truncation error
$$L_{i+1}=y(t_{i}+h) - (y(t_{i})+hf(t_{i},y(t_{i}))) = O(h^{2})$$

## Backward Euler/Implicit Euler
- Better stability in certain situations $$\begin{cases} \begin{align} &u_{i+1}=u_{1}+hf(t_{i+1}, u_{i+1}), \ \ \ i=0,1,2, \dots \\ &u_{0} = \alpha \end{align} \end{cases}$$
##### Local truncation error 
$$O(h^{2})$$

## Example  - forward
![[Pasted image 20230511171150.png]]
![[Pasted image 20230511171353.png]]

## Example - forward
![[Pasted image 20230511174243.png]]

## Example - backward
![[Pasted image 20230511180313.png|550]]
![[Pasted image 20230511180344.png|500]]