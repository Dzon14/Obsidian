---
aliases: [nyquistkriteriet, nyquistteoremet, nyquist theorem]
---

# Nyquist Criterion
**The Nyquist Criterion** - Assume that the loop transfer function has no poles in the right-half plane, and that possible poles on the imaginary axis are unique (Stable). Given this, the system is asymptotically stable if the point −1 lies to the left of the Nyquist curve as it is traversed from ω = 0 to ω = ∞.

**Svenska:**
Antag att kretsöverföringsfunktionen inte har några poler i högra halvplanet och att eventuella poler på imaginära axeln är unika (Stabilt). Då är slutna systemet asymptotiskt stabilt om punkten −1 ligger till vänster om Nyquistkurvan då denna genomlöps från ω = 0 till ω = ∞.
	
- When lying close to -1, the system will start to oscillate a bit

### Example
$$G_{o}= \frac{K}{s(s+1)(s+2)}$$
Substituting s with iw and then finding $w = w_{0}= \sqrt{2}$ which is when the imaginary part is zero. To determine where the [[Nyquist Curve]] intersects the real axis we investigate $$G_{0}(i \sqrt{2}) = - \frac{3K}{3\cdot 6} = - \frac{K}{6}$$
The curve will lie to the right of the point -1 for $K < 6$. It is stable. 

## [[Stability Margins]]
#regler 