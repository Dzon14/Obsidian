---
tags: [fysik]
---
# Harmonisk Svängningsrörelse

I en harmonisk svängningsrörelse är accelerationen, och därmed [[Krafter|nettokraften]], proportionella och riktade mot jämviktsläget. Om man drar en hängande fjäder nedåt kommer fjäderkraften vara riktad uppåt, mot fjäderns jämviktsläge. Om man sen släpper fjädern kommer den dras ihop och botten kommer passera jämviktsläget, varpå [[Fjäderkraft|fjäderkraften]] blir riktad nedåt. På så sätt oscillerar (svänger) fjädern runt sitt jämviktsläge. Fjäderkraften ges av hookes lag $F = -kx$.

Avståndet till jämviktsläget kan beskrivas med en sinusfunktion,

$$    x(t) = Acos(\omega t + \delta)$$

där A är amplituden, dvs största avståndet från jämviktsläget. $\omega$ är vinkelhastigheten (samma sak som vinkelfrekvens!!). $\omega = 2\pi f = \frac{2\pi}{T}$. Hastigheten och accelerationen kan enkelt fås genom att derivera $x(t)$.

$$    v(t) = -\omega Asin(\omega t+ \delta)$$
$$    a(t) = -\omega^2 Acos(\omega t+ \delta)$$
med [[Newtons Lagar|newtons andra lag ]] och ekvationen för [[Fjäderkraft]] fås $a(t) = -\frac{k}{m}x$, vilket leder till
$$    \omega^2 = \frac{k}{m}$$

En harmonisk svängningsrörelse har ingen dämpning. Svängningar kan dock vara dämpade olika mycket, då måste man använda andra modeller. $\omega_0$ är *resonansvinkelfrekvensen*, dvs frekvensen vid vilken systemet befinner sig i resonans.

### [[Energi]] i en harmonisk svängningsrörelse
[[Energi]] i en harmonisk svängningsrörelse är summan av den potentiella och kinetiska [[Energi|energin]]. Den kinetiska [[Energi|energin]] beskrivs av $K = \frac{1}{2}mv^2$, vilket för en harmonisk svängningsrörelse blir

$$K = \frac{1}{2}m\omega^2A^2sin^2(\omega t + \delta)$$

Eftersom $\omega^2 = \frac{k}{m}$ blir då

$$K = \frac{1}{2}kA^2sin^2(\omega t + \delta)$$

Den potentiella [[Energi|energin]] ges av

$$U = \frac{1}{2}kx^2$$

eftersom att x ges av $x(t) = Acos(\omega t + \delta)$ blir [[Energi|energin]]

$$U = \frac{1}{2}kA^2cos^2(\omega t + \delta)$$