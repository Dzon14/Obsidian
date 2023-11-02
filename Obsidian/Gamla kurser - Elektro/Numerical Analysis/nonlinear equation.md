---
aliases: [nonlinear system, nonlinear systems, nonlinear equations]
tags: [num]
---
# Nonlinear equations
- Cannot be written as $Ax=b$
-  All numerical methos [[nonlinear equation|nonlinear equations]] are *iterative*
- Generally harder than [[linear systems]], since it's impossible to know how many solutions there are and there's no algorithm for its solution that always works. Although an exception for this is zeros of polynomials. For ex:$$P_{4}(x) = c_{0}+c_{1}x+c_{2}x^{2}+c_{3}x^{3}+c_{4}x^{4}$$with all its roots. 

There are two standard forms: $$\begin{align} f(x) = 0 \\ x= g(x) \end{align}$$where x is the solution sought and f and g are functions. We want to look at both scalar and vector valued x,f,g