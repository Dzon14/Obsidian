---
tags: [komsys]
---
# Seminarium 1 - KomSys

## Lab 1 - Physical link lab: Five tasks
1. Select LED = decide message (application layer)
2. Transmit pre-defined frame (check outcome on MasterNode)
3. Create your own frame (combo of task 1 and 2)
4. Receive pulses and decode symbols (Physical layer)
5. Expand task 4: detect SFD and decode frame (Link Layer)

## Lab 2 - The Data Link lab: Three tasks
1. [[adressering]]
2. [[felhantering]]
   - ARQ
3. [[feldetektering]]
   - [[cyklisk redundanscheck|CRC]]

## Physical devices/tools
- Master node - Ready for use
- Access point - Ready for use
- Development Node - Den vi ska implementera

## The layered model
"Divide and conquer"
Three layers:
- Application - assign to [[addressering|adress]] and select LED
- Link - adressing, ARQ , CRC
- Physical - Transmit and receive
Interfaces are used to communicate between the layers.


+