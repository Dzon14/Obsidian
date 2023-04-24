# Linear phase
When we apply a filter to an input signal, it is often beneficial if all frequency components experience the same delay (and are not shifted relative to each other) so that the shape of the signal is maintained.

From lecture 6: $$\Delta(\omega) = - \angle H(\omega)/\omega \ \ \ [samples]$$
Here a filter introduces a delay to a freq. component at angular freq $\omega$.

If we want all frequency components to experience the same delay, the requirement is that $\Delta(\omega)$ is constant for all $\omega$.

Assuming that constant delay is $\Delta_0$ we can write the requirement as $$\Delta_{0} = - \angle H(\omega)/\omega \Rightarrow \angle H(\omega) = - \Delta_{0}\omega$$
where $-\Delta_0(\omega)$ is a **Linear** function of $\omega$.
We see that the phase response of the filter must be a linear function of $\omega$ (with slope $-\Delta_0$).

![[Pasted image 20220921094532.png|500]]

## Linear phase - important slide!!
The symmetry conditions on impulse responses can be expressed in terms of the [[Z-transform]] ($H(z)$) (using the time-reversal and delay properties).
![[Pasted image 20230407175947.png]]

[[Notch filters|IIR filter]] cannot have a linear phase if it's BIBO stable.

#el 