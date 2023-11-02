---
aliases: [känslighetsfunktionen, känslighetsfunktion]
---

# Sensitivity Function
In a feedback with open-loop transfer function ($G_{0}=G_{R}G_{P}$) the sensitivity function is given by $$S = \frac{1}{1+G_{P}G_{R}} = \frac{1}{1+P(s)C(s)}$$
- A transfer function which can be interpreted in (three) different ways.

#### Sensitivity Function as a Stability Margin
- Maximum value of the sensitivity function: $$M_{s}= \underset{\omega}{max} \lvert S(i \omega) \rvert$$
![[Pasted image 20220909163635.png|400]]
The figure shows that $M_s$ is given by the inverse of the shortest distance to the [[Nyquist Curve|Nyquist]] curve. 

#### Sensitivity Function as a measure of a Disturbance Rejection
In a system, disturbances can occur in many ways, and are often represented with
- The load disturbance $\mathcal{l}$ - enter at the process input in the same way as the control signal
- Measurement noise $\mathcal{n}$ - Measurement disturbances, often electrical disturbances (such as high freq. etc). 

When the control signal is $u = 0$, the process output becomes $$Y_{ol}(s) - N(s) + G_{P}(s) L(s)$$
If we know close the loop and set $r=0$, the output becomes $$Y_{cl}(s) = \frac{1}{1+G_{R}(s)G_{P}(s)}N(s) + \frac{G_{P}(s)}{1+G_{R}(s)G_{P}(s)}L(s)$$
The ratio of the two outputs is $$\frac{Y_{cl}(s)}{Y_{ol}(s)} = \frac{1}{1+G_{P}(s)G_{R}(s)} = S(s)$$
**Conclusion:** The Sensitivity function describes how disturbances are affected by the [[Feedback]]. For a frequency $\omega$, 
$\lvert S(i \omega) \rvert < 1$ disturbances are *rejected*, while for
$\lvert S(i \omega) > 1 \rvert$ disturbances are amplified by the feedback. 


#### Sensitivity Function as a measure of sensitivity to Modelling errors
![[Pasted image 20220912121729.png|500]]
#regler