---
aliases: [signal bus]
---
# Signal Buses
Signal buses is a more convenient way of treating multiple bits or wires. 
It's used in large scale circuit diagrams.
## Benefit of Signal buses
We group together signals which is a more compact way of treating signal.
Easy to perform addition etc. 
![[Pasted image 20211103112201.png|400]]

## Signal Bus Assignment
 ![[Pasted image 20211103112414.png|400]]

### Ways to assign value
![[Pasted image 20211103112617.png|400]]

### Aggregating Vectors
common in [[VHDL]]. We glue/concenate vectors together
It's done by using "&"

### Downto or To?
using "To" is the reverse of Downto. For ex: if $(Z_2, Z_1, Z_0) = (1,0,0)$ 
"2 downto 0" gives bit 2 as 1 and bit 0 as 0. If we use "2 to 0" bit 2 is 0 and bit 0 is 1.
Do NOT mix these together, stick to either Downto or To.