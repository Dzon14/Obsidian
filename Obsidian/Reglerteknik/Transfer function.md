# Transfer function
Laplace domain!

$Y(s) = G(s)U(s)$ , 
where $G(s)$ is the model (transfer function of the system), $Y(s)$ is [[Laplacetransform|Laplace transformation]] of the output ($\mathcal{L}$(y(t)) and $U(s)$ is the laplace transform of the input 

**Good:**
- Turns things into complex analysis.
- Good for interconnection. Turns any interconnection you want to do into linear algebra. For instance, when using two process steps, you just multiply them (G1 multiplied by G2, if they are the steps)
- Handles delays

**Bad:**
- MIMO mess
- Computation is hard (should use space-state here instead)

#### One-sided [[Laplacetransform|Laplace transformation]]
![[Pasted image 20220830164036.png]]

$$\mathcal{L}(q(t))(s) = F(s) = \int_{0}^{\infty} q(t)e^{-st} \, dt$$


### The relation between State-space and Transfer function
Often one wants to alternate between working with the state space description and the transfer function. Therefore it is essential to be able to transit between these descriptions.

![[Pasted image 20220830220240.png]]
![[Pasted image 20220830220249.png]]


#regler