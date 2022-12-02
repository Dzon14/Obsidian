---
tags: [el]
---

## Reducerad form av [[Linear Sequential Circuit|linjära sekvensnät]]
1. Ta fram [[Diagnostic Matrix|K-matrisen]] och räkna ut dess [[Rang]]. Om rangen är mindre än antalet rader så går kretsen att minimera. 

2. Bilda en ny matris T genom at ta de X första raderna från K.  (X=rangen) 

3. Hitta en [[Invers Matris#Högerinvers|högerinvers]] R till T
Tänk att $$T = \begin{pmatrix}M N\end{pmatrix}$$ där M är en [[Kvadratisk Matris]]. För att bilda M tar man tre [[linjärt oberoende]] kolumner från T. Hitta $M^{-1}$ istället. 
$$R=\begin{pmatrix}M^{-1}\\0\end{pmatrix}$$
man kan alltså skita i N, då den kommer multipliceras med nollan.

4. För att hitta den reducerade formen multiplicerar man sedan sina matriser A, B, C och H (se [[Linear Sequential Circuit|linjära sekvensnät]]) på följande vis:
![[Pasted image 20211028104922.png]]