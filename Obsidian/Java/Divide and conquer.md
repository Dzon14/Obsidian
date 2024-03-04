---
aliases: [Söndra och härska]
tags: [prog]
---
# Divide and conquer
- Mergesort och Quicksort
- Teknik för att konstruera rekursiva algoritmer
- Avser rekursiva algoritmer som minst två rekursiva anrop i varje upplaga.
		- Problemet delas upp i två eller flera mindre som löses [[Rekursion|rekursivt]] (söndra)
		- Lösningarna kombineras till en lösning till det ursprungliga problemet (härska)
		![[Pasted image 20211104120333.png|100]]
### [[Sortering]] av element i en vektor:
- Dela vektorn i två lika stora halvor
- Sortera [[Rekursion|rekursivt]] första halvan $a[0... n/2]$
- Sortera rekursivt andra halvan $a[n/2 +1 ... n-1]$
- Slå samman de båda sorterade delvektorerna -> $a[0 ... n-1]$
Härska-steget är algoritmkonstruktionen och Söndra-steget är rekursiva anrop.
Finns en metod som kallas för [[Mergesort]]

