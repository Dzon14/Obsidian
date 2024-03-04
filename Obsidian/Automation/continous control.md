---
tags:
  - automation
---
# Continous control concepts 
- Reglerteknik kopplat till automatinskursen

## Important controller concepts
- Open loop
- Closed loop
- Feed-forward
- Feedback
- Stationary error
- Stability
- Time delays

## Some control ideas
- Simple controllers – PID 
- Cascade control 
- State feedback 
- Feed forward automation 
- More advanced control

## Feedback controller
![[Pasted image 20240214142824.png|500]]

## On-off controller
![[Pasted image 20240214143019.png|500]]
![[Pasted image 20240214143532.png|400]]
## Proportional (P) control
![[Pasted image 20240214143121.png|400]]
- e är skillnaden mellan ut och insignalen (felet)
![[Pasted image 20240214143351.png|400]]

## Stationary error
- When e $\Rightarrow$ 0, u $\Rightarrow$ 0
- One option: increase gain (P)
	- May lead to instability
- Better option: introduce integral action 

## Integral action
![[Pasted image 20240214143902.png|500]]

#### PI-control
![[Pasted image 20240214143943.png|500]]

## The PID controller
![[Pasted image 20240214144010.png|450]]

## Test model - 3 tanks in series
![[Pasted image 20240214144104.png|500]]
#### Tanks in series
![[Pasted image 20240214144225.png|400]]

## P-control
![[Pasted image 20240214144250.png|500]]

## PI-control
![[Pasted image 20240214144518.png|500]]

## PID-control
![[Pasted image 20240214144533.png|500]]
No (or marginal) oscillations but slow

### P vs PI control - step change
![[Pasted image 20240214144623.png|400]]

### PI vs PID control - step change
![[Pasted image 20240214144647.png|400]]

## Ziegler Nichols tuning
1. Turn the controller to P-only mode, i.e. turn both the Integral and Derivative modes off. 
2. Note if control gain is positive or negative. 
3. Apply the input. 
4. Change $K$ in step increments and wait for a steady state. 
5. Increase until sustained periodic oscillation and note the critical $K_{u}$
6. Note the period of the oscillation, $P_{u}$
![[Pasted image 20240214144922.png|200]]
IMPORT EXAMPLE HERE
## Tyreus-Luyben Tuning
- Same procedure to find $K_{u}$ and $P_{u}$
- Less aggressive - less oscillations
![[Pasted image 20240214145011.png|250]]

### Comparison in tuning
![[Pasted image 20240214145036.png|400]]

## Imroving the performance
- Cascade control
- State feedback
- Feed-forward

### Cascade control
![[Pasted image 20240214145146.png|500]]
![[Pasted image 20240214145902.png|500]]
![[Pasted image 20240214145918.png|500]]
![[Pasted image 20240214150004.png|500]]
![[Pasted image 20240214150019.png|500]]
- The stationary error is easily removed by integral action on the outer loop 
- Only one integral action
	- If the time constants of the loops are close they can start working against each other 
- More than one integral action possible if the time constants are different 
- In practice: the inner loops are typically sampled faster
##### Cascade control - alternative representation
![[Pasted image 20240214150126.png|500]]
![[Pasted image 20240214150209.png|500]]
- Close to state feedback.
### State feedback
![[Pasted image 20240214151546.png|400]]
- Feed back states to controller 
- Pole placement used for controller design
	- Hand calculations for small (2nd order) systems
	- Matlab for larger systems 
- If all states measurable
	- Control can be made fast (if no limits on the control action)
- Price: many sensors

#### Concentration in 3 tanks
![[Pasted image 20240214153832.png|500]]

#### State feedback 3 tanks in series
![[Pasted image 20240214154006.png|500]]
#### Example: control design
![[Pasted image 20240214154842.png|550]]
![[Pasted image 20240215082759.png|450]]
If we take a factor 12:
![[Pasted image 20240215082907.png|450]]

### Feed-forward
- **Measure** the refernce value or the disturbance before it hits the plant
- **Compensate** for the disturbance before it has affected the plant
- **The price**: must supply a model of the influence of the disturbance
![[Pasted image 20240215083155.png|500]]
- No feedback – no guarantee that $y_{ref}$ is achieved 
- Need a perfect model between $v$ and $y$
- Often sufficient for control

#### Feed forward + feedback
![[Pasted image 20240215083424.png|300]]
- You can also have feed forward from reference (insteaed of disturbance)
- Furthermore, you can have FF from both Ref and Disturbance (see lecture slides)

## Time delays
- Time delays in the process
	- Delay in the physical process 
	- transport, slow dynamics
	- Delay in the measurement of the variable
	- Delay in the control action 
- May introduce oscillations 
- Makes the control slow
	- Control parameters must be moderate
![[Pasted image 20240215084047.png|450]]
- With no delay we can have a good control, otherwise it can be unstable
**Solutions:**
- Use moderate control parameters
- Use controller with delay compensation
	- Smith predictor

### Smith predictor
![[Pasted image 20240215084222.png|450]]
- $e^{-sT}$ is the delay
- We can get a 0 error.

## Some practical limitations
- Control actions
	- Amplitude
	- Direction 
- Measurement
	- States – are they possible to measure?
	- Disturbances – are they possible to measure?
	- Noise 
- Time varying process
	- Process behaviour not constant

## The windup problem
![[Pasted image 20240215094818.png|500]]

### Changing the D part
![[Pasted image 20240215094837.png|500]]

### Noise filtering of the D part
![[Pasted image 20240215094904.png|350]]

### Adaptive controller
![[Pasted image 20240215094926.png|450]]

## Predictive control
![[Pasted image 20240215094945.png|500]]
![[Pasted image 20240215095002.png|500]]