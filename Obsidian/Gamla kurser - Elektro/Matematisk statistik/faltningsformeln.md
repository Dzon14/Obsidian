---
tags: [matstat]
aliases: [faltningsformel]
---
# Faltningsformeln

## Diskreta fallet
Om X och Y är [[oberoende stokastiska variabler]], vilket är ett vanligt och **viktigt** fall får vi $$p_{Z}(k) = \sum\limits_{i+j}^{}p_{X}(i)p_{Y}(j) = \sum\limits_{i=0}^{k}p_{X}(i)p_{Y}(k-i)$$
Härleds utifrån [[summa av stokastiska variabler|summa av s.v.]] 

## Kontinuerliga fallet
Om X och Y är **oberoende** och genom derivering med avseende på z får vi följande [[täthetsfunktion]] för Z $$f_{Z}(z) = \int\limits_{-\infty}^{\infty} f_{X}(x)f_{Y}(z-x) \ dx$$