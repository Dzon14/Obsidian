---
tags: [matstat]
aliases: [summan av stokastiska variabler, summa av s.v.]
---
# Summa av stokastiska variabler

## Summa av [[diskreta stokastiska variabler]]
X och Y är diskreta. Vi har [[sannolikhetsfunktionen]] $$p_{Z}(k) = P(Z=k)=P(X+Y=k )$$Händelsen X + Y = k kan inträffa på olika sätt:
- Man kan ha X = 0, Y = k eller X = 1, Y = k-1 osv enda till X=k, Y=0. [[Sannolikhet|sannolikheten]] för händelsen kan uttryckas med 
$$p_{Z}(k) = P(X+Y=k )\sum\limits_{i+j=k}^{}p_{X,Y}(i,j) = \sum\limits_{i= 0 }^{k}p_{X,Y}(i,k-i)$$Analogt blir $$F_{Z}(z) = \sum\limits_{i+j \leq z}^{}p_{X,Y}(i,j)$$
Om X och Y är [[oberoende stokastiska variabler]], vilket är ett vanligt och **viktigt** fall får vi $$p_{Z}(k) = \sum\limits_{i+j}^{}p_{X}(i)p_{Y}(j) = \sum\limits_{i=0}^{k}p_{X}(i)p_{Y}(k-i)$$Vilket kallas [[faltningsformeln]] för oberoende [[diskreta stokastiska variabler]]

## Summa av [[kontinuerliga stokastiska variabler]]
Vi får [[fördelningsfunktion|fördelningsfunktionen]] $$F_{Z}(z) = P(X+Y \leq z )= P((X,Y) \in A_{z}) = \int\limits_{x+y \leq z}^{} \int\limits_{}^{} f_{X,Y}(x,y) \ dx \ dy$$
Om X och Y är **oberoende** och genom derivering med avseende på z får vi följande [[täthetsfunktion]] för Z $$f_{Z}(z) = \int\limits_{-\infty}^{\infty} f_{X}(x)f_{Y}(z-x) \ dx$$och är [[faltningsformeln]] för oberoende [[kontinuerliga stokastiska variabler]]

#### Exempel
![[Pasted image 20221108174145.png]]

## Summa (av [[väntevärden]] osv?)

**Sats:** För alla [[stokastisk variabel|s.v]] X och Y gäller
$$\begin{align} &E(X + Y) = E(X) + E(Y) \\ &V(X + Y) = V(X) + V(Y) + 2C(X,Y) \end{align}$$
**Följdsats:** För [[oberoende stokastiska variabler]] gäller $$\begin{align} &V(X+Y) = V(X) + V(Y) \\ &D(X+Y) = \sqrt{D^{2}(X)+D^{2}(Y)} \end{align}$$