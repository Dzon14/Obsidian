---
tags: [elmagi]
---
# Inductances
In [[magnetostatics|magnetostatic]]s, the inductance of [[magnetic circuits]] is defined in terms of total [[magnetic flux]] generating (or linking) capability of the current-carrying circuits. 
($I \text{ or } \Phi$)
![[Pasted image 20221128104226.png]]
We can now define the following

## Self inductance 
We can define the self inductance $L_{11}$ as the proportionality constant, $$\Phi_{11} = L_{11}I_{1}$$, where the unit is $[H]$ (henry).

## Magnetic flux linkage
$C_{1}$ can consist of $N_{1}$ turns in general, so we can define the magnetic flux linkage as $$\begin{align} &\Lambda_{11} = N_{1}\Phi_{11} = L_{11}I_{1} \ \ \ [Wb] \ \ \ \text{ in which case: } \\ &L_{11}= \frac{\Lambda_{11}}{I_{1}} \ \ \ [H] \end{align}$$where $L_{11}$ is the inductance of N-turns. 
$\Rightarrow$ Self-inductance of loop $C_{1}$ is the magnetic flux linkage per unit current in the loop itself.

## Mutual inductance 
(Still referring to the circuit figure). We note that som flux lines originated from loop $C_{1}$ also flows through loop $C_{2}$ by the amount $\Phi_{12} = \int\limits_{S_{2}}^{} \vec{B}_{1} \cdot \ d \vec{s}_{2} \ \ \ [Wb]$
We define the mutual inductance $L_{12}$ as proportionaly constant for $\Phi_{12} \propto I_{1}$, for ex  $\Phi_{12}= L_{12}I_{1}$. 
- More generally, if loop $C_{2}$ consists of $N_{2}$ turns then the magnetic flux linkage is $\Lambda_{12}= N_{2}\Phi_{12}= L_{12}I_{1}$
  $\Rightarrow$ $L_{12} = \frac{\Lambda_{12}}{I_{1}}$
  $\Rightarrow$ Mutual inductance between two circuits is the magnetic flux linkage with one circuit per unit current in the other circuit. 
- $L_{12} = L_{21} = M$

Notes: 
1) For linear circuit, inductance is a physical property (like capacitance). It is a function of the geometrical shapes and physical arrangements of the conductor circuits, as well as the permeability of the medium. 
2) When $I_{1}, I_{2} \neq 0$, the total magnetic flux linkages are: $$\begin{align} \Lambda_{1}= \Lambda_{11}+ \Lambda_{21} = L_{11}I_{1} + L_{21}I_{2} \ \ (\text{loop }C_{1})  \\ \Lambda_{2}= \Lambda_{12}+ \Lambda_{22} = L_{12}I_{1}+L_{22}I_{2} \ \ (\text{loop }C_{2})\end{align}$$
3)  $L_{21}= L_{12}$ by reciprocity. May be easier to calculate one than the other. 

## Recipe (to find inductance)
1) Choose an appropiate coordinate system to find $\vec{B}_{1}$ (or $\vec{B}_{2}$)
2) Assume a current $I_{1}$ (or $I_{2}$) on a circuit. 
3) Find $\vec{B}_{1}$ (or $\vec{B}_{2}$) using [[Biot-Savart law]] or the two tools of [[Ampere's circuital law]] and [[vector magnetic potential]].
4) Find flux linkage for each turn $$\begin{align} &\Phi_{11}= \int\limits_{S_{1}}^{} \vec{B}_{1} \cdot \ d \vec{s}_{1} \ \ \ [Wb] \ \ \ (\text{Or calc. } \Phi_{22}) \\ &\Phi_{12} = \int\limits_{S_{2}}^{} \vec{B}_{1} \cdot \ d \vec{s}_{2} \ \ \ [Wb] \ \ \ (-||-)\end{align}$$
5) Find self and mutual inductance by $$L_{11}= \frac{\Lambda_{11}}{I_{1}}, L_{12}= \frac{\Lambda_{12}}{I_{1}} \ \ \ (\text{or for }L_{22})$$
## Example 1
![[Pasted image 20221128111933.png]]

## Example 2
![[Pasted image 20221128111954.png]]
![[Pasted image 20221128112014.png|660]]