---
tags: [komsys]
---
# Dikjstras algoritm
Här utgår man från noderna istället för bågarna ([[Bellman-Ford]]).
Noderna besöks i ordning efter minsta kostnad från roten räknat - *Shortest Path First (SPF)*.

1. Identify the root (the node itself)
2. Attach all neighbor nodes temporarily
3. Make link and node with least cumulative cost permanent
4. Choose this node
5. Repeat 2 and 3 until all nodes are permanent. 

s.169 - 170