---
aliases: [LTI-system, LTI]
---

# Linear and time-invariant (LTI) systems
- The impulse response h(n) of an LTI system is the output signal, when the input signal is a unit impulse at time n = 0.
![[Pasted image 20220831083753.png]]
- An arbitrary input signal x(n) can be written as a sum of delayde impulses
- Since LTI systems are both time-invariant and linear, the output signal y(n) will be the corresponding sum of impulse responses

## Response to sinusoids
With the input $$x(n) = Ae^{j \omega n}$$
we get $$y(n) = \sum_{k=-\infty}^{\infty}h(k)Ae^{j \omega (n-k)}$$
By splitting up to the exp in the sum we get $$y(n) = \sum_{k=-\infty}^{\infty}h(k)Ae^{j \omega n}e^{-j \omega k}$$
We now write $$y(n) = \left( \sum_{k=-\infty}^{\infty} h(k)e^{-j \omega k}\right) Ae^{j \omega n}$$
where the **parantese** is the **[[Discrete-time Fourier Transform|DTFT]]** $H(\omega)$ of $h(n)$.
- The same complex sinusoid comes out of the LTI system but multiplied by a complex constant $H(\omega)$ - which means that the C-sinusoid is an egienfunction of the system with the eigenvalue $H(\omega)$.
- **Reminder:** $Ax = \lambda x$, where x is the eigenvector and $\lambda$ is the eigenvalue.

##### Two complex sinusoidals
Do as above for both inputs (separately) and then add them because of linearity. 
- if we input cosine, we get an output (if $h(n)$ is real-valued) $y(n) = H(\omega)Acos(\omega n)$, Where the cos term is an eigenfunction of LTI systems. 
- Same for sinus.
- For both cases we use Eulers formula (from e to cos/sin).

### General expression
We can write the relations in terms of magnitude and phase.
$$\begin{align} y(n) = H(\omega)Ae^{j \omega n} = \lvert H(\omega) \rvert e^{j \angle H(\omega)}Ae^{j \omega n} \\ = \lvert H(\omega) \rvert Ae^{j(\omega n + \angle H(\omega))}  \end{align}$$
For real-valued impulse responses and cos or sin inputs we express the output in the same form but with cos or sin instead of e. $$y(n) = \lvert H(\omega) \rvert Acos(\omega n + \angle H(\omega))$$
By looking at the shape of the signals, we see that there's a **delay** cause by the phase shift with $$\Delta (\omega) = - \frac{\angle H(\omega)}{\omega}$$
**Note:** The delay of the signal is typically frequency dependent and negative phase shifts give positive delays. 

## LTI systems with rational system function
[[Poles]] and [[Zeros]] characterize both amplitude and phase of [[Z-transform]] expressed in rational form. 

By placing poles and zeros in the z-domain, it should be possible to design filters. with some desired frequency response ($H(\omega$))




#el 