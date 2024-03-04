---
tags:
  - automation
---
# Real Time Control

## Real-time programming important features
- Execution flow determined by external events 
- Act on data and on external signals (sensors) 
- May explicitly refer to time
- Timing constraints
- The result cannot be predicted
- Multitasking
- The program never terminates - waits for new data (while-loop etc)

## Important Concepts
- Multitasking
- Scheduling - process states
- Resource protection
- Process synchronization
- Periodic execution

## Multitasking
- Don't have to be in real time programming, but is very common
![[Pasted image 20240208082155.png|500]]
- All statements between cobegin and coend will run concurrently
![[Pasted image 20240208082230.png]]

#### Managing Multitasking
- Divide the CPU between several processes (activities)
- Context switching
- A scheduler
- Pre-emptive scheduling
- Time slice (graph b above) - the program will run a bit slower than if each program hade its own cpu core, but the user won't notice this too much.

## Scheduling - process states

#### The states of a process
![[Pasted image 20240208084146.png|500]]

#### Scheduling strategies
- Cooperative scheduling – round robin 
- Interrupt scheduling – priorities 
- Pre-emptive scheduling
- Time-slice scheduling

## Resource Protection

#### Resources
- CPU
- Disk areas, memory cells
- I/O units
- Variables
- Bus connection

#### Mutual Exclusion
- Means that two activies can not operate on the same resource at the same time
- **Safety** – access limits have to be respected. Protected area is not accessed by more than 1 process at a time 
- **Liveness** – a program is supposed to do what it is meant to do. No indefinite blocking

#### Creating a Deadlock
- Two processes P1 and P2 
- Two resources r1 and r2(a certain I/O or a certain memory position) 
1. P1 reserves r1 and P2 reserves r2 
2. P1 needs also r2 and will wait for P2 
3. P2 needs r1 and will wait for P1

#### Deadlock
![[Pasted image 20240208085049.png|500]]
- Avoid this
#### Conditions to Create Deadlock
- **Mutual exclusion** – some resources can only be reserved by 1 process at a time 
- **Non-preemptive allocation** – a resource can only be released by the one that made the reservation 
- **Successive allocation** - You can take one resource after the other
- **Inverse allocation**
Enough to break ONE of these conditions to avoid a deadlock!!!

#### The Race Condition
![[Pasted image 20240208085552.png|450]]
- Some operations may not be interrupted! For instance, both processes here will store x (which has different values in both)

#### Using Semaphores
- To solve the problem above
Semaphore sem – an integer 
**Signal:** increase the value with 1 (unconditionally) 
**Wait:** if sem>0 the decrease the value with 1; 
	otherwise wait

#### Semaphore example - Protecting Resources
![[Pasted image 20240208092533.png]]
By using this technique, whe cannot be at the same (protected resource) at the same time - ok
- To use semaphore we need a hardware component - test_and_set

## Process synchronization

#### Synchronization (single-sided)
![[Pasted image 20240208092748.png|550]]

## Periodic execution
![[Pasted image 20240208093543.png|550]]

## Real-time Programs
- Be ready to run
- Never terminate
- If not running - wait
- Running efficiently
- Structured (difficult to debug!)

## Real-time Language Features
- Definition of processes that can be executed in parallel 
- Priority driven process switch 
- Synchronization 
- Data exchange among processes 
- Direct access to external hardware 
- Time related functions 
- Interrupt and exception handling