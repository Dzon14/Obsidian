---
tags:
  - automation
---
# The Poisson process
- Special case of the Markov process 
- The prob. for an event during the time interval $\Delta t$ is $\lambda \cdot \Delta t$ 
- Only 1 event at a time 
- *No memory*: the number of events within $[t1,t2]$ independent of the number of events within $[t3,t4]$ (no overlap) 
- Time intervals between events are independent and exponentially distributed 
- Average waiting time $1/\lambda$ 

## A birth process - a generalisation of a poisson process
- It defines a continuous process which takes values in the natural numbers and can only increase by one (a "birth") or remain unchanged.
- Describes the arrival pattern
- Arrival rate $\lambda$
![[Pasted image 20240118171639.png|500]]

## Simple transfer line - a birth process
![[Pasted image 20240118171707.png|600]]

## The transfer line generator
![[Pasted image 20240118172646.png|600]]

## Transfer line solution
![[Pasted image 20240118172743.png]]
#### Transfer line process
Input + 4 machines + output $\rightarrow$ 6 states
![[Pasted image 20240118172928.png|500]]

## Work in progress
![[Pasted image 20240118173006.png|550]]

## Superposition
![[Pasted image 20240118173213.png|500]]

## Decomposition
![[Pasted image 20240118173315.png|400]]

## Birth-death process
- Deaths decrease the state by one (birth increases by one).
![[Pasted image 20240118173350.png]]

## Birth-death generator
![[Pasted image 20240118173714.png]]

## Two machines and one buffer
![[Pasted image 20240118173743.png|550]]

## State graph
![[Pasted image 20240118173804.png|550]]

## Probability vector
$$\vec{p}(t) = [p_{000},p_{001},...,p_{N11}]$$
## Isolated machine efficiency
![[Pasted image 20240118174015.png|500]]

## System efficiencies
![[Pasted image 20240118174044.png|500]]

## Total system production
$$P_{s}= \mu_{1} \cdot E_{1} = \mu_{2} \cdot E_{2}$$
## Average buffer size
$$\vec{n} = \sum\limits_{n=0}^{N}\sum\limits_{\alpha_{1}=0}^{1}\sum\limits_{\alpha_{2}=0}^{1}n \cdot p(n, \alpha_{1}, \alpha_{2})$$