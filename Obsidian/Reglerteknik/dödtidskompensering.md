---
tags: [regler]
aliases: [dödtid, delay compensation]
---
# Dödtidskompensering
[[Derivative control strategy|D-delen]] i en [[PID-controller|PID-regulator]] predikterar framtida värden genom att studera derivata. Denna metod fungerar dock dåligt när processen har en lång dödtid.
Dödtidsregulatorer studerar styrsignalen (istället för att studera mätsignalen vid prediktionen).

Processen $$\frac{1}{1+5s}e^{-10s}$$ har en dödtid på 10 sekunder.

## Otto-Smith-regulatorn
![[Pasted image 20221003161131.png|450]]
Signalen vi hade fått om vi ej har en dödtid i processen. En identisk process bortsett från att dödtiden är borttagen. 

