---
tags: [num]
---
# Partial pivoting
Chooses largest magnitude in column as pivot. Possible because rows may be interchanged $\Rightarrow$ No swamping

The partial pivoting protocol consists of comparing numbers before carrying out each elimination step. The largest entry of the first column is located, and its row is swapped with the pivot row, in this case the top row

[[Gauss elimination|Gaussian elimination]] with [[LU factorization]], as described above, is not a stable numerical method. For one thing, if a pivot is zero the scheme breaks down. Better stability is obtained when pivots are large in modulus compared to all entries below them, and this effect can be obtained by dynamically swapping the order of the equations as the LU factorization progresses

$$P^{-1}= P^{T}$$

- Important to always check that $$\lvert a_{p1} \rvert \geq \lvert a_{i1} \rvert$$in every elimination step 

## Example
![[Pasted image 20230328135102.png|700]]

