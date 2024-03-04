---
tags:
  - automation
---
# Control implementation / Combinatorial and Sequencing control

## Combinatorial vs Sequential
- Combinatorial - no memory 
	- Only depends on current signals
- Sequential - contains state(s)
	- Next state is a function of: 
		- Current inputs
		- Current state
Applicable for:
- Machine and/or Control system

## Example: Combinatorial Control
![[Pasted image 20240131144211.png|500]]
## Example: Sequential Control
![[Pasted image 20240131144308.png|550]]
Consequently:
- The controlled machine may contain states
- The controller may contain states
- The macro view of controller and machine contain states if any subsystem contain states.
![[Pasted image 20240201100857.png]]

## Focus on the Controller
- Monst controllers are sequential
- Is this a sequential controller? :
![[Pasted image 20240131144546.png|500]]
if yes . where is the state?

## Event Driven Systems - State Concept
![[Pasted image 20240131144655.png|500]]

## Sequential Control Tools
- State diagrams
- Petri nets
- Sequential Function Charts - Grafcet
- Switching theory 
- PLC languages IEC61131

## [[PLC programming]]

### The classical Transfer Line
![[Pasted image 20240207151724.png|500]]

## Simple Cell
![[Pasted image 20240207151829.png|500]]

## Petri Net of the simple cell
![[Pasted image 20240207151926.png]]
One product (token) in the machines at a time.

## The manufacturing cell
![[Pasted image 20240207152426.png|550]]
![[Pasted image 20240207163745.png]]
## Controlling the Cell
![[Pasted image 20240207153059.png|550]]
- The scheduler keeps everything in order, errors as in the example above won't happen.

## Two different developments
![[Pasted image 20240207154210.png|500]]
- Ladder programming is at the manufacturing industry part. However, it is on its way out, but many company still prefers it.

## Sequential Control tools
Where we are now:
![[Pasted image 20240207154306.png|500]]

## Elementary Boolean expressions
![[Pasted image 20240207154330.png]]

## De morgans theorem
![[Pasted image 20240207154343.png|400]]

## Back to [[PLC programming]]