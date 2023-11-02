---
tags: [komsys]
---
# Bellman-Ford
- Itererar fram den lägsta kostnaden från en nod till andra noder i grafen genom att upprepat räkna ut kostnaden för att ta sig från en nod via en båge till nästa nod.
	  - Skapa lista över alla bågar, sedan sätta kostnade för utgångsnoden (roten) till 0 och kostnaden för alla andra noder i grafen oändligheten. 
	  - gör sedan n st iterationer (n = antal noder - 1)
	  - Den längsta vägen i ett träd får vi om alla noder ligger efter varandra.
	  - I varje iteration och för varje båge (u,v) mellan nod u och nod v adderas kostnaden för nod u, d(u) med kostnaden för bågen mellan nod u och nod v $c(u, v)^{2}$.
	  - När alla iterationer genomförts har man lägsta kostnad från roten till alla andra noder i grafen. 

s.167-168