---
tags: [el]
---
# Sequential circuits
The output depends not only on current input but also on past. 
A memory is needed to implement this.
FPGAs typically contain D-type flip-flops (D FF) and D-type latches (D-latch).

## Signal Assignment
Inside a [[Process in VHDL]] we can use that
- Sequential statement
- if/else statement
- case statement
![[Pasted image 20211108094934.png|150]]

**We cannot use:**
- [[Selected Signal Assignment]]
- [[Conditional Signal Assignment]]