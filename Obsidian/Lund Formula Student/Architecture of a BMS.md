# Architecture of a BMS

The different parts of BMS
![[Pasted image 20220914223409.png|700]]

### BMS master
- MCU
- Communication interface and shutdown circuit control
- Pre- and discharge
- Calculate SoC and SoH
- Monitor charging
- Communication with slaves, current sensor and rest of LV

##### High voltage card
connected to the BMS master
- Pre-/discharge
- Indicator light

##### Isolation monitoring device 
connected to the BMS master
- Measure isolation (resistance) between HV+, HV- and low voltage ground

### Battery pack and Slave configuration 
- 130 cells in series
- 5 segments with 26 cells
- 5 slave modules per segment - 25 in total 
- Each slave module measures 4 or 6 cell voltages and every second cell temperature
- Communicate through a daisy chain of isoSPI

### Sensor and slave boards
 - On top of each segment 
 - Voltage- and temperature sensors
 - Battery stack monitoring IC
 
### Current sensor
 - Hall effect sensor

#lfs