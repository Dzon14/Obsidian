---
tags: [num]
---
# Memory
![[Pasted image 20230327152719.png]]
For a 3d problem with 100 nodes in each dimension $\Rightarrow n = 10^{6}$
Let $k \approx 10$
$\Rightarrow$ memory (using double precision: 6 byte) we obtain
![[Pasted image 20230327152725.png]]

$\longrightarrow$ [[sparsity|sparse matrix]] of this size can be stored and dealt with on an everyday laptop ... full matrices *not*.

Using [[LU factorization|LU]] decomposition needs O($n^{3}$) FLOP would need $\approx$ 16 years