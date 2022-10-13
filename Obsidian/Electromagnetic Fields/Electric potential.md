---
tags: [el]
aliases: [electric potential]
---
# Electric potential
A measure that is related to the among of work to move a test charge $q_0$ in the E field due to another charge $q_{1}$ (or a system of multiple charges).

$$\vec{E} = - \nabla V$$

![[Pasted image 20220919115112.png]]

The work against the [[Electric field|field]] is: $$W = - \int_{p_{i}}^{p_{f}} \vec{F} \cdot \ d \vec{l} = -q_{0} \int_{p_{i}}^{p_{f}} \vec{E} \cdot \ d \vec{l}$$ (since $\vec{F} = q_{0} \vec{E}$)

We define change of electrical potential $\Delta V = V_{1}- V_{0}$ as $$V_{1}-V_{0}= \frac{W}{q_{0}}= \frac{q_1}{4 \pi \varepsilon_{0}}\left( \frac{1}{R_{p_f}}  -\frac{1}{R_{p_f}}\right) = - \int\limits_{p_{i}}^{p_{f}} \vec{E} \cdot \ d \vec{l}$$

where $R_{p_{i}} and R_{p_{i}}$ are the distance between point charge $q_{1}$ and points $p_{i}$ and $p_{f}$ respectively.
If $p_{i}$ goes towards infinity (test charge moved form infinitely far away, with a reference electric potential of $0V$) we can definite electric potential as $$V_{1}= \frac{q_{1}}{4 \pi \varepsilon_{0}R_{p_{f}}}$$
Electric potential is scalar, thus
$$V = \frac{1}{4 \pi \varepsilon_0}\sum_{k=1}^{n}\frac{q_{k}}{\lvert \vec{R}-\vec{R'_{k} \rvert}}= V_{1}+..+V_{n}$$

## Example
- Find $\vec{E}$ for an [[electric dipole]] (i.e., two charges $+q$ and $-q$ separated by distance $d$).
![[Pasted image 20221005115418.png]]




