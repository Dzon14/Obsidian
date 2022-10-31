---
aliases: [stability, stable, stabil, stabila, stabilt]
---
# Stabilitet
If all [[poles]] are in the left side of the complex plane.

**Stability** - A linear dynamic system is stable if $x(t)$ is bounded for all initial states if 
$u(t) = 0$.

**Instability** - A linear dynamic system is unstable if there exists a initial state, which results in an unbounded state $x(t)$ when $u(t) = 0$.

**Asymptotic Stability** - A linear system is asymptotically stable if $x(t) \rightarrow 0$ as $t \rightarrow \infty$ for all initial states if $u(t) = 0$.

$$\text{Asymptotic stable} \Rightarrow \text{stable}$$

### Example
$$x(t) = x_{0}e^{at}$$
Depending on the sign of a we get three cases, $$\begin{cases} a < 0 \ \ \ \  \text{Asymptotically stable} \\ a = 0 \ \ \ \ \text{Stable} \\ a > 0 \ \ \ \ \text{Unstable}\end{cases}$$
## Diagonal case
The stability concept can also be determined from the eigenvalues of a diagonal matrix. 

1. If all eigenvalues of the A matrix have negative real parts, the system is asymptotically stable.
2. If any eigenvalue of the A matrix has positive real part, the system is unstable.
3. If all eigenvalues of the A matrix have negative or [[Zeros|zero]] real parts, the system is stable.


#regler