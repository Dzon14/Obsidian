---
tags: [matstat]
aliases: [binomialfördelningen]
---
# Binomialfördelningen

# Ekonomi
![[Pasted image 20231009112926.png]]
- För binomialfördelning kan det ofta passa med [[Kombinatorik]]

Formel är (se nedan i matstat)

## Exempel
![[Pasted image 20231009114123.png|550]]
![[Pasted image 20231009114512.png|550]]



# Matstat

$$p_{X}(k) = \begin{pmatrix} n \\ k \end{pmatrix}p^{k}(1-p)^{n-k}, \ \ \ k = 1,2,...,n,$$där $0 \leq p \leq 1$. Vi erinrar även om kodbeteckningen $X \in Bin(n,p)$.

## Förekomst
Binomialfördelningen uppträder vid vissa typer av slumpmässiga försök. 

**Sats 7.1:** Antag att sannolikheten är p att en händelse A inträffar i ett enskilt försök. Om $n$ oberoende försök utförs och X är antalet gånger som A inträffar, gäller att $X \in Bin(n,p)$.

Binomialfördelningen uppträder också som fördelningen för summan av oberoende likafördelade tvåpunktsvariabler. 

Summan av indikatorvariabler har samma fördelning som X (binomialfördelning), alltså: $X = I_{1}+I_{2}+...+I_{n}$.

## Exakta egenskaper
[[sannolikhetsfunktionen|sannolikhetsfunktion]]: $$p_{X}(k)= \begin{pmatrix} n \\ k \end{pmatrix}p^{k}(1-p)^{n-k}$$
[[fördelningsfunktion]]: $$F_{X}(k) = \sum\limits_{j=0}^{k}\begin{pmatrix} n \\ j \end{pmatrix}p^{j}(1-p)^{n-j}$$
**Sats 7.2:** Om $X$ är $Bin(n,p)$ gäller att $$E(X) = np, \ \ V(X) = np(1-p), \ \ D(X) = \sqrt{np(1-p)}$$
**Sats 7.3:** Om $X \in Bin(n_{1},p)$ och $Y \in Bin(n_{2},p)$, där $X$ och $Y$ är oberoende, gäller att $X+Y \in Bin(n_{1}+n_{2},p)$

##### Exempel
![[Pasted image 20221121174648.png]]

## Approximativa egenskaper
Approximationer för när de exakta uttrycken för sannolikhets-/fördelningsfunktionerna är för besvärliga.

1. **Normalapproximation**
   För stora n kan binomialfördelningen approximeras med en [[normalfördelning]]. Då är nämligen X ungefär normalfördelad med det [[väntevärden|väntevärde]] och den [[standardavvikelse]] som anges i Sats 7.2, dvs approximativt gäller att $X \in N(np, \sqrt{np(1-p)})$. Av formel (6.4) på sidan 144 följer då att man har $$P(a < X \leq b) \approx \Phi \left( \frac{b-np}{\sqrt{np(1-p)}} \right) - \Phi \left( \frac{a - np}{\sqrt{np(1-p)}} \right)$$Nogrannheten kan förbättras om man lägger till + 1/2 efter a och b enligt $$P(a < X \leq b) \approx \Phi \left( \frac{b+ \frac{1}{2}-np}{\sqrt{np(1-p)}} \right) - \Phi \left( \frac{a + \frac{1}{2} - np}{\sqrt{np(1-p)}} \right)$$
   Vi har nu infört **halv- eller kontinuitetskorrektion**.

##### Exempel
![[Pasted image 20221121180122.png]]

2. **Poisson-approximation**
Om p är litet kan man approximera binomialfördelningen med [[Poission Stokastisk Variabel]]-fördelningen. Fördelad med parametern $\mu=np$ och vi får $$p_{X}(k) \approx \frac{(np)^{k}}{k!}e^{-np}, \ \ \ k=0,1,...$$Approximationen är vanligen tillräckligt noggrann om $p$ är högst lika med 0.1.
![[Pasted image 20221121181400.png]]

## Om relativa frekvenser
Kvoten mellan absoluta frekvensen och hela antalet försök ($Y=\frac{X}{n}$).
Vi har räknereglerna $$\begin{align} &E(Y) = p, \\ &V(Y) = \frac{p(1-p)}{n}, \\ &D(Y) = \sqrt{\frac{p(1-p)}{n}} \end{align}$$
Följande sats gäller:
- [[Bernoullis sats]]

För stora n har man approximativt $Y \in N(p,\sqrt{p(1-p)/n})$. 
Om man har två oberoende frekvenser $Y_{1}= \frac{X_{1}}{n_{1}}$ och $Y_{2}=\frac{X_{2}}{n_{2}}$ då gäller approximativt att $$Y_{1}- Y_{2} \in N \left( p_{1}- P_{2}, \sqrt{\frac{p_{1}(1-p_{1})}{n_{1}}+\frac{p_{2}(1-p_{2})}{n_{2}}} \right)$$

