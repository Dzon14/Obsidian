---
tags: [matstat]
---
# Diskret tvådimensionell stokastisk variabel 
Om X och Y båda antar endast ett ändligt eller uppräkneligt oändligt antal olika värden, säges den [[stokastisk variabel|s.v]] (X,Y) vara diskret. 

**Def:** Storheterna  $$p_{X,Y}(j,k) = P(X =j,Y =k), \ \ \ j = 0,1,2,..., \ k =0,1,2,...$$kallas [[sannolikhetsfunktionen]] för den diskreta tvådimensionella [[stokastisk variabel|s.v]].
Även kallad den **simultana** [[sannolikhetsfunktionen]].

En sannolikhet kan beräknas genom $P((X,Y) \in A) = \sum\limits_{(j,k)\in A}^{}p_{X,Y}(j,k)$ 
Summan av sannolikheterna är 1:
$\sum\limits_{j=0}^{\infty}\sum\limits_{k=0}^{\infty}p_{X,Y}(j,k) = 1$

[[fördelningsfunktion]] kan bestämmas ur [[sannolikhetsfunktionen]] genom summering: $$F_{X,Y}(x,y) = \sum\limits_{j \leq x}^{}\sum\limits_{k \leq y}^{}p_{X,Y}(j,k)$$X och Y är båda endimensionella. Deras fördelningar (kallas för **marginalfördelningar**) får man genom genom att hantera den simultana fördelningen för X och Y. 
Se [[marginella sannolikhetsfunktionen]]