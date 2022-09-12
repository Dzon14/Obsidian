---
aliases: [stationära fel, stationära felet]
---
# Stationary Errors 
With a setpoint $\mathcal{r}$ and a load disturbance $\mathcal{l}$, we get a transfer function $$Y = \frac{G_{R}G_{P}}{1 + G_{R}G_{P}}R \ + \ \frac{G_{R}}{1+G_{R}G_{P}}L$$
### The servo problem
A case for which $\mathcal{l}=0$, where we are only interested in the setpoint tracking properties of the controller. For ex. in motor control, in vehicles etc. 
$$Y = \frac{G_{R}G_{P}}{1+ G_{R}G_{P}}R = \frac{G_{0}}{1+G_{0}}R$$
### The regulator problem
- $\mathcal{r} = 0$. 
- Studying the effect on load disturbances ($\mathcal{l}$). 
- Often in process industries
$$Y = \frac{G_{p}}{1+G_{R}G_{P}}L$$



#regler