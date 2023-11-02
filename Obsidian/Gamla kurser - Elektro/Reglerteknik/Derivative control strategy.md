---
aliases: [D-delen, D-controller, D-part]
tags: [regler]
---

# Derivative control strategy
The D-part in a PID-controller is proportional to the controller error. Without the D-part, the PI-controller will only see old errors and not predict future errors. 

$u(t) = K_{prop}e(\tau) + k_{1} \int_{0}^{t} e(\tau) \, d \tau + K_{D} \, \frac{de(\tau)}{dt}$
- If error signal is not zero, the area will increase

From textbook:
![[Pasted image 20220830143631.png]]