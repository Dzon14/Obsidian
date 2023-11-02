---
aliases: [simple parity-check code, parity bit]
tags: [komsys]
---
# Paritetsbit
Simple Parity-Check Code
Extra bit to make the total number of 1s in the codeword
- Even $\rightarrow$ even parity
- Odd $\rightarrow$ odd parity

![[Pasted image 20230123154451.png|350]]

A problem with this method is that it can detect an odd number of errors only. Cannot detect if 2 bits are wrong.


- Sändaren lägger till en bit i slutet, om mottagaren jämför detta med datan och upptäcker ojämnt antal ettor i paketet så läggs en etta till, annars nolla.