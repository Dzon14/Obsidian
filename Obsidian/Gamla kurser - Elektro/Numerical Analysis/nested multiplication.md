---
tags: [num]
aliases: [Horners method]
---
# Nested multiplication
If we have a polynomial $$P(x) = 2x^{4} + 3x^{3}-3x^{2}+5x-1$$and we wan to find $x=\frac{1}{2} \Rightarrow P(\frac{1}{2})$, it's nested form is
![[Pasted image 20230321135023.png]]
It can be seen as writing the polynomial backwards and factorising as much as possible.
Once you can see to write it this way—no computation is required to do the rewriting—the coefficients are unchanged. Now evaluate from the inside out: 
![[Pasted image 20230321135225.png]]