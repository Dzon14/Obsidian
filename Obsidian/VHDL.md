# VHDL 
- En typ av [[Hardware Description Language]]
"Very high speed integrated circuit Hardware Description Language"
Invented 1980
- Standardize documentation of hardware
- Mycket av VHDL går inte att använda för att realisera kretsar, utan mer att simulera

## Alternatives to VHDL
- Verilog
- SystemVerilog

##### Högre nivå:
- SystemC
- CatapultC
- MatLab

## Structure of VHDL
A Source file including:
- Library: Predefined types, Reuse designs
- Entity: Name of the module, Inputs/Outputs, Parametrization
- Architecture: Behavioral description, Use of subcomponents
- Package declaration
- Package body
- Configuration

## Objects in VHDL
Four kind of objects:
- Signal: can be viewed as a wire (or wire with memory) in a hardware. All input and output ports declared in the entity are signals.
- Constant: A wire with constant value. Can be declared in the architecture
- Variable: SOMETIMES viewed as a wire in hardware (depends on how u describe the circuit, better to use signals)

## Data types in VHDL
- INTEGER
- BOOLEAN
- BIT (0 or 1)
- BIT_VECTOR (1-dim array of BIT)

## VHDL Operators
Around 30 operators. Some are:
- not
- and
- or
- xor
- nand
- nor
- xnor

The operater <= is used to assign value to a signal
The operator := is used to assign value to a constant.

[[Simple Signal Assignment]]
[[Conditional Signal Assignment]]
[[Selected Signal Assignment]]
[[Structural Design]]
[[Testbench]] 
