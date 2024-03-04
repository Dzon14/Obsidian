---
tags:
  - automation
---
# Production control

## Criterias 
- Minimize the production time
- Minimize the production costs
- Satisfy delivery dates

	- Minimize buffers and inventory
	- Minimize idle time
	- Minimize average waiting time

## Time scales in production control
![[Pasted image 20240131153735.png|500]]
As a pyramid: ERP - MES - Control
ERP - Enterprise Resource Planning
MES - Manufacturing Executional System

## Levels of control
- Production level (long term planning)
	- Finding the right production rate
	- Finding an appropriate inventory to meet demand 
- Cell level (short term planning)
	- Routing (which way?)
	- Scheduling (in what order?) 
- Machine level
	- Control of sequential operations (PLC)
	- Control of continuous processes/movement (e.g. PID)

## Long term planning
![[Pasted image 20240131154053.png|350]]
Underneath the demand - failure
Above - production
#### Hedging point strategy
- How to find the “optimal” size of inventory 
- Strategy for planning production rate on a hourly and daily (and longer) basis 
- Machines will break and production will be disturbed 
- Keep the expected average xj(t) close to zero
- To get the "optimal" buffer size (H) we need to estimate:
	- The demand, $d$
	- The mean time between failurse (MTBF), $T_{f}$
	- The mean time to repair (MTTR), $T_{r}$
- We also need to define the time period for the analysis, $T$ and the number of failures, $N_{f}$  
$$N_{f}= \frac{T}{T_{f}+T_{r}}$$
#### One breakdown
![[Pasted image 20240131155333.png|350]]
Minimize $g(H)$!!!!!
- Can't deliver at negative
- H is optimal for inventory
- Repaired at B, maximum production after (U) with the slope U-d. Lastly back to optimal inventory
- We can calculate the cost with $g(H)$.
#### Hedging point calculations
![[Pasted image 20240131155601.png|500]]
- In the book, do not learn this. 

#### Hedging point control strategy
- To control the hedging point
![[Pasted image 20240131162021.png]]
- Remember H is optimal inventory level

## Short term planning
- Routing
	- A products path through the machines
	- Not treated here, assumed to be known
- Scheduling
	- The order in which different products are produced.
	- Sequencing
(The book is a bit confusing on this)

#### Complexity
- Type of plant
	- Flow shop, job shop
- Arrival pattern
	- Dynamic, static
- Level of detail
	- Failure rates, uncertainty
![[Pasted image 20240131162226.png]]

#### Criteria for scheduling
- Production time
	- Average time in shop 
- Idle time of machines
	- Waiting time 
- Average lateness of product
	- How late (or early) is the product in respect to due date
- => minimizing costs (operating, inventory)

#### The sequencing problem
![[Pasted image 20240131162334.png|550]]

#### One maching and n jobs (n/1)
![[Pasted image 20240131162404.png|500]]
![[Pasted image 20240131162457.png|400]]
![[Pasted image 20240131162515.png|500]]
If Lateness is negative, count it as 0?
![[Pasted image 20240131162548.png|500]]

#### Prioritizing
- Sometimes it is necessary to prioritize a job.
- Weight can be used to order the production: $$ \frac{P_{1}}{w_{1}} \leq \frac{P_{2}}{w_{2}} \leq ... \leq \frac{P_{n}}{w_{n}}$$
#### Two machines and n jobs (n/2)
Two cases:
- Without buffer between machines
- With buffer between machines
![[Pasted image 20240131163050.png|550]]

#### Processing time - Gantt chart
![[Pasted image 20240131163120.png|550]]

#### Minimizing the processing time
**ALWAYS AT THE EXAM**
Johnson’s procedure 
- Choose the shortest time of Pi,1 and Pi,2 
- If shortest job time is on M1 
	- put this job first 
	- else
	- put this job last
- Eliminate the job from the list and repeat
![[Pasted image 20240131163450.png|600]]
**Solution:**
![[Pasted image 20240131165147.png|400]]
**Another example:**
![[Pasted image 20240205153729.png|600]]
#### n/3 problem
- Can be solved under certain conditions:
	- Same order for all jobs, i.e. flow shop
	- if M2 (the machine in the middle) is completely dominated by either M1 or M3
	- This is true if:
 ![[Pasted image 20240131164308.png]]
- Introduce virtual machines M1' and M2'
![[Pasted image 20240131164346.png]]
- Apply Johnson's procedure

#### Flexible manufacturing
- If the order of operations is not the same for all jobs? 
- Can be solved in some special cases 
- Optimal solution often not possible
- Graphical approaches used

#### Two jobs and m machines (2/m)
![[Pasted image 20240131164516.png|500]]
- Finding the shortest path 
	- 45 degree angle (direction) 
- Can be extended to 3/m
	- Computer solution
- Count the squares for time units. You cannot just choose a point and estimate the time.
**Another example:**
![[Pasted image 20240205154254.png]]
![[Pasted image 20240205154334.png|700]]
