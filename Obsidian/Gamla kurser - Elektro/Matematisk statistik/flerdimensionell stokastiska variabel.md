---
tags: [matstat]
aliases: [stokastisk vektor, flerdimensionella stokastiska variabler]
---
# Flerdimensionell [[stokastisk variabel]]

- [[tvådimensionella stokastiska variabler]]

## Största och minsta värdet
Vi behandlar två [[stokastisk variabel|s.v]]. X och Y; vi antar att de är oberoende.

##### Största värdet av två
Sätt $Z = max(X,Y)$. Vi får $$\begin{align} F_{Z}(z) &= P(Z \leq z) = P(X \leq z) = P(X \leq z \text{ och } Y \leq z) \\ &= P(X \leq z) P(Y \leq z) = F_{X}(z)F_{Y}(z)\end{align}$$
##### Minsta värdet av två
$Z = min(X,Y)$. $$\begin{align} F_{Z}(z)= P(Z \leq z) = ... = 1 - (1-F_{X}(z))(1-F_{Y}(z)) \end{align}$$
##### Största och minsta värdet av fler än två
- Om Z är största värdert blir $F_{Z}(z) = (F(z))^{n}$.
- Om Z är minsta värdet blir $F_{Z}(z) = 1-(1-F(z))^{n}$
