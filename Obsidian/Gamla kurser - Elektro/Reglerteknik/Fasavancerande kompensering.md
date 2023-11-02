---
tags: [regler]
aliases: [lead compensation]
---
# Fasavancerande kompensering
Påverkar egenskapen runt skärfrekvensen - påverkar snabbhet och robusthet.
 $$G_{K}= K_{K}N \frac{s+b}{s+bN}=K_{K}\frac{1+ \frac{s}{b}}{1+ \frac{s}{bN}}$$
 $N > 1$.
 ![[Pasted image 20220926183639.png]]
 3 parametrar: $K_{K}$, N och b.

**Egenskaper:**
- Höjer högfrekvensförstärkningen
- Höjer faskurvan

**Användning:**
- Påverka snabbhet ($\omega_c$)
- Påverka robusthet ($\varphi_{m}$)

## Procedur (Parametrar bestäms)
1) Bestäm önskad $\omega_c$ och $\varphi_{m}$
2) Önskad fasökning vid $\omega_c$ ger N. N bestämmer hur stor toppen på kompenseringslänken faskurva är. Den fasökning som behövs vid önskade skärfrekvensen $\omega_c$ är $$\Delta \varphi = \varphi_{m} - (180 \degree + argG_{0}(i \omega_c))$$
3) Se till så att faskurvans topp hamnar vid $\omega_{c} \Rightarrow b \sqrt{N} = \omega_c$
4) Se till så att $\omega_c$ blir skärfrekvens $\Rightarrow \lvert G_{K}(i \omega_{c}) \cdot G_{0}(i \omega_{c) \rvert}= 1$ 
   Där $G_{K}(i \omega_{c)}= K_{K}\sqrt{N}$

## Exempel (elmotor)
$$G_{P}(s) = \frac{100}{s(s+10)}$$
- Gör systemet dubbelt så snabbt (fördubbla $w_{c}$) med bibehållen robusthet ($\varphi_{m}$)
- I **bilden** från [[Fasretarderande kompensering]] ser vi att den ursprungliga skärfrekvensen är 8 och den ursprungliga fasmarginalen $50 \degree$. Vi bestämmer nu parametrarna i den fasavancerande kompenseringslänken enligt de fyra stegen ovan.

1) fördubbla: $\omega_{c}= 2 \cdot 8 = 16$ och $\varphi_{m}= 50 \degree$
2) vid $\omega_{c} = 16$ ser vi i diagrammet att $argG_{0}(i \cdot 16) \approx -150 \degree$. Vi får en fasökning på $\Delta \varphi = \varphi_{m} - (180 \degree- 150 \degree)  = 20 \degree$. I figuren nedan ger detta $N = 2$. 
3) Välja b så fastoppen hamnar vid $\omega_c$ .$b \sqrt{N} = \omega_{c} = 16$ får vi $b = \frac{16}{\sqrt{2}} \approx 11$
4) I bodediagrammet ser vi från $\omega_{c}= 16$ att $\lvert G_{0}(i \omega_c) \rvert \approx 0.35$. Vi får då $K_K \approx2$ eftersom $$\lvert G_{K}(i \omega_{c} \rvert \cdot \lvert G_{0}(i \omega_{c}) \rvert \approx K_{K}\sqrt{N} \cdot 0.35=1$$ ![[Pasted image 20220926190602.png]]

- Vi får då resultatet och den fasavancerade kompenseringslänken till $$G_{K}(s) = K_{K}N \frac{s+b}{s+bN} = 4 \frac{s+11}{s+22}$$