---
aliases: [feedback system, återkoppling, återkopplingen]
---

# Feedback
![[Pasted image 20220906162313.png]]
n is showing that the measurement is not exact.
e is the error signal. You want to turn this error into a control action (this is done through the control system).
-1 is a multiplier to give a negative input.
r is what you want to happen.
d is an external signal

Equations from the picture:
$$\begin{align} Y(s) = P(s) U_{1}(s) \\ -D + U = C(s)E(s) \\ Y_1(s) = \tilde{Y}(s) \\ E = R+Y_{1} \\ \tilde{Y} = Y + N \\ U = D + U_{1} \end{align}$$
Then by eliminating internal variables, we get $$\begin{align} Y(s) = P(s)(D(s)+U_{1(s))} = P(s)(D(s)+C(s)E(s)) \\ =P(s)(D(s)+C(s)(R(s)+1(Y(s)+N(s)))) \\ = P(s)D(s) + P(s)C(s)R(s) - P(s)C(s)N(s) - P(s)C(s)Y(s) \\ = (1+P(s)C(s))Y(s) = P(s)D(s) + P(s)C(s)R(s)-P(s)C(s)N(s)\end{align}$$
By breaking out $Y(s)$ we get
$$Y(s) = \frac{P}{1+PC}D(s) + \frac{PC}{1+PC}R(s)-\frac{PC}{1+PC}N(s)$$
We only want external signals or transfer functions of a component. 
We get the following block scheme
![[Pasted image 20220906163556.png|500]]
where every block is a [[Transfer function]]. If compared with the first picture - from D to Y there's only a P (in the numerator), just as there is a P between them in the first picture. Same goes for the others. 

- The denominator is always $$\frac{\text{Product of stuff in the path}}{1-(-1 \cdot P(s)C(s))}$$
### Open loop system
$$G_{0}= G_{R}G_{P}$$
$G_{P}$ - Transfer function of the process
$G_{R}$ - Transfer function of the controller

### Closed loop system
$$G(s) = \frac{G_{o}(s)}{1+G_{o}(s)}$$
where $G_{o}$ is the open loop transfer function

## Steam engine
- One of the earliest example of control application. 
- Its angular speed is measured. 
![[Pasted image 20220906153031.png|200]]

### Uncontrolled Steam engine
![[Pasted image 20220906153155.png|300]]
An open-loop system. The output $\omega$ (angular speed) should be kept constant. 


#regler 