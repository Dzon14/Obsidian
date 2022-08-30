---
aliases: [P-delen, P-controller]
---

# Proportional control strategy
Is used when it is small errors in the control system. This is reduced by lowering the amplification.

![[Pasted image 20220830140720.png]]

![[Pasted image 20220829163652.png|400]]

### Example

![[Pasted image 20220829163949.png]]

$$y =K_{p}K_{e}= K_{p}K(r-y)$$
$$y + K_{p}K_{y}= K_{p}K_r$$
$$y = \frac{K_{p}K}{1+K_{p}K} \cdot r$$
- In some controllers the proportional band (PB) is used instead of amlification. It follows $$PB = \frac{100}{K} \ [\%]$$
- The P-controller makes the oscillations in [[OnOff regulator (control strategy)]] disappear. 

-  For small controller-errors, the P-controller is working in its PB. The error is then given by $$e = \frac{u-u_{0}}{K}$$
- e is zero when if at least of one of the conditions below is granted. 
	1. K is infinite big
	2. $u_{0}= u$
Alternative 1 is the same as PB = 0. It also corresponds to On/off control, which will give a on/off control problem. Therefore option 2 is the best solution.

![[Pasted image 20220830141730.png]]



#regler 