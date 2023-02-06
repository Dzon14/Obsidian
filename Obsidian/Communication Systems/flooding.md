---
tags: [komsys]
aliases: [översvämning]
---
# Flooding
Används i vissa specialfall. T.ex då noder inte vet var destinationsnoden finns. 
Här görs inget egentligt vägval utan ett paket som kommer till en nod skickas ut på nodens samtliga länkar utom den som paketet kom in till noden på.

hop count är en övre gräns för hur många gånger paketet kan kopieras och s kickas vidare. 

- Kan ses som ett enkelt [[routingprotokoll]], där noderna inte behöver kommunicera information om nätets struktur med varandra