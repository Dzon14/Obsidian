---
tags: [num]
---
# Loss of significance
An advantage of knowing the details of computer arithmetic is that we are therefore in a better position to understand potential pitfalls in computer calculations. One major problem that arises in many forms is the loss of significant digits that results from subtracting nearly equal numbers.

We don't want to lose these significant digits. 
For ex. if we want to substract $\sqrt{9.01}-3$ , using a three digit computer (since we have three digit at most here), we get $\sqrt{9.01} = 3$, however in reality it is $\approx 3.0016662$.
To solve this we can calculate like this: $$\begin{align}  \sqrt{9.01}-3= \frac{(\sqrt{9.01}-3)(\sqrt{9.01}+3)}{(\sqrt{9.01}+3)} = \frac{9.01 - 3^{2}}{\sqrt{9.01}+3} = \frac{0.01}{3.00+3} = \frac{0.01}{6} \\ = 0.00167 \end{align}$$