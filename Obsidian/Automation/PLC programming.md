---
tags:
  - automation
---
# PLC programming

The standard IEC 61131-3 implies: 
- Definition of sequential function chart (SFC), and 4 language options
	- Instruction List (IL)
	- Function block (FBD)
	- Ladder diagram (LD)
	- Structured text (ST)

## Ladder Diagram / Ladder programming
#### Ladder Framework
![[Pasted image 20240131145122.png|300]]

#### Ladder Symbols
![[Pasted image 20240131145141.png|500]]

#### Boolean Logic in LD
![[Pasted image 20240131145247.png|400]]

#### Set - Reset in LD
- State implementation
![[Pasted image 20240131145355.png|400]]

#### Reflections
- A relay has only one coil, consequently we use only one coil symbol with the same name. 
- An arbitrary number of make/break elements can be used in a ladder diagram.
- Symbols may be physical or logical in a PLC.

### An elementary PLC structure
![[Pasted image 20240131145702.png|400]]

#### State encoding in LD
![[Pasted image 20240201091748.png|400]]
- If Relay coil (B) is activated, we are in the B state.
- A and x - set condition?
- The encoding of state C:
![[Pasted image 20240201100759.png|300]]
- we do not leave B until we have reached C, then we know we have reached B before
	- C will be set while B is set
- B becomes false before C becomes true?
- See example for seq control in [[control implementation]].

#### Alternative State Transitions
![[Pasted image 20240201093817.png]]
- C and D are always in series (both cases). If in parallel (C and D) - it doesn't work. 
- y and z must NOT be true at the same time (cus then we go to both C and D - two active states, which is a problem if it is not our intention)
- To be safe you can inverse one of them and then put it with the other with AND. (y AND z-inversed, for ex.)

#### Several ways to Enter a State
![[Pasted image 20240201094136.png|400]]

#### Using INIT
![[Pasted image 20240201100924.png]]

#### Example
![[Pasted image 20240207134908.png]]
![[Pasted image 20240207154859.png]]
![[Pasted image 20240207154909.png]]
## Instruction List (IL)

## From ladder to PLC code
Ladder and IL can always be directly translated
![[Pasted image 20240207154714.png]]
ldi - load inverse
![[Pasted image 20240207163852.png]]
orb - or block. Orb operates on both and puts it in the lower end of the stack
Orb takes the lowest two blocks in the stack

## From Boolean to PLC
![[Pasted image 20240207155227.png|500]]
and - and block. Orb but it does and istead

## Function Block Diagram
![[Pasted image 20240207155316.png]]
- 30 seconds before Q1 is true (T#30s). Timer on delay, not timer off.
- Superior language in some applications
## Structured Text (ST)
![[Pasted image 20240207155420.png]]
- Strongly resembles Pascal
- := is an assignment.

## Sequential function chart (SFC)
![[Pasted image 20240207155701.png|500]]

## Controlling a simple Batch Tank
![[Pasted image 20240207155733.png|600]]

## The sequential function chart
![[Pasted image 20240207155857.png]]

## The finite state concept
- The process is represented by 5 states
- Only 1 state at a time! 
- A transition signal marks the change from one state to another one 
- A condition for transition (from a sensor, a timer, an operator)
- In each state there is an action

## Grafcet
- Developed in France 1977 
- Graf + AFCET (Association Francaise pour la Cybernetique Economique et Technique) 
- French standard 1982 
- IEC standard 1988 - IEC 848 (=SFC, Sequential Function Chart)
- Essential part of IEC 61131-3

### Alternating Parallel Branches
![[Pasted image 20240207160131.png|300]]
Conditions at both places

### Grafcet for a Drill
(Alternating parallel branches)
![[Pasted image 20240207160204.png|500]]

### Simultaneous Parallel Branches
![[Pasted image 20240207161824.png]]
A double line after the condition (only ONE condition) which means: if condition true, we start the parts simultaneously.
It ends with double line, which means both paths must have finished, then the condition after the bottom double line will be true. 

#### Implemented with ladder:
![[Pasted image 20240207162143.png|500]]
Error in the book, page 493. 

## Batch Operation
- From a batch we can get SFC?
- We ask the batch if we can get something?
#### Structure of a Batch Operation
![[Pasted image 20240207163035.png|500]]

#### Important Concepts
- Process cell 
- Process unit 
- Batch 
- General recipe 
- Control recipe 
- Phase

#### Batch - from the start
![[Pasted image 20240207163155.png|500]]

#### Batch
![[Pasted image 20240207163225.png|450]]
- Identify phases and parameters for each unit
	- Raw material (sort, volume) 
	- Mixing (time, speed) 
	- Temperature control (setpoint value) 
	- Empty (time)
- Write the executing of the recipe $\Rightarrow$ becomes a SFC program

#### Batch - several units
![[Pasted image 20240207163345.png|500]]
