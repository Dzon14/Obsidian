---
tags: [num]
---
# Numerical differentiation
- Used to approximate the derivative of a function using numerical techniques. Useful when the function to be differentiated is too complex to be solved analytically, or when only a set of data points are available
- The basic idea of numerical differentiation is to approximate the derivative of a function at a given point by computing the slope of a secant line passing through two points on the function that are close to the point of interest. The slope of this secant line is an approximation of the derivative at that point.

## Formulas

##### Two-point forward difference
$$f'(x_{i}) = \frac{f(x_{i}+h)-f(x_{i})}{h}- \frac{h}{2}f''(c)$$where $c$ is between $x$ and $x+h$. The $\frac{h}{2}f''(c)$ term is truncation error $\mathcal{O}(h)$. It  is derived using Taylor expansion.

##### Two-point backward difference
$$f'(x_{i}) = \frac{f(x_{i})-f(x_{i}-h)}{h}= f'(x) + \mathcal{O}(h)$$
**Example**:
![[Pasted image 20230502164055.png]]

##### Three-point symmetric/centered/central difference
$$f'(x_{i}) = \frac{f(x_{i}+h) - f(x_{i}-h)}{2h} - \frac{h^{2}}{6}f'''(c) = f'(x_{i})+\mathcal{O}(h^{2})$$where $x_{i}-h < c < x_{i}+h$. $\mathcal{O}(h^{2})$ is the truncation error. 
**Example**:
![[Pasted image 20230502164325.png]]

##### Three-point centered-difference for second derivative
$$f''(x_{i}) = \frac{f(x_{i}-h)-2f(x_{i}) + f(x_{i}+h)}{h^{2}}- \frac{h^{2}}{12}f^{(iv)}(c)$$for some $c$ between $x_{i}-h$ and $x_{i}+h$. Truncation error of two: $\mathcal{O}(h^{2})$.

## Rounding error
There is also rounding error (not only truncation error $\mathcal{O}(h)$). Let $\tilde{f}(x)$ be the quantity $f(x)$ as it is stored in the computer's memory with a relative error up to $\epsilon_{mach}$. The rounding error for Two-point forward is  $$\frac{\tilde{f}(x_{i}+h)-\tilde{f}(x_{i})}{h}- \frac{f(x_{i}+h)-f(x_{i})}{h}$$which is bounded, in modolus, by $$\frac{2 \epsilon_{mach}}{h}\lvert f(x_{i}) \rvert$$The rounding errors in the other two difference formulas are bounded by expressions similar to the one above, and it's the growth of the rounding error, as $h$ decreases. This is responsible for the V-shape in the graph below
![[Pasted image 20230502103714.png|550]]
##### Example - Rounding error

## Conditioning of numerical differentiation
- see [[condition number]]
In lights of the results in Figure 1, is numerical differentiation fundamentally ill-conditioned? Or are there better methods which are stable in the sense that the error dexreases monotonically with h?
- The conclusion is that numerical differentiation is always sensitive to high-frequency noise (such as rounding) and should, if possible, be avoided. If numerical differentiation is deemed necessary and high accuracy is of concern, then difference formulas should be of *higher order*, that is, have truncation errors $\mathcal{O}(h^{p})$ with a not too small integer p.

**Relative condition number of a problem**: $$\kappa_{prob} = \underset{\delta}{max} \frac{\text{relative change in solution}}{\text{small relative change } \delta/x \text{ in input}}$$For the differentiation problem and with $\tilde{x}=x + \delta$ this becomes $$\kappa_{prob}= \lim_{\delta\to0}\underset{\delta}{sup}\frac{\lvert \frac{f'(\tilde{x})-f'(x)}{f'(x)} \rvert}{\lvert \frac{\delta}{x} \rvert} = \frac{\lvert f''(x) \rvert \cdot \lvert x \rvert}{\lvert f'(x) \rvert}$$which should not be large unless $f'(x) \approx 0$

**Conditioning of differentiation with respect to perturbations in f itself**:
Small perturbation $\tilde{f}(x) = f(x) + \epsilon_{mach}sin(\omega x)$ where $\omega \approx \frac{\pi}{h}$ so that $\tilde{f}(x) - f(x)$ models small amplitude high-frequency noise at some assumed sampling points. The relative condition number becomes $$\kappa_{prob} = \frac{\lvert \frac{\tilde{f}'(x)-f'(x)}{f'(x)} \rvert}{\lvert \frac{\tilde{f}(x)-f(x)}{f(x)} \rvert} = \lvert \omega \rvert \frac{\lvert cos(\omega x) \rvert \cdot \lvert f(x) \rvert}{\lvert sin(\omega x) \rvert \cdot \lvert f'(x) \rvert}$$ which is large and grows as $\frac{1}{h}$, just like the rounding error of all three formulas in figure 1. 

## [[numerical differentiation in matrix form]]
