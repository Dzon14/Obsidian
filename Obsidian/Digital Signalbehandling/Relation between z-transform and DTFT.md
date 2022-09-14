## Relation between z-transform and DTFT
- This relationship allows us to understand the **DTFT** better, making use of [[Poles]] and [[Zeros]] of $X(z)$. 

See def. for [[Z-transform]] & def. for DTFT in [[Fourier transform|fouriertransform]].

DTFT can also be expressed in angular frequency as $$X(\omega) = \sum_{n=-\infty}^{\infty}x(n)e^{-j \omega n}$$
We have a similarity between these two and if the unit circle $\lvert z \rvert = 1$ is inside the ROC of the z-transform, we have $$X(f) = \underset{z=e^{j2\pi f}}{X(z)} \text{and} X(\omega) = \underset{z=e^{j \omega}}{X(z)}$$
**Reminder:** $\lvert z \rvert = 1 \ \text{since} \  z=e^{j2 \pi f}  = e^{j \omega} \text{has magnitude 1}$

![[Pasted image 20220914082752.png|500]]

### Poles and zeros influencing $X(\omega)$
![[Pasted image 20220914083645.png]]

### A geometric view - magnitude of $X(\omega)$
![[Pasted image 20220914083923.png]]
**Two conclusions:**
- A zero close to the unit circle will attenuate $X(\omega)$ near its location. The closer the stronger the attenuation
- A pole close to the unit circle will amplify $X(\omega)$ near its location. The closer the stronger the amplification. 

### Phase of $X(\omega)$ using poles and zeros
![[Pasted image 20220914085835.png]]
**Two conclusions:**
- Poles and zeros contribute with phase charges of opposite sign.
- When a zero or a pole is close to the unit circle, the phase change changes rapidly near it. 

#el