---
aliases: [Field Programmable Gate Array]
tags: [el]
---
# FPGA - Field Programmable Gate Array
- Programmerbar
- Använder D-[[vippor]].
- "Look-up tables"

[[EDA]] - Ett program för att programmera FPGA.

### FPGA Design Flow
En 8 stegs process.
##### Design Entry
Different entry points:
- Schematic
- Hardware Description Language (HDL)
- High Level Synthesis (HLS)

Constraints:
- Clock frequency
- Signal delay
- Power consumption
- Connection to pins of FPGA

##### Simulation
Behavioral simulation/RTL simulation:
- Verify functionality of design
- Relatively fast simulation
- No information on delays
- No information of resources

##### Synthesis
Translates/Maps design to device resources:
- Lock-up tables (LUTs)
- Flip-flops
- Latches
- Adders
- Multipliers
- Memory
- (fyll i sen)
- Generates a netlist of the design

Efter detta är det implementering, simulering, Timing analysis, Programming och testing. 