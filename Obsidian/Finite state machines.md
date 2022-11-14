---
tags: [el]
---
# Finite state machines
Usually it is described in two divided parts (two processes), The combinational part and the memory
![[Pasted image 20211108100624.png|500]]

## Creating a Data type
In the architecture you can create your own data types:
```VHDL
type state is(start, pause, stop)
```
Example: (A state machine with two states)
![[Pasted image 20211108101224.png]]
**The Combinational part:**
![[Pasted image 20211108101303.png|300]]
**Memory part:**
![[Pasted image 20211108101345.png|300]]

## Unintentional Latch
**A common mistake when describing FSM is that the designer forget to always assign values to the output of the combinational part of FSM. **
![[Pasted image 20211108102151.png|300]]
Always se default values!