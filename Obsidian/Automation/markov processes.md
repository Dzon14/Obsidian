---
tags:
  - automation
---
# Markov processes

## Fundamentals
- Transitions in discrete time -> Markov chain
- When transitions are stochastic events at arbitrary point in time -> Markov process
- Continous time description
- Consider the time interval $\Delta t$ 
- Probability for state transition: $a \cdot \Delta t$
- Parameter $a =$ intensity 
- (e.g. production rate, repair rate), dimension 1/time

## State graph
![[Pasted image 20240118164644.png|350]]

## State transition
$P[s_{i}(t)] =$ probability to be in state $s_{i}$ at time $t$. 
Probability for transition from $s_{i}$ to $s_{j}$ during the time $\Delta t$ is $a_{ij} \cdot \Delta t$
![[Pasted image 20240118165017.png|500]]

##### Probability of no transfer
Can be expressed as: $$1 -  (\text{prob to leave the state } s_{j}) = 1 - \sum\limits_{i \neq j}^{m}a_{ji} \Delta t$$
## State transition cont. 
![[Pasted image 20240118165312.png|400]]
![[Pasted image 20240118165435.png|300]]
![[Pasted image 20240118165526.png|300]]

#### Probability vector
$\vec{p}(t) = (p_{1},p_{2},...,p_{m}) = (P[s_{1}(t)] \ P[s_{2}(t)] \ ... \ P[s_{m}(t)])$
Note: a row vector! Sum of $\vec{p}(t) = 1$

## State transition cont. 
![[Pasted image 20240118170023.png|400]]

## Stationary solution
$$0 = \vec{p}(t) \cdot \vec{A} = \vec{p} \cdot \vec{A}$$
must use the extra condition: sum($\vec{p}$) $=1$ (IMPORTANT)
Interpretation: $$\text{flow of events} = \text{rate} \cdot \text{probability}$$
In stationarity: $$\text{the flow of events into } s_{i} = \text{ the flow of events out of } s_{i}$$
## Simple example
**NOTE**: This method is only for 2x2 matrices. 

![[Pasted image 20240118170414.png|400]]
![[Pasted image 20240118181314.png|550]]

![[Pasted image 20240118170535.png|400]]

## Special case of the markov process: [[the poisson process]]

## Examples
![[Pasted image 20240125152549.png]]
![[Pasted image 20240125152608.png]]![[Pasted image 20240125152713.png|550]]
