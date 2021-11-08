# Testbench
[[VHDL]] can be used to create testbenches that can generate input patterns to a circuit that we test during simulation.
- A testbench is not intended to be used during synthesis
- ALl features of [[VHDL]] can be used during testing
- Typically you first test individual modules. then subsystems and last the full system
- Create an instance of a module, generate input patterns, observe the output and compare with specification

## Basic structure of testbench
![[Pasted image 20211103115216.png]]
## Testbench using [[Signal buses|signal bus]]
![[Pasted image 20211103115535.png]] 
## Wave window
![[Pasted image 20211103115641.png]]

## Assert Command
![[Pasted image 20211108103229.png|500]]

## Testbench for [[Sequential circuits]]
To simulate a synchronous circuit we must generate
- Clock signals
- Input patterns
We need two processes in VHDL for this. 

#### Clock generator
![[Pasted image 20211108103505.png]]

#### Input generator 
![[Pasted image 20211108103603.png]]

 