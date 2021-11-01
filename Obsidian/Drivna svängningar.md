## Drivna svängningar

Om man tillför mekanisk [[Energi]] till ett system blir det en driven svängning, exempelvis om en motor drar massan på en fjäder upp och ned. Det är ett specialfall då den drivande kraften kan beskrivas som en sinusformad rörelse. Den drivande kraften kan beskrivas med 

$$    F_{driv} = F_0cos\omega t$$

där $\omega$ är den frekvensen på den drivande kraften (alltså inte $\omega_0$ som är resonansvinkelfrekvensen för systemet). 

Ett system måste inte svänga med sin resonansfrekens, beroende på frekvensen fås olika fas och amplitud. Om man tillför [[Energi]] snabbare än den försvinner ökar amplituden, om [[Energi]] tillförs lika snabbt som den försvinner blir amplituden konstant. 

Rörelseekvationen för drivna svängningar:

$$\frac{d^2x}{dt^2} + \frac{b}{m}\frac{dx}{dt} + w_0^2x = \frac{F_0}{m}coswt$$

där $\omega_0^2 = \frac{k}{m}$

lösningen till diff-ekvationen blir

$$x(t) = Acos(\omega t - \delta)$$

där både amplituden A och fasförskjutningen $\delta$ beror på den
drivande frekvensen

$$A = \frac{F_0}{\sqrt{m^2(\omega_0^2 - \omega^2)^2 + b^2\omega^2}}$$

$$\tan\varphi = m\frac{(\omega_0^2 - \omega^2)}{b\omega}$$