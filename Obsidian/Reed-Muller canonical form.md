---
aliases:
 - "RMF"
 - "RSE"
 - "Ring sum expansion"
 - "ANF"
---


Finns fyra sätt att ta fram RMF:
1. Byt ut and och or med hjälp av [[Boolean Algebra#Räknelagar|de boolska räknelagarna]]
Om man utgår från ett uttryck från en [[Karnaugh Map|karnaugh mappen]] där inga termer överlappar så blir termen ab=0 i a+b+ab.
2. Använd [[De Morgans Lag]] för att bli av med 'or', använd sen a'=1+a
3. Skriv funktionen i [[Disjunktiv Normalform|DNF]], använd sen att 
$m_i V m_j = m_i+m_j+m_i m_j = m_i+m_j$
4. Reed-Muller transform