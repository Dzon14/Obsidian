---
tags: [regler]
aliases: [feed forward]
---
# Framkoppling
Till skillnad från [[Feedback|återkoppling]] där en störning måste ha påbörjats för att regulatorn ska reagera på den, så använder framkoppling en teknik där man kompenserar för störningen redan innan reglerfelet sker. T.ex temperatur i bostadshus (med utomhustemp och inomhustemp), eller en bil som åker mot en uppförsbacke.

## Framkoppling av störflöden i tankprocess
![[Pasted image 20221003152707.png|300]]
(FB - feedback)

 **Två fall:**
 1) Störning ($v_{1}$) på övre tanken
 ![[Pasted image 20221003153219.png]]
 (FF - feed forward)
Där styrsignalen ges av $$u = u_{FB}+u_{FF}$$
[[Transfer function|överföringsfunktion]]en ges av $$X = V_{1}+U = V_{1}+U_{FB}+G_{FF} \cdot V_{1}=U_{FB}+(1+G_{FF})$$
Där vi väljer $G_{FF}=-1$, så att störflödet aldrig kommer att ge upphov till någon ändring i nivån y. Framkopplingsdelen av regulatorn ges då av $$U_{FF}= G_{FF}V_{1} = -V_{1}$$

2) Störning ($v_{2}$) på undre tanken
![[Pasted image 20221003153917.png|500]]
Överföringsfunktionen blir 
$$X = V_{2}+G_{P1}(U_{FB}+G_{FF}V_{2})= G_{P1}U_{FB}+(1+G_{P1}G_{FF})V_2$$
där vi sätter $G_{FF}= -\frac{1}{G_{P1}}$.
Vi får framkopplingen $$U_{FF}= G_{FF}V_{2}=-\frac{1}{G_{P1}}V_{2}$$

De flesta processer är av lågpasskaraktär. 
Antaget $$\begin{flalign} &G_{P1}(s) = \frac{1}{s+a} \\ &G_{FF}= - \frac{1}{G_{P1}}=-(s+a) \\ &U_{FF}= -(s+a)V_{2} \Rightarrow \text{ deriverar }v_{2}\end{flalign}$$
Att derivera kan dock ge upphov till störningskänslighet och bör undvikas.
Istället kan man:  1. Lågpassfiltrera $V_{2}$ eller stryka de deriverande termerna vilket ger $$u_{FF}= -av_{2}$$
