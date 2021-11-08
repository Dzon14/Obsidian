## Process in [[VHDL]]
- A process can be viewed as a sub circuit within an architecture
- A process has a sensitivity list which specifies which signals will trigger it
- When one of the signals in the sensitivity list changes value, the process is activated
- Statements within it are evalueted in sequential order
- At the end outputs of the process are updated with the latest value assigned in the process and the process is suspended. 

### Syntax of a Process
![[Pasted image 20211108094700.png]]