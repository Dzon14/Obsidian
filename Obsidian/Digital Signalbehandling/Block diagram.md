# Block diagram
![[Pasted image 20220831081957.png|800]]
see pdf for examples. 
**Brute force:**
In short: with only "+" , add all the inputs with a delay module in between and then multiply in the end. If some operations are "-", do the same as before but a -1 multiplier for the negative ones. 
In a recursive system (still brute force): 
- We need a x(n) and y(n-1),
- multiply y(n-1) by the factor (eg. 0.9)
- add x(n) to 0.9y(n-1)
- we have y(n) in to places - connect them

#el 