---
tags:
  - automation
aliases:
  - markovkedja
  - markovkedjor
  - markov chain
---
# Markov Chains
- The focus on these notes will be on automation.
- Useful for manufacturing systems (a fundamental aspect of automation) that are non-deterministic, event-driven, stochastic and have disturbances. 
- To evaluate how various parameters influence overall system capacity and effiiency

## Modelling manufacturing systems
- Markov chains (discrete time)
- [[markov processes]] (continous time)
- Poission processes (continous time)
#### System to analyse
![[Pasted image 20240117165038.png|500]]
#### Two machines and one buffer
![[Pasted image 20240117165116.png|500]]
- Buffer skyddar linan från att helt stanna när en maskin går sönder

## The state of a transfer system
![[Pasted image 20240118175827.png]]

## State graph
![[Pasted image 20240117165200.png|500]]

## Example - Transfer Line
![[Pasted image 20240118180012.png]]

## Transition probability
![[Pasted image 20240117170055.png]]
#### The transition probability matrix
![[Pasted image 20240117170156.png|300]]
#### Probability distribution vector
![[Pasted image 20240117170548.png|400]]
- Sannolikheten att vara i de olika tillstånden i händelse k.
## State propagation
$$\vec{P}(k+1) = \vec{p}(k) \cdot \vec{P}$$
$$\vec{p}(k) = \vec{p}(k-1)\vec{P}=\vec{p}(k-2)\vec{P}^{2}= \ ... \ = \vec{p}(0)\vec{P}^{k}$$
- $\vec{P}$ är "the transition probability matrix".
### Small example
![[Pasted image 20240117170905.png|500]]

## Stationary solution
$\vec{p}_{stat} = \vec{p}_{stat} * \vec{P}$  equivalent to  $\vec{p}_{stat}(I-\vec{P}) = 0$
Needed extra condition: sum of $\vec{p}_{stat}=1$
This gives the average behaviour of the system. A system with a stationary solution independent of initial state is said to be **ERGODIC**. (Ergodic är typ stabil).
- To be **Ergodic** all the states must have a path to eachother.
- If there are more than one absorbing states, it is not **ergodic**
- If the system is periodic (eigenvalue = -1), it is not **ergodic**

## Periodic solution
If at least one eigenvalue of $\vec{P} = -1$ then the system is periodic
Note: it may still have a solution fulfilling  $\vec{p}_{stat}(I-\vec{P}) = 0$
![[Pasted image 20240118180925.png]]
If one of the eigenvalue is = 1 (as the row sum) it is an indicator that it is correct (???)

## Classifying states 1/2
- **Recurrent** state: probability **= 1** of sooner or later returning to that state (can be subdivided into null (inf. time) and nonnull recurrent state)
- **Transient** state: probability less than 1 of sooner or later returning to that state
- **Periodic** state: state with period $t$ if it is only possible to return to that state in $t, 2t, 3t$ ... steps
- **Absorbing** or **trapping** state, $p_{ii}(k) = 1$
#### Example
![[Pasted image 20240117171936.png|500]]
Solution:
![[Pasted image 20240118180506.png|600]]


**Absorbing state:**
![[Pasted image 20240117172151.png|400]]

## Classifying states 2/2
- A set of states are a **closed chain** if once in one of the states, the system will never leave the set. Every Markov chain has at least one closed set. 
- States i and j communicate if there is a positive probability to go from one to the other in finite time, i.e. pij (k) > 0 and pji(k) > 0 for some k If all states communicate then the system is irreducible
- If all states communicate then the system is **irreducible**

#### Example 6.8
![[Pasted image 20240117172526.png|400]]
![[Pasted image 20240117172656.png|500]]

## Recurrence probability
$f_{j}^{n} = P$ (to return to the state $j$ for the first time after $n$ steps)
$$f_{j}= \sum\limits_{n=1}^{\infty}f_{j}^{n}$$
### Example 6.3
![[Pasted image 20240117173049.png|600]]

## Mean reccurence time
$$\mu_{j} = \sum\limits_{n=1}^{\infty}nf_{j}^{n} = \frac{1}{\vec{p}_{j}}$$
Note: only holds if the system is ergodic

## Example 6.9 
![[Pasted image 20240117173752.png|400]]

## Example 6.11
![[Pasted image 20240117173837.png|500]]

![[Pasted image 20240118181116.png]]