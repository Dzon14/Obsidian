---
tags: [matstat]
aliases: [betingade väntevärdet]
---
# Betingade [[väntevärden]]

## Definition
**Diskreta fallet:** Det betingade [[väntevärden|väntevärdet]] för $X$ givet $Y = k$ definieras av $$E(X|Y =k) = \sum\limits_{j=0}^{\infty}jp_{X|Y=k}(j)$$**Kontinuerliga fallet:** Givet $Y=y$ definieras av $$E(X|Y=y) = \int\limits_{-\infty}^{\infty} xf_{X|Y=y}(x) \ dx$$Det betingade väntevärdet $E(X|Y =y)$ betecknas ibland $\mu_{X|Y=y}$.

- Om X och Y är oberoende så gäller att $E(X|Y=y)= E(X)$.
#### Exempel
![[Pasted image 20221114160323.png]]

## Sats
Lagen om total förväntan $$E(X) = \begin{cases} \sum\limits_{k=0}^{\infty} E(X|Y=k)p_{Y}(k) \ \ \ \ \ (\text{diskreta fallet} \\ \int\limits_{-\infty}^{\infty} E(X|Y=y)f_{Y}(y) \ dy \ \ \ \ \ (\text{kontinuerliga fallet})\end{cases}$$
#### Exempel
![[Pasted image 20221114160632.png]]