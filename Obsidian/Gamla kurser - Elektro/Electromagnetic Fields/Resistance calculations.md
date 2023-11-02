---
tags: [el]
---
# Resistance Calculations
In general, calculations of resistance can be based on the simple concept $R = \frac{l}{(\sigma S)}$, by recognizing that the conductor in question can be broken down into small parts, each having an elemental resistance dR (in which l$l,\sigma,S$ are all constants). Then, all the dR's is combined (integrated) over the varying parameter to give $R$ via either series or parallell connections.

## Recipe (Vincent)
The main challenge of using the dR approach is to make sure that the elemental volume and conductivity behavior contributing to dR is correctly identified (what is varying and what is not for the dR’s over the conductor). In general, we can formulate a recipe for calculating resistance:

1) Choose the appropriate coordinate system
2) Identify which of the parameters $l, \sigma, S$ is not constant between the terminals and write it as a function of position along the conductor (if not already given to you)
3) Identify dR for series or dG (elemental conductance) for parallel connection
4) Calculate resistance R by integrating dR (or conductance G by integrating dG, R=1/G)

## Example 1 - Cylindrical conductor
![[Pasted image 20221103155017.png]]

## Example 2 - Conically conductor
![[Pasted image 20221103155127.png|710]]

## Example 3 - Half-ring flat conductor
![[Pasted image 20221103155253.png|700]]
![[Pasted image 20221103155311.png|700]]

## How to calculate the resistance á la Ludvig
![[Pasted image 20221103155436.png]]
![[Pasted image 20221103155448.png]]