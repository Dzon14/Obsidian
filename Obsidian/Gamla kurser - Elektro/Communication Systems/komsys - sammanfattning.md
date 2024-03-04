---
tags: [komsys]
---
# KomSys Sammanfattning
### Internet Protocol Suite = TCP/IP model
![[Pasted image 20230116104300.png|600]]
- Connection oriented, error control, retransmission, flow control, congestion detection, sends ACK
- Fördelar: Allt som fungerar med IP fungerar med nätet. Övre lager behöver inte veta vad de andra lagrena gör.
- Nackdelar: Under fragmentering behöver alla fragment varsin header vilket är ineffektivt jämfört med cross-layer. 
### OSI-modell
![[Pasted image 20230316101753.png|500]]
- För OSI behövs också en header för alla lager, då dessa jobbar individuellt. Behövs ej för cross-layer.

## Physical Layer (F2) - 2.1-3, 3.1-5
- Lägsta nivån och ansvarar för överföring av bitar. Överförs genom fysiskt medium (tvinnad parkabel, koaxial, fiber eller trådlöst)
- Tvinnad: Kopparledare tvinnade. Överföring via elektromagnetiska vågor. Koppar låg resistans $\Rightarrow$ dämpning lägre.
- Koaxial: enkel kopparledare med metallhölje och isolerande material. MIndre störningskänsligt $\Rightarrow$ maximal bandbredd längre. 

#### Sampling, kvantisering och kodning
Allmänt om Sampling, quantization och kodning:
En kontinuerlig signal samplas (analogt till diskret med avseende på tid) (dubbla högsta frekvensen - Nyquist Criterion|nyquistteoremet). Sample rate är hur många samples per sekund (t.ex 1 per sek är 1 Hz). Kvantisering (analogt till diskret med avseende på amplitud) används för att ge varje mätvärde en specifik amplitudnivå (avrundat), så man kan representera signalen med ett begränsat antal bitar. Vid kvantisering uppstår alltid ett kvantiseringsfel (avrundningsfel) som berpr på storleken av kvantiseringssteget (längd mellan amplitudnivåer). För att kunna lagra dessa i binär form så kodas den med antal bitar. $2^{k}$ där k är bitarna som behövs för koda samplen till binära tal. Kodning: Gör om diskreta signaler till digitala bia en binär representation
- Människohörsel: 20kHz, allt över filtreras ut.
- Stadsmiljö: 4kHz
- Mänskligt tal: 300Hz - 3400Hz
- Kvantisering med 8 bitar - telefoni
- Kvantisering med 16 bitar - CD
- **Brus:**
SNR - signal to noise ratio: $$SNR = 10 \cdot log \frac{P_{s}}{P_{n}}$$
där $P_{s}$ är signalens medeleffekt och $P_{n}$ brusets medeleffekt.
Kvantiseringsfel blir tillräckligt litet om försumbart med annat brus (se uppgift 1). Alltså $$SQNR < SNR$$**Filter**: Innan man samplar behöver man filtrera signalen. Detta görs enligt samplingsteoremet, och genom användning av ett LP-filter med en brytfrekvens på kan man filtrera ut brus. T.ex filtrera ut människohörsel.

#### Dital transmission - olika metoder
- **On-off keying (OOK)**: låg vid 0a och hög vid 1a.
- **Non-return-to-zero keying (NRZ)**: Hoppar mellan högt o lågt då den ej går i viloläge. Här är det tvärtom där 1 ger lågt och 0 ger högt (?).
- **Return to zero keying (RZ)**: Som NRZ men mellan olika värden går signalen till noll.
- **Manchesterkodning**: Kombinerar NRZ med klockpuls, vilket ger inga synkproblem och dubbel signalfrekens (jmfrt med NRZ). (se exempel)
- **Differentiell Manchesterkodning**: Signalen beror på föregående. Om 0 kommer pulsen vara samma som föregående, annars skiftar. 
 ![[Pasted image 20230316120001.png|200]]



#### Exempeluppgifter på det fysiska lagret
**1 - Beräkning på sannolikhet för paket**
Vid analog-digital omvandling uppkommer kvantiseringsdistortion eftersom en samplad signal endast kan representeras av ett begränsat antal värden (binära tal). Då blir det en designfråga att använda ett rimligt antal bitar per samplad signal i en A/D-omvandlare (ADC) för att kunna uppnå tillräckligt små kvantiseringsfel. Förklara hur vi kan bestämma detta i ett kommunikationssystem.
	Svar: kvantiseringsfelet blir tillräckligt litet om det är försumbart jämfört med annat brus i kommunikationen. För att se detta måste man jämföra SNR (signal-to-noise ratio) och SQNR (signal-to-quantisation-noise ratio). SNR är definierat som signalens medeleffekt dividerat med brusets medeleffekt och anges i decibel. $\text{SNR} = 10 \cdot log (\frac{P_{s}}{P_{n}})$. Genom att välja rätt bitar för kvantisering kan vi få SQNR < SNR. 

**2 - AD-omvandling**
En analog ljudinspelning av olika ljudeffekter från stadsmiljö ska skickas över ett digitalt kommunikationssystem (typ Internet). Innan de skickas måste ljudfilerna AD-omvandlas, och vid mottagaren måste de DA-omvandlas. Hur skulle du dimensionera AD-omvandlaren, och vad innebär det för överföringshastigheten?
	Svar: Det beror på frekvenser i den analoga signalen. Ska vara dubbla av maximala frekvensen enligt Nyquist. Exempelvis om signalen är 20kHz (ljudeffekter från staden) så blir samplingsfrekvensen minst 40Khz. Kvantisera sedan med 8 eller 16 (optimalt). Viktigt att ha 2 kanaler (stereo) för att kunna återge en bra representation av stadsmiljön. 
	Överföringshastighet: $40k \text{ samples/s } 16 \text{ bits/sample } \cdot 2 \text{ channels }= 1.28 \ Mbps$

**3 - Kompressionsgrad**
Videoformatet 4K UHD betyder att bilden har 3840 $\cdot$ 2160 pixlar, där färgen för varje pixel specificeras med 4 bytes. Den vanligaste bildhastigheten är idag 24 fps (frames per second = bilder per sekund). För att kunna överföra den typen av video över Internet måste den komprimeras. Normalt ligger den resulterande hastigheten för 4K UHD efter komprimering på ungefär 25  Mbps. Hur mycket det är komprimerat beskrivs ofta av kompressionsgraden, som okomprimerad hastighet delat med komprimerad hastighet. Vad blir kompressionsgraden för 4K UHD i detta exempel?
	Svar: Originalvideo: $3840 \cdot 2160 \cdot (4 \cdot 8) \cdot 24 \text{ bits/s } = 6370099200 \text{ bits/s } =  6370 \ Mbps$. $$\text{KG} = \frac{6370}{25} = 254.8$$
###### Uppgifter på Digital transmission

**4 - Manchesterkodning och blockdiagram**
a) En Manchester-kodad signal består egentligen av två sammanslagna signaler. Vilka? Vilken bitsekvens motsvarar den? Konvertera bitsekven- sen till Differential Manchester.
![[Pasted image 20230310102439.png|500]]
Svar: Data + clock pulse: 101101001101100101
Differential: 
b) I bild 2 visas ett blockdiagram som representerar ett enkelt kommunikationssystem som håller på med att skicka ut en signal x(t). Beskriv konceptet ERROR inom datakommunikation med hjälp av blockdiagrammet. Identifiera komponenterna x(t), h(t), n(t), y(t) i samband med din beskrivning. Ange även vilka sorter av error som kan finnas i ett kommunikationssystem.
![[Pasted image 20230310104254.png|300]]
Svar: Error sker när bitarna blir korrupta. h(t) är vart bitarna förbereds och sedan skickas av kommunikationssystemet (kan även uppstå errors här). n(t) är brus som läggs till i signalen. y(t) = x(t) + n(t). Dessa brus kan skapa errors. Finns två errors: Bit errors och Burst errors. 

**Extra - Olika transmissionsmetoder**
Den binära sekvensen x = 10010010 . . . skall skickas över en optisk fiber. Skissa signalen som skickas om modulationen som används är: 
*Eftersom det är optisk fiber kan inte negativa pulser användas*
a) Non-return to zero (NRZ). Ange en fördel och en nackdel med tekniken. 
Svar: 
![[Pasted image 20230316173654.png|300]]
b) Return to zero (RZ). 
Svar:
![[Pasted image 20230316173716.png|300]]
c) Differentiell RZ. (Fungerar enligt samma princip som differentiell Manchester-kodning men med pulsformen för RZ).
Svar:
![[Pasted image 20230316173817.png|350]]

**5 - Anslutning, round-trip time osv**
Antag att en spelare har sin dator ansluten via en ADSL-länk på 2 km till en router i access-nätet. Spelservern som hen spelar mot ligger i Washington, och denna nås via en fiberlänk på 6550 km, via en router och ytterligare 10 km fiber. I bild 4 visas en skiss över förbindelsen. Utbredningshastigheten i både kopparkabel och fiber är ungefär 2/3 av ljushastigheten i vakuum, dvs ungefär v = 2 ∗108 m/s. Den inbyggda tidsfördröjningen i de två routrarna är Tr = 1 ms medan det i residential gateway (RGW) för ADSL är ungefär Tg = 20 ms.
![[Pasted image 20230310104922.png|450]]
a) Kommer förbindelsens round-trip time (RTT), dvs tiden fram och tillbaka mellan spelaren och servern, att hålla sig under 85 ms, den högsta ping-tiden som tillåter att alla typer av spel kan fungera utan nätverksproblem?
Svar: Utbredningstid: $T_{p} = \frac{6562 \cdot10^{3}}{2 \cdot 10^{8}}  =33 \ ms$
Totala tiden blir alltså 110 ms (fram o tillbaka), dvs över 85 ms. .
b) Om spelaren uppgraderar till en fiberansluting istället för ADSL, kommer den inbyggda fördröjningen i RGW att minskas till ungefär Tg = 2 ms. Hur kommer det att påverka spelupplevelsen för det här fallet?
Svar: Blir 74 ms, förbättrar

**6 - Sampling**
Ljudspåren till en blockbuster skall spelas in i DVD-Audio format med full surround sound, dvs med 5 kanaler. För att konvertera ljudet från analog till digital form inför inspelning får man välja, i enlighet med DVD-Audios specifikationer, en av de fördefinierade samplingsfrekvenserna (44.1 kHz, 48 kHz, 88.2 kHz, 96 kHz, 176.4 kHz, eller 192 kHz) samt kodningsalternativen (16 bitar, 20 bitar, eller 24 bitar per sample). Ljudet sparas sedan på DVD med hjälp av linjärt PCM, antingen okomprimerat eller med icke-förstörande datakomprimering. DVD-Audio specifikationen begränsar den maximala bithastigheten till 9,6 Mbps. Samplingsfrekvens/kodningsalternativ kombinationer som gör att denna gräns överstigs måste genomgå datakomprimering.

a) Givet samplingsfrekvensen (96 kHz) skall användas, vilket kodningsalternativ borde tillämpas för att nå minimalt kvantiseringsfel utan datakomprimering?
	Svar: Totalt 9600000 bps, vilket blir $\frac{9600000}{5 \ kanaler}=$ 1920000 bps per kanal. Det är maximala gränsen. Dela det på 96 kHz vilket ger 20 bits.

b) Givet kodningsalternativet (24 bitar per sample) skall tillämpas, vad är den högsta samplingsfrekvensen som kan väljas utan att behöva datakomprimering?
	Svar: $\frac{1920000}{24}=80kHz$, finns ej bland alternativ så vi väljer 48 kHz.

c) För bättre ljudkvalitet, vi väljer kombinationen (96 kHz / 24 bitar per sample). Vad är den minsta effektiviteten datakomprimeringen måste nå för att kunna hålla bithastigheten inom tillåtna gränser.
	Svar: $96000 \cdot 24 = 230400$ bps. Det är över gränsen. $\frac{2304000}{1920000}= 1,2$ eller högre.

**Extra**
a) Beskriv kortfattat de tre olika steg som ingår i analog till digital-omvandling. 
Svar: Sampling, kvantisering och kodning
b) Före analog till digital-omvandling bör den analoga signalen filtreras. Ange kortfattat varför och ange specifikationer för filtret (LP/HP/BP samt relaterade brytfrekvenser).
Svar: Sampling sker med dubbla frekvensen (samplingsteorem) $F_{s} = 2 f_{max}$. Alla bidrag för maxfrekvensen kommer vikas under rekonstruktion. Kan förekomma frekvenser man ej vill ha (brus). Därför används lågpassfilter (LP) med brytfrekvens $\frac{F_{s}}{2}$.

## Data Link Layer (L3-L4)
- 4.1-5 och 5.1-6
- Dataöverföring och access till nätet
- **Frames** are used as 
		  - Synchronization points (Preamble, SFD)
		  - To switch between users (Adressing)
		  - Error handling (CRC)

### Dataöverföring (L3)
- Protokoll - krävs för kommunikation, regler för vad som ska gällas i dataöverföringen.
-  **Ramstruktur:** Flagga - Kontroll - Data - Kontroll - Flagga
- **Applikationsprotokoll**: Kommunikation mellan två användarapplikationer.
- **Länkprotokoll:** Tar emot data från applikationen och ser till att denna kommer korrekt till mottagaren. 
- **Overhead:** onödig data (överflödigt). Varje skikt (layer) bidrar med en egen header som drar ner effektiviteten. 
- **Payload:** Nyttig data
- Man kan se allting som i lager, dvs ethernet (som är längst ned, dvs fysiska lagret) har en header o data osv, som sedan skickas till nästa lager (IP) som också har en header och data osv, sedan Transport. Detta packas sedan upp lager för lager. 
		- T.ex I ethernet header så kan det i datan finnas IPv4 med header o data o i den datan finns det annat osvosv. Viktigt att tänka på detta sätt vid uppgifter där man ska räkna bytes. 
		- Exempelvis: Ethernet/MAC -> IP -> UDP
- **Throughput**: måttenhet för hur mycket data som kan överföras mellan två punkter i ett kommunikationssystem under en viss tidsperiod. (bps)

##### ARQ:
**stop-and-wait**: Måste få bekräftat för varje paket som skickas. Långsamt eftersom endast ett paket kan skickas i taget. Det innebär att om man ska skicka datagram nummer 17, och ACK för datagram 12 kommer, så kastar man det, då man redan har fått ACK för nummer 12. Annars hade man aldrig skickat paket 13.
**Go-back-N**: Kan skicka flera åt gången mha ett sändfönster. Fönstret flyttas fram när ramen längst till vänster blivit bekräftat. Om fel uppstår för en ram så sparas de andra ramarna i fönstret i ACK, medan sändaren skickar om alla. Den som kommit bort får nu en ACK och de som det inte var något fel på kastas bort av mottagaren. 
**selective repeat**: En variant av go-back-n där mottagaren kan skicka en NAK vid fel så sändaren direkt kan skicka endast det paketet som är fel. Detta leder till att man enbart kan skicka det förlorade paket i sliding window, istället för alla paket. För att detta ska fungera behöver sliding window storleken vara maximalt hälften så stort som det största sekvensnummret.

#### ALOHA
**Pura ALOHA**:
- Skickar en frame så fort den har något att skicka.
- Kollisioner kan ske iom ingen kontroll sker innan de skickar data. En terminal vet att det har blivit kollision om den ej får en ACK inom en viss tid $\Rightarrow$ den skickar datan igen. Att det lätt blir kollisioner är dock en brist med ALOHA då utnyttjandet av länken blir låg.
![[Pasted image 20230316125442.png|300]]
**Slotted ALOHA**:
En ny version (1975) av ALOHA för att förbättra prestandan.
Tiden delas in i intervaller som motsvarar transmissionstiden för ett [[datapaket]]. En central klocka används sedan för att synkronisera alla terminaler. Terminalen får endast skicka ett paket i början av varje tidsintervall. 
$\Rightarrow$ I varje tidsinterball är det antingen tyst, skickas paket eller kollision. Detta ökar det maximala uttnytjandet av länken med en fördubbling.
- Halverar tiden när ingen annan kan skicka, och maximal throughput blir 36% av länkkapaciteten.

#### Felhantering
 - Forward Error Correction (FEC) - mottagaren korrigerar bitfel själv. Bygger på samma princip som feldetektering, sändaren lägger till bitar,
- Retransmission - sänder om hela [[datapaket|datapaketet]](ramen)
- Använda ACK.

#### Feldetektering
**Paritetsbit**: Enklaste metoden där sändaren lägger till en bit och mottagaren jämför den med tillhörande data. Jämn paritet - lägger till en etta (vid ojämnt antal ettor) annars en nolla. Udda paritet tvärtom. Ett problem med detta är att endast ett ojämnt antal bitfel i ett [[datapaket|paket]] kan upptäckas, inte jämnt antal bitfel. 
**CRC**: Jobbar med flera paritetsbitar. Given bitsekvens kan göras om till ett polynom d(x) - dataordet. Vi har även ett kodord c(x) följt av paritetsbitar r(x). $c(x) = d(x) \cdot x^{k} + r(x)$. Vi har även ett generatorpolynom g(x). Sedan divideras $d(x)\cdot x^{k}$ med g(x) då detta ger paritetsbitar r(x). Addera sedan r(x) till c(x) och det blir jämnt delbart med g(x). Om *bitfel* som kan representeras med e(x), vi får då kodordet $y(x) = c(x) + e(x)$. Vid dividering av g(x) fås resten s(x). Om s(x) = 0 är det korrekt annars är det någon error. Tänk på att det är **XOR** vid divisionen.
- Kan göra binärt eller polynomialt.
**Kontrollsumma/Checksum**: 
Sändaren delar upp datan i segment av ett visst antal bitar. Sedan adderas segmenten till varandra och resultatet blir en delsumma. Eventuela carry bits adderas till delsumman och vi får en slutsumma. Slutsumman har nu lika många bitar som varje segment. Komplettera slutsumman och skicka med paketet (sändaren). Mottagaren delar sedan upp i segment och adderar. Dvs kontrollsumman adderas som ett av de andra segmenten och carry bits adderas efteråt. Sedan tas komplementet av summan, om det är noll har paketet tagits emot korrekt. 
![[Pasted image 20230316151122.png]]

#### Exempeluppgifter
**7 - ARQ**
En sändare har sänt alla ramar till och med sekvensnummer 17. Hur kommer sändaren att agera på ett mottaget ACK, och i förekommande fall, NAK, om ARQ-metoden är:
	a) stop-and-wait ARQ och sändaren tar emot ACK(13)?
	Svar: Kastar ACK(13) och alla ramar fram till ram 16 blir kvitterade.
	b) go-back-n ARQ och sändaren tar emot ACK(13)? Sändfönstret slutar vid sekvensnummer 20.
	Svar: Sänder om ramar 13-17 och fortsätter sända 18-20.
	c) selective repeat ARQ och sändaren tar emot ett ACK(13) och även ett NAK(13)? Sändfönstret slutar vid sekvensnummer 20.
	Svar: Sänder om ram 13 och fortsätter sända 18-20.

**8 - Feldetektering**
Antag att bitsekvensen (dataord) 010111 ska skickas över en länk. CRC används för feldetektering med generatorpolynomet g(x) = $x^{4}+x^{3}+x^{2}+1$. Se till att du använder binärdivision i den ena deluppgiften och polynomdivision i den andra. (vilken som vilken)
a) Ange bitsekvensen (kodord, dvs data och CRC-bitar) som skickas iväg.
	*Svar*: Polynomdivision! resten blir $x^{2}+x$ alltså r = 0110, alltså det som skickas iväg är 0101110110
	![[Pasted image 20230316180523.png|450]]

b) Introducera ett 2-bitars fel i det kodord som tags emot och visa hur det kan upptäckas av mottagaren.
	*Svar*: Binärdivision! Resten blir ej noll $\rightarrow$ fel
	![[Pasted image 20230316175627.png|300]]

**Extra - feldetektering**
Sekvensen x = 11000110100101000011 skall skyddas med en feldetekterande kod som adderar fyra bitar innan den skickas över en kanal. Vilka fyra bitar skall läggas till om koden är: 
a) Fyra bitars checksum. 
Svar:
![[Pasted image 20230316175338.png|250]]
b) Fyra bitars CRC beräknat med g(x) = $x^{4}+x+1$
Svar: 
![[Pasted image 20230316180641.png|250]]

**9 - Sannolikhet**
För att skicka data från nod A till nod B används Stop-and-wait ARQ flödeskontroll. Själva transmissionstiden i nod A och nod B är $T_{t}$, medan propageringstiden är $T_{p}$ i båda riktningarna. När allt fungerar som det ska skickar nod A en ram och väntar på ett korrekt mottaget ACK från B innan den skickar nästa. Om något går fel och A inte får ett ACK väntar den time out-tiden $T_{to}$ innan den skickar om ramen. Sannolikheten att det uppstår ett fel i transmissionen från A till B är $P_{a}$ medan sannolikheten att det uppstår ett fel i transmissionen från B till A är $P_{b}$.
Ledning: Följande två standardsummor för |x| < 1 kan vara bra att ha
$$\sum\limits_{i=0}^{\infty}x^{i}=\frac{1}{1-x}, \ \ \ \ \ \ \ \ \ \ \ \ \sum\limits_{i=0}^{\infty}ix^{i}=\frac{x}{(1-x)^{2}}$$
a) Vad är det förväntade antalet omsändningar $E[K]$ som behövs när A skickar en ram till B och får ett korrekt ACK tillbaka?
	*Svar*: Antag att ett paket kastas om mottagaren detekterar fel i det, vilket innebär att om det blir fel på endera länken kommer A inte att få ett korrekt ACK från B. Ett korrekt ACK kan bli mottaget i A om båda överföringarna är felfria, alltså $P_{rätt}= (1-P_{a})(1-P_{b})$. Sannolikheten för att det blir fel blir då $P_{fel}=1-P_{rätt}=P_{a}+P_{b}+P_{a}P_{b}$. Det förväntade antalet omsändningar är antalet omsändningar som behövs tills A får ett korrekt ACK. $$E[K]= \sum\limits_{k=0}^{\infty}kP_{fel}^{k}P_{ratt} = P_{ratt}\frac{P_{fel}}{(1-P_{fel})^{2}}=\frac{P_{fel}}{1-P_{fel}}$$

b) Vad är den förväntade tiden $E[T]$ för att skicka en ram från A till B och få ett korrekt ACK tillbaka?
	*Svar*: Det kommer ta time-out tiden $T_{to}$ innan A skickar om. $E[T_{oms}] = E[T_{to}K] = T_{to}E[K]$
	Tiden fär ett korrekt skickat paket är $T_{rätt}= 2T_{t}+2T_{p}$ och vi får $$E[T] = T_{rätt}+E[T_{oms}] = 2T_{t}+2T_{p}+T_{to}\frac{P_{fel}}{1-P_{fel}}$$

c) Evaluera $E[K]$ och $E[T]$ för värdena $T_{t}$ = 1; $T_{p}$ = 0,1; $T_{to}$ = 5; $P_{a}$ = $P_{b}$ = 0,05.
	*Svar*: Sätt in värden 

**10 - ram och ARQ**
(a) Ange tre grunder varför ramar används på datalänkskiktet i stället för att skicka en bitström kontinuerligt ut. Förklara även varför flaggor används. 
	*Svar*: Header/preamble är flagga. EJ samma sak som SFD, utan SFD är en del av ethernet-flaggan. 
	 i) För att kunna synkronisera. ii) switch between users. iii) felhantering. Flaggor används för att visa vart ramen börjar och slutar vilket hjälper mottagaren.

(b) En dator försöker skicka 5 datapaket (nummer 1-5) till en annan dator. Paket nummer 2 kommer inte fram rätt, det vill säga det kan antas vara förlorat. Alla andra paket kommer fram korrekt. Anta Go-back-N med ett sändfönster med storlek 3. Beskriv vad som skickas mellan sändare och mottagare (gärna med ett flödesdiagram) fram till och med det att sändaren får ACK på det sista datapaketet.
	*Svar*:
	![[Pasted image 20230314110153.png|350]]

**Extra**
Besvara följande frågor. 
a) Beskriv kortfattat hur Go-Back-N ARQ fungerar. Förklara även ’sliding window’ konceptet. Vad händer om man väljer fel fönsterstorlek? 
Svar: Kan skicka flera åt gången där det använder ett slidint window av viss storlek. Vid ACK så flyttas fönstret fram ett steg. Om inget ACK så kommer alla ej ACKade frames skickas om. Om man väljer fel window size kan duplicates råka sändas. 
b) Vad är skillnaden mellan ALOHA och Slotted ALOHA? Vad har det för påverkan på deras genomströmning (throughput)?
Svar: I (pure) ALOHA skickas en frame när det finns att skicka. 18% Kapacitet. I Slotted ALOHA delar man in tiden i slots. En central klocka används sedan för att synkronisera alla terminaler. Terminalen får endast skicka ett paket i början av varje tidsintervall. 36% kapacitet (dubbelt så stor eftersom time vulnerable to collisions är halva jmfrt med pure).
c) Beskriv kortfattat hur CSMA/CD hanterar kollisioner? Varför finns det en minimalstorlek för ramar i CSMA/CD? Vad är relationen mellan denna ramstorlek och ’propagation time’? 
Svar: Se Anteckningar.
d) Vad är ’hidden terminal’ problemet som uppstår i trådlösa LAN, exempelvis WiFi? Hur löses problemet?
Svar: Se 

### Access till nät (L4)
- 5.1-6
-  **LAN:** där det både finns trådbundet (ethernet, gigabit ethernet vanligast) och trådlöst (WLAN) (används i de flest hushåll)
- **MAC:** Regler för hur och när terminalerna ska få sända data på länken.
Samma terminaler på länken måste använda sig av samma accessmetod så att dataöverföringen sker på ett kontrollerat sätt. Det finns olika accessmetoder enligt bild. Random access protocols är även kallad contention based. 
![[Pasted image 20230314111412.png|500]]
- **MTU** - största storleken på ett paket som kan skickas över nätverket. Iom IPv6 ej kan fragmenteras är det extra viktigt att just denna inte är större.
- **TTL** - Maxmängden av routrar som paket kan hoppa till innan den kastas. Efter varje router som tar emot paketet, minskar TTL tills 0, då slängs den. (bra för att inte få paket som cirkulerar förevigt)
- **Hidden terminal** - Detta problemet uppstår när två stycken trådlösa sationer, B och C, är utanför varandras transmissionsområde (transmission range) och försöker kommunicera med en tredje station A. Detta leder till att det sker en kollision för A. Undviks genom handshaking mechanism RTS/CTS/ACK.

#### CSMA/CD
- CSMA/CD detects collisions by monitoring the BUS after sending a frame. If the energy level on the link is significantly higher than that of a normal transmission, the sender concludes that a collision has occurred. For that, the colliding signal must have enough time to propagate to the sender before it has transmitted the frame’s last bit. The time required can be as long as twice the maximum propagation time (i.e. RTT on a link with maximum length). That’s why the frames have to be longer than a certain minimum size. 
**För att undvika kollisioner CSMA**:
- Interframe space - Terminalen väntar en tid IFS efter att den har detekterat att länekn är ledig, för att en annan terminal kan ha börjat sända.
- Contention window - Tidsintervall där en trminal väntar random antal intervall samtidigt som den lyssnar på länken efter någon annan terminalsändning
- Acknowledgement - time out för ala terminaler, ACK skickas om ramen korrekt mottagen. 

#### Polling
master - slave / primary - secondary
- Primär - styr access till länken
- Sekundär - Får skicka data enbart på begäran från primärdatorn. 
- Primär skickar POLL för data, sekundär svara med data eller NO-POLL
- Fördelar: Ingen kollision och fungerar i alla nättopologier
- Nackdelar: En terminal måste vara primärdator vilket gör det komplicerat. Om primärdator slutar funkar blir det ingen överföring.

#### Token ring
En turordning och alla får en rättvis del av kapaciteten. Terminalerna är kopplade i en ring och fungerar som sändare och mottagare. Terminalen med token får skicka ett datapaket|paket.
- Fördelar: Kapacitet delas upp lika mellan terminaler
- Nackdelar: Om det enbart är en terminal som vill skicka data kan den inte använda all kapacitet. Problematiskt om token försvinner genom bitfel. Komplicerat att koppla in och ut terminaler. 

#### Reservation
Grundprincipen är att en terminal måste reservera kanalen på något sätt innan den får skicka. Sedan skickar terminalen under den tiden den har reserverat kanalen. 

#### Läsa ramar
![[Pasted image 20230316192521.png|500]]

##### Exempeluppgifter:

**11 - ramstorlek vid överföring**
En tänkt 10 Mbps-länk ska användas för att överföra ramar enligt CSMA/CD. Länken måste vara 5 km lång. Utbredningshastigheten är 2/3 av ljushastigheten (300.000 km/s) i vakuum. Vad är den minsta ramstorleken som kan tillämpas så att systemet fungerar end-to-end?
	Svar: utbredninstiden: $t_{U}= \frac{l}{v_{U}} = \frac{5 \ km}{2 \cdot10^{5} \ km/s} = 2.5 \cdot 10^{-5} \ s = 25 \mu s$. 
	För CSMA/CD måste transmissionstiden vara $t_{T}$ > $2 \cdot t_{U}$ (round-trip time). Transmissionstiden är tiden att skicka iväg en ram med storlek $s_{Ram}$ på en länk med transmissionshastigheten $br_{T}$ (bit rate). 
	$t_T = \frac{s_{Ram}}{br_{T}}$$$\begin{align}  \frac{s_{Ram}}{br_{T}}>2 \cdot t_{U} \Leftrightarrow s_{ram} > br_{T} \cdot 2 \cdot t_{U} \Leftrightarrow s_{Ram} > 10 Mbps \cdot2 \cdot25 \mu s \\ \Leftrightarrow s_{Ram} > 10^{7}bps \cdot2 \cdot25 \cdot10^{-6} \ s \Leftrightarrow s_{Ram} > 500 bits = 62,5 \ B\end{align}$$

**12 - Data skickad mellan datorer**
Dator A i figuren nedan ska skicka 1 GB data till dator B. UDP över IPv6 används.  
- LAN A är ett Gigabit Ethernet (1000BASE-T) med MTU = 9.600 bytes.  
- LAN B är ett 10 Mbps Ethernet (10BASE-T) med MTU = 512 bytes.  
- LAN C är ett 100 Mbps Ethernet (100BASE-T) med MTU = 1.500 bytes.  
Fördröjningen i routrarna antas vara försumbar, och minneskapaciteten oändlig. Även utbredningstiden skall försummas.
![[Pasted image 20230314113538.png]]
Allmänt: 
MTU = max storlek på nätverkslagrets paket. Kommunikation är begränsad till min(MTU) = 512 B (maxgränsen på payload i ethernet) hela vägen eftersom IPv6 används. Varje IPv6-paket har en total overhead på 40 B (se header filen). UDP lägger till 8 B overhead. Total overhead blir 48 B. Payload blir då 512-48  = 464 B i varje IPv6-paket. Antal paket är $\frac{10^{9} \ B}{464 \ B} = 2155173$ (avrundat uppåt för att få med all data).
Ethernet tillför 8 + 14 + 4 = 26 B overhead per ram. Varje Ethernet-ram är alltså 512 + 26 = 538 B
a) Hur mycket data, overhead och payload, skickas totalt från dator A? Applikationslagrets overhead kan försummas.
	Svar:  Det skickas totalt 2155174 $\cdot$ 538 B = 1,16 $\cdot$ $10^{9}$ B (antal paket $\cdot$ data för varje ethernet ram)
	Alt. $10^{9}$ + 2155173 $\cdot$ (48 + 26 B) = 1,16 $\cdot \ 10^{9}$ B

b) Hur lång tid tar det för dator A att skicka iväg hela datamängden?
	Svar: LAN A (1 Gbps i transmissionshastighet) ger tid = $\frac{1,16 \cdot 10^{9} \cdot 8 \ bits}{10^{9} \ bits/s}= 9,28 \ s$. ($t = \frac{s}{v}$)
c) Hur lång tid tar det innan hela datamängden kommit fram till dator B?
	Svar: $\frac{9,28}{0,01} = 928 \ s$.


**13 - Ramar**
Givet följande 4 Ethernetramar som var och en kapslar in ett IPv4-paket. Preamble och SFD är borttagna.
![[Pasted image 20230314140921.png|400]]
Här är första bitarna fysiska lagret, destination, (ethernet/mac), sedan IP och sedan transport
a) Hur många hopp kan RAM 3 göra innan den slängs?
Svar: TTL: 0x02 = 2. 14 bytes i ethernetheader + 9 bytes i IPv4 Header (tills TTL)
(b) Vad är IP-adressen för paketens slutliga destination?
Svar: IP destination: 0x82 ed 1c 28 vilket konverteras till 130.237.28.40
(c) Till vilken MAC-adress skickas ramarna?  
Svar: (alla har samma destination), första 6 bytes är densamma för alla (destination adress), alltså 0x 00 00 5e 00 01 01 
(d) Vad för typ av konversation som vi ser delar av? 
Svar: Traceroute. Alla ramar och paket har samma destination men TTL-fältet ökar för varje IP-paket och därmed ram (går från 01 till 04). 
(e) Vad saknas i konversationen?
Svar: ICMP echo reply saknas då vi ser ett ICMP echo request. Vi ser ICMP echo request genom att räkna oss igenom 16 bytes för ethernet sedan 20 för hela IP och så kan vi se att 08 ger en echo request. 

**Extra - ramar**
Givet följande Ethernet-ramar där preamble, SFD och CRC är borttaget: 
![[Pasted image 20230316192354.png]]
a) Vilken/vilka flaggor är satta i IP-headern i ram 1 och vad betyder det? 
Svar: Eftersom type field är 0800 är det IPv4. Flagga är på 40 (hexadecimalt) vilket innebär "D: 0x40 Do Not Fragment" $\Rightarrow$ Do Not Fragment.
b) Vilka tre mottagaradresser finns i ram 2? Ange de tre adresserna samt varför de behövs. 
Svar. 14 steg fram för ethernet. Sedan i payloaden är det IPv4 och där tar vi 16 steg fram för att komma till destination adress (som är 4 bytes stor) $\rightarrow$ *Destination IP*: 82 eb 12 bd. Vi vet även *MAC-address* (från ethernet destination) är 00 07 74 41 af a7. Vi vet att TCP används från att kolla på Protocol på IPv4 header. För att hitta TCP destination behöver vi först gå 14 steg för ethernet, sedan 20 steg för hela IPv4 o sen 3 steg till destination port (3 o 4). *TCP Destination* blir alltså 09 93.
c) Ange vilket protokoll som används på lager 4. 
Svar: TCP används. 
d) Rita ett händelseschema. Meddelanden ritas som pilar mellan två tidslinjer, en för varje värd, i diagrammet. För varje meddelande ska de satta flaggorna på lager 4 anges. Vad gör den här sekvensen av meddelanden?
Svar: Se på uppkopplingsfas i anteckningar. SYN - SYN och ACK - ACK vilket utgör en TCP handshake

**14 - throughput, överföring av ramar**
I bild 5 visas scenariot ifrån labb 2 där en Development Node kommunicerade med en Master Node via en Access Point. Development Node skickade ramar innehållandes data och Master Node svarade direkt med ett ACK. Bithastigheten var 10 bps och en ram var 48 bitar lång.  
Antag istället att båda noderna skickar data och att vi använder oss av pure ALOHA men inte Stop-and-Wait ARQ. En nod kan inte generera en ny dataram medans den skickar eller tar emot en ram. Nodernas försök att skicka ramar är enligt en Poissonfördelning. Med dessa antaganden kan det i pure ALOHA visas att om antalet dataramar genererade under den tiden det tar att skicka en ram är G, så är antalet lyckade sändningar i genomsnitt $S = G \cdot e^{-2G}$
(a) Vad blir det för throughput om det totalt produceras 360 ramar med data per timme?  
Svar: Frame transmission time = $\frac{\text{frame size}\cdot2}{\text{bit rate}}= \frac{96}{10}=9,6 \ s$.
Antal ramar per sek = $\frac{360}{3600} = 0,1$. Med detta kan vi räkna ut antal ramar producerade under en frame transmission time $G = 0,1 \cdot 9,6 = 0,96$ och vi får då $S = G \cdot e^{-2G} = 0,1407$
(b) Hur många ramar med data per timme skulle det behöva vara totalt för att vi skulle kunna uppnå maximal throughput för pure ALOHA? Vad är effektiviteten då?
Svar: Max throughput när G = 0,5. effektiviteten blir $S = 18,39$%
Antal ramar producerade per timme blir då $\frac{0,5}{9,6} \cdot 3600 = 187,5$.


## Network layer (L5-L6)
- 6.2-3, 7.1-3, 8.1-5
- 7.4-6, 7.8, 12.10
- Nivån som hanterar paketadressering, routing och fraktionshantering. Här väljer man bässta vägar för paketet. Man använder IP-protokoll.

#### Internet Protocol - IP
Kan bestå av tre skikt: nät, transport och applikation. 
- På nätnivå finns endast IP, två versioner - 4 och 6.
- På transportnivå finns TCPv4 och TCPv6 och UDP
- På applikationsnivå finns massa olika, t.ex http, SMTP och ftp.config
- **MTU** - maximum transfer unit (max ramar). Inkluderar INTE headern för ethernet.

Adressering och routing: 
- Nätadress: Adressering som är gemensam för alla nät 
- Routing: Regler för hur data skickas mellan nät 
- Router: Nätenhet som är kopplade till flera nät och kan skicka data mellan nät

#### IPv4
Ett datagram som består av header och payload (nyttolast). Totalt 65536 bytes.
- 34 bitar
- Kan fragmenteras hos en router. Fragmentering kan ske flera gånger under paketets väg då IPv4 skickas ut så att endast nästa länk klarar det osv.
- 
**Addressering**:
- adressen är 32 bitar. 
**Header**:
- Headern består av 20-60 byte.
- s. 139-140 visar mer förklaring.
**Fragmentering**:
- Om datagram längre än länkprotokollets MTU $\Rightarrow$ fragmentera. Varje fragmet får egen header
- Vid fragmentering kopieras alla fält i headern förutom flaggor, fragment offset och total längd.
- Se exempel för CIDR

#### IPv6
- 128 bitar / 26 bytes
- Tillåter inte fragmentering hos router, men har fragmenteringsmekanism själv. Den fragmenterar automatiskt. Om en väg inte klarar längden får paketet kastas, drf måste sändaren veta hur paketet ska skickas genom nätet.
- Vid adressering för IPv6 kan man förkorta. Kom ihåg att dubbla semikolon kan ersätta hela följder av nollor MEN endast en gång
- Jämfört med IPv4 har denna fler adresser, bättre headerformat, funktioner för realtidsdata, säkerhetsfunktioner och möjlighet till utökning av protokollet. 
**Addressering**:
- 16 bytes, skrivs hexadecimalt för att den är så lång
**Nedkortnings av IPv6**:
short form = F331:F3::3F 
long form = F331:00F3:0000:0000:0000:0000:0000:003F 
**Byte av IP form**:
IPv6 $\rightarrow$ IPv4 genom dual stack, tunnelling eller header translation.
**Header**: Datagrammet har en basheader och payload. Payloaden har eventuella extra headers för tillvalsfunktioner och data. 
- Längd 40 bytes och payload kan ha 65 535 bytes.

#### Overhead
- Onödig data (överflödig data). 
- Varje skikt bidrar med en egen header som drar ned prestandan. 


#### ICMP - Internet Control Message Protocol
- Hjälpprotokoll till IP på nätskiktet. (både v4 o v6)
- Utvecklats i viss mån för att kompensera för Internetprotokoll|IPs saknande av feldetektering, felkorrigering och hjälpfunktioner (även ge status)
- It is a protocol used by network devices, such as routers, to communicate error messages and operational information about the status of the network. It is used to provide feedback about issues with network packets, such as when a packet cannot reach its intended destination, when a network is congested, or when a device is unavailable. ICMP messages are usually generated by network devices and sent to the source of the problematic packet, providing feedback to help diagnose and resolve network issues.
-  Finns tre olika ICMP messages: *Echo request*, *Time exceeded* och *destination unreachable*. TTL count ökar vid varje echo request för att hitta en router (varje gång det passerar en router). t uses wrong port number to get DR from destination.
**Ping command**: Använder sig av ICMP (Echo). Används för att se om 
	- Om en remote host är aktiv eller inte 
	- Round trip delayn för kommunikationen med host 
	- Data förluster (Packet loss) 
	Ping kommandot skickar iväg en echo request till en adress, sen väntar den på ett svar. Pingen är lyckad om: 
	- Echo request kommer fram till destinationen
	- Echo meddelandet kommer tillbaka på den bestämda tiden som kallas timeout. TTL värde i echo request kan inte ändras.
**TTL timer**: Räknas ner när ett datagram passerar en router (t.ex om man har 3 i timer så delas först 1 ut, sen 2 och sen 3). När det blir noll så kastas datagrammet och ICMP meddelande till användaren skickas ut.
**Traceroute**: Traceroute är ett sätt att trace paketets route från sändare till mottagare. Oftast för att felsöka då man inte vet vart felet skett. Tracear paketens path när den åker genom IP nätverket (från source till destination). Den skickar paket med växande TTL värden (1 för första datagrammet, 2 för andra osv) som får routrar att skicka ICMP meddelanden vart datagrammet hamnade (när alla TTL delats ut/tagit slut). Genom detta kan traceroute göra en lista med alla routrar som paketet passeras. När TTL nått noll kommer routern skicka tillbaka time exceeded. Om man vill kan man få mottagaren att svara med destination unreachable.

#### IGMP - Internet Group Management Protocol
Ett protokoll som används för att hantera och övervaka IP-multicastgrupper på ett nätverk. IGMP möjliggör kommunikation mellan en multicast-sändare och mottagare genom att möjliggöra skapandet av en multicast-trädstruktur. 
- En metod för att skicka IP datagram tilll en grupp av intresserade mottagare i en enda transmission.

#### ARP - Adress Resolution Protocol
-  Används för att hitta MAC-adressen för en värddator om man vet Internetprotokoll|IP-adressen för denna värddator. 
Ett protokoll inom datanätverk som används för att mappa en IP-adress till en fysisk adress (MAC-adress). När en dator vill skicka data till en annan dator på nätverket, behöver den veta mottagarens MAC-adress. Då skickar den ut en ARP-förfrågan som innehåller mottagarens IP-adress. Alla datorer på nätverket som hör förfrågan svarar med sin MAC-adress, och den efterfrågande datorn sparar sedan informationen i en tabell för att slippa göra samma förfrågan igen i framtiden. ARP fungerar på datalänknivå (Layer 2 i OSI-modellen) och används i lokala nätverk.
- Ingen IP header när ARP används.
- ARP Request och ARP Reply
Om mottagern är på ett annat nätverk, vilket man kan se i IPn, behöver inte sändaren mottagarens MAC-address och skickar därför den till "Default Gate" istället. Den kommer i sin tur vidarebifoga den till mottagaren. Så när sändaren skickar det till "Default Gaten" kommer man ha "Default Gatens" MAC-address, men ha kvar IPn till den rätta motagaren.

#### Router
- Ingångar, utgångar (interface), buffertminnen och vägväljarmodul (kopplar samman ingångar och utgångar, väljer väg)
- **Vägväljare** - hit är ett antal länkar kopplade. Vägväljaren skickar vidare paketet ut på nästa länk i nätet (till destination). Inport/utport. Vägväljaren bestämmer vilken. Finns algoritmer för detta...
- **Forwarding** - Nätet förflyttar datagrammen (försedd med avsändaradress och mottagaradress) genom nätet till mottagaren på det sätt som just då är det bästa. Datagrammen tas emot som ramar, enligt aktuellt länkprotokoll. Där tas kontrollinformationen bort så skickas resterande vidare till vägväljarmodulen. Vägväljarmodulen beräknar bästa väg, där den sedan bestämmer vilken utgång datagrammet ska skickas från.

#### Routing (och olika algoritmer)
Används då routern behöver veta hur nätet ser ut innan det skickar iväg datagram. Routern har en *routing table* som håller koll på kommande hopp.
**Dikjstras algoritm**: Shortest Path First (SPF), s 169-178
Används för att beräkna Spanning (shortest path) tree. (se exempel)
**Bellman-Fords algoritm**:
Noderna skickar "distance vectors", som ger info om närliggande noders listor.
- Om nod flrsvinner kommer närliggande noder upptäcka det vid nästa annonseringstillfälle. Vektorn tas då bort från närliggande noders lista soms sedan sänds vidare vid nästa tillfälle. Detta kan dock skapa ghost-vägar som sker när en nod skickar sin vektor periodiskt så närliggande noder till noden som försvann tror att den finns. 

#### Ny dator ansluter sig till ett nätverk
Saker som behövs för att internet ska fungera:
- IP-adress
- Subnetsmask
- Standard gateway
- DNS-serveradress
Datorn kan normalt få dessa parametrar från en DHCP-server (Dynamic Host Configuration Protocol) som är konfigurerad på det lokala nätverket. DHCP-servern tilldelar datorn en IP-adress, subnätmask och standardgateway. DNS-serveradresser kan också tilldelas via DHCP eller konfigureras manuellt på datorn.
- DHCP (dynamisk tilldelning)
- Statisk tilldelning - adminstratören sköter manuellt. 

### Exempeluppgifter på Network Layer

**15 - Router**
A. En router sägs arbeta på nätverksnivån. Men vilka lager måste en router också förstå för att kunna fungera? 
Svar: Den måste även förstå det fysiska lagret och (data)länklagret, annars kan den ej kommunicera på ett LAN
B. En router vidarebefordrar IP-paket. Dock två fält i ett IPv4-paket som går genom en router måste ändras. Vilka, och varför? 
Svar: TTL-fältet räknas ner för varje router paketet passerar. Eftersom IPv4-headern ändras måste då även checksum i headern ändras.
C. En router innehåller köer (buffer) både på ingångar och utgångar. Varför behövs dessa? Förklara också varför köerna medför fördröjning (delay).
Svar: Köer behövs för att routern inte ska behöva slänga paket om den är upptagen. In-köerna behövs för att inkommande paket kan behöva vänta på att behandlas. Ut-köerna behövs för att utgående paket måste vänta om utgående länk är upptagen. Fördröjnings uppstår i köerna när paketen måste vänta på att bli behandlade. 

**Extra - P2P och dual stack m.m**
Vi har två IP-baserade nät som är sammankopplade med en punkt-till-punktlänk (p2p-länk). Både IPv4 och IPv6 körs parallellt (Dual Stack). På grund av länkens bristande tillförlitlighet är ARQ-metoden Stop-and-Wait implementerad. Länken använder Half Duplex. Nedan följer ett antal påståenden om p2p-länken, som kan vara antingen sanna eller falska. För varje påstående ange om det är sant eller falskt och motivera varför. 
a) Routrarnas respektive interface på p2p-länken behöver inte ha adresser på länknivån (MAC-adresser) för att routingen mellan de två näten skall fungera. 
Svar: *Sant* - Så länge respektive router känner till vilket nästa hopp är för varje destination och vilket interface detta nästa hopp ansluter krävs inga MAC-adresser.
b) P2p-länkens ram måste ha en payload (MTU) som är stor nog att ha plats för de allra största IP-paketen. 
Svar: *Falskt* - Både IPv4 och IPv6 har fragmenteringsmekanismer
c) Eftersom Stop-and-Wait används, räcker det med att ramheaderns sekvensnummerfält har plats för en binär siffra, en bit. 
Svar: *Sant* - För att Stop-and-Wait ska klara av alla felfall måste minst två olika sekvensnummer användas, exempelvis 0 och 1
d) P2p-länk kräver kollisionshantering i någon form. 
Svar: *Sant* - Använder half duplex, så det kan förekomma kollisioner om båda skickar samtidigt annars.
e) Eftersom p2p-länken kopplar samman två IP-baserade nät är ARQ på länken omotiverad; den önskade funktionaliteten finns i TCP/IP-stacken.
Svar: *Falskt* - Endast TCP tillhandahåller tillförlitlighet, och då hela vägen från host till host. UDP/IP är best effort. En eventuell omsändning/felkorrektion berör hela vägen från källa till destination; ARQ är inte onödigt


##### Exempeluppgifter på CIDR

**16 - CIDR på IPv4**
a) Enligt CIDR-beteckning anges antal konsekutiva ettor i en IPv4-adress nätmask i /xx form direkt efter adressen. En av IP-adresserna i ett subnät är 255.230.64.47/26. Vad är den första respektive den sista IP-adressen i detta subnät? Hur många adresser har tilldelats? 
Svar: Subnätsmasken är 26 bitar (nät-id). Alltså är host-id 32-26 = 6 bitar (6 st nollor) Vi har alltså tilldelats $2^{6}=64$ adresser. I adressen har vi 47 vilket binärt är 00101111, där 00 på början tillhör masken och resterande host-id. Blocket måste alltså börja med 000000 och sluta med 111111. (00)(000000)= och (00)(111111) = 63. 
Alltså är blockets första adress 255.230.64.0 och sista 255.230.64.63.

b) I ett IPv4-nät behöver man allokera adresser för 750 datorer, var och en med en egen unik IP-adress. Ange den längsta nätmasken som uppfyller kravet. Antalet konsekutiva ettor i nätmasken avser dess längd. 255.255.255.0 är således längre än 255.255.0.0.   
Svar: Då vi tar det närmsta $2^{x}$ som innehåller fler än 750 adresser får vi en storlek på blocket som är 750.  Dvs $2^{10}$. Nätmaskens längd blir därmed 32-10 = 22 bitar. Detta motsvarar 11111111 11111111 11111100 00000000 = 255.255.252.0 i decimal form. 

c) Hur ser följande IPv6-adresser ut i förkortat / oförkortat form?  
- 56A7:0345:0000:0000:0000:000A:1A4C:B200 -- i förkortat form  
- F331:0:0:34A::7 -- i oförkortat form
Svar: Förkortat form: 56A7:345::A:1A4C:B200 
Oförkortat form: F331:0000:0000:034A:0000:0000:0000:0007

**17 - CIDR IPv4**
Ett block IPv4-addresser identifieras med hjälp av 123.123.128.0/18 (CIDR-beteckning). Antag att blocket delas i 4 lika stora subnät.  

a) Vad är den gemensamma subnät-masken för alla subnäten?
Svar: subnätsmasken är 18 bitar (nät-id). 4 subnät kräver 2 bitar (1 bit per 2 subnät) till för identifiering, dvs 20 bitar (ettor) i subnätsmasken. Vi får ett host-id på 32-20 = 12 bitar (12 st nollor). 
Skriver om adressen till binärt ger 0111 1011 0111 1011 1000 0000 0000 0000.
Om vi skriver subnätmasken får vi 1111 1111 1111 1111 1111 0000 0000 0000.
(skriv upp dessa över varandra och se vilka man kan röra, de sista nollorna kan man ändra då ettorna visar att de är fasta.)
Bara av att kolla på subnätmasken får vi den gemensamma 255.255.240.0

b) Ange adresserna till näten (med CIDR-beteckning).  
(se truls bild)
Subnät 1: 123.123.128.0/20
Subnät 2: 123.123.144.0/20
Subnät 3: 123.123.160.0/20
Subnät 4: 123.123.176.0/20
![[Pasted image 20230315114254.png|450]]

c) Hur många användbara IPv4-adresser finns det i ett subnät? Varför?
Svar: 12 bitar i host id , $2^{12} = 4096$
 olika adresser. Minus 2 bitar (från innan) blir det 4094 kvar. 

**Extra - CIDR IPv4**
Ett block IPv4-adresser identifieras med hjälp av 200.1.128.0/20 (CIDR-beteckning).
a) Vad är blockets subnet-mask?
Svar: 255.255.240.0
b) Antag att blocket delas i 16 lika stora sub-nät. Vad är den gemensamma subnet-masken till dessa? 
Svar: 16 sub-nät ger 4 bitar för att täcka det. nya subnätsmasken blir 24 bitar $\Rightarrow$ 255.255.255.0.
c) Hur många IPv4-adresser finns det i ett sub-nät? 
Svar: 0-255 ger 256 adresser.
d) Ange den första respektive den sista användbara adressen av det sista sub-nätet i detta block.
Svar: 
![[Pasted image 20230316171113.png]]
 
**18 - CIDR**
a) Du jobbar som administratör hos en ISP som äger adressblocket 128.20.224.0/20 (CIDR-beteckning). Du har två kunder som behöver adresser till sina 1000 datorer vardera, två som behöver 500, samt två som behöver 250. Vilka adressblock tilldelar du dessa 6 kunder?
Svar: 
![[Pasted image 20230315161626.png]]

b) Hur ser följande IPv6-adresser ut i förkortad/oförkortad form?  
(i) 56A7:0000:0000:00AA:0C03:0000:3003:FF22 – i förkortad form  
Svar: 56A7 :: AA : C03 : 0 : 3003 : FF22
(ii) 0000:0000:0000:FFFF:0000:AAA7:0000:0000 – i förkortad form  
Svar: :: FFFF : 0 : AAA7 : 0 : 0 
(iii) F331:F3::3F – i oförkortad form  
Svar: F331 : 00F3 : 0000 : 0000 : 0000 : 0000 : 0000 : 003F
(iv) 0:0:DD33:E::0 – i oförkortad form
Svar: 0000 : 0000 : DD33 : 000E : 0000 : 0000 : 0000 : 0000

##### Exempeluppgifter på forwarding och routing

**19 - forwarding**
Givet forwarding-tabellen i tabell 1, ange adressen till nästa nod för följande IP-adresser.
![[Pasted image 20230315131514.png|400]]
a) 130.236.128.100  
Svar: 129.100.1.1 DEFAULT ROUTE (eftersom 130.235.0.0/16 täcker enda till 130.235.255.255).
b) 84.24.2.254  
Svar:
![[Pasted image 20230315134237.png|450]]
4.236.17.9 DIRECT MATCH eftersom  84.24.0.0/22 täcker enda till 84.24.3.255
c) 191.231.194.12
Svar: 181.13.62.5 DIRECT MATCH (täcker enda till .63) Här täcks det även av den under, men denna "täcker först".

**20 - forwarding**
a)
![[Pasted image 20230315170725.png|350]]
Givet forwarding-tabellen, ange adressen till nästa nod för följande IP-adresser. 
(i) 191.231.194.86  
Svar: 73.32.56.123. Rad 2 täcker ej då 6 st nollor endast ger 63 adresser och vi behöver 86. 
(ii) 100.100.12.234 
Svar: Rad 4 ger (27 nät-id) 5 st nollor, alltså 31 adresser vilket ger att den täcker 160 till 191. Detta täcker ej 234. Vi får till default gateway $\Rightarrow$ 112.123.89.1 (default route)
(iii) 84.34.23.10  
Svar: Rad 3 täcker ej $\Rightarrow$ default route, 112.123.89.1
(iv) 130.235.128.100
Svar: Rad 1 ger 16 nollor, eftersom det är två stycken oktetter som ändras i detta fall får vi $2^{16} = 65536$ adresser alltså 0-65535. Det kommer täcka. Alltså - 81.12.32.104

##### Exempeluppgifter på kommunikation mellan enheter

**21 - Requests mellan enheter**
I figuren nedan visas ett nätverk. Dator A ska skicka ett ICMP request-meddelande till dator C. Dator A känner inte till C:s IP-adress, men väl dess DNS-namn. Nätet mellan Router1 och Router2 är ett så kallat broadcastnät med mutiple access. Alla i figuren visade enheter har precis initialiserats  
och således är alla cachar och adresstabeller tomma. All nödvändig konfiguration är dock utförd.
![[Pasted image 20230314175440.png|450]]
Visa i tidsordning alla ramar som syns vid pilen märkt 1 och dessa ramars innehåll. Börja med den första ramen som skickas fram till och med ICMP request-meddelandet. Av ditt svar ska framgå varje rams avsändar- och destinationsadress på länk- och nätverkslagret och vilken typ av meddelande som skickas.  
Tips: Använd en tabell som nedan för ditt svar. Använd ($*$) för broadcast-adresser.
Svar:
Med MAC(Router1) resp. IP(Router1) avses nedan MAC och IP för interfacet som ansluter routern till nätet som ansluter till switchen.
![[Pasted image 20230314191623.png|500]]![[Pasted image 20230314191634.png|500]]

##### Exempeluppgifter på vägväljar-algoritmer

**22 - Bellman**
![[Pasted image 20230314193435.png|450]]
I Bellman-Fords algoritm skickar noderna så kallade 'distance vectors' till sina direktanslutna grannar för att sedan skapa varsin routingtabell. I nätverket ovan skickas dessa vektorer med viss  
periodicitet.  
A. Hur ser nod C:s initiala vektor ut?
![[Pasted image 20230314202241.png|400]]
B. Hur uppdateras C:s vektor/routingtabell efter att den fått nod F:s initiala vektor? Förklara rad för rad hur du resonerar. 
Nod F:s initiala vektor:
![[Pasted image 20230314202323.png|450]]
Kostnaden (C-F) är 2 så alla dessa kostnader måste ökas med 2 och sedan jämföras med C:s egna tabell rad för rad enligt Bellman-Ford. Den uppdaterade versionen för C blir:
![[Pasted image 20230314202534.png|450]]
C. Antag nu att nod A kraschar. Hur måste C agera?
Om A försvinner, upptäcker C detta vid nästa annonseringstillfälle när det inte ankommer någon vektor från A. Då måste C ta bort A från sin vektor. (Hade C haft rad i vektorn med A som nästa nod, hade C tagit bort även dessa.) Sedan kan C skicka sin uppdaterade vektor vid nästa  
tillfälle.
D. Routingalgoritmen Distance Vector kan sammanfattas med uttrycket "good news travel fast, bad news travel slow." Varför?
Det tar längre tid att vidarebefordra information om fel i nätverket (som när en nod eller länk kraschar). Kan till och med ta fler annonseringserioder att upptäcka felet (i externa fall). Pga detta kan det även uppstå "ghost-vägar", som är att t.ex A försvinner och C tar bort den, men innan C hinner skicka en update så skickar F sin vektor som innehåller A. Till slut kommer C tro att den kan nå A via F $\Rightarrow$ fel.

**23 - Bellman**
Noderna A, B, C, D, E, G och H bildar ett nätverk, och i bild 1 visas deras routing-tabeller med destination (d), total kostnad (c) och nästa nod (n). *I tabellerna representerar ’-’ en direktlänk*. När man ritar kan man endast utgå ifrån direktlänkar, ist för att kolla på allt.
![[Pasted image 20230315114906.png]]
a) Rita grafen som beskriver nätverket. Samtliga noder, länkar och kostnader ska vara med.  
![[Pasted image 20230315120431.png|300]]
b) Antag att en ny nod F anslutas till nätet med två länkar F-C (kostnad 1) samt F-E (kostnad 2). Nu ska nätverkets samtliga routing-tabeller uppdateras enligt Bellman-Ford-algoritmen. Ange steg för steg hur uppdateringen sker hos nod F. Visa hur den nya nodens routing-tabell ser ut precis när den anslutas och efter varje steg.
Svar: F har initialt endast tre rader (kopplingar) som är C,E och F. Sedan kommer uppdatering till C och E ske, där ordning ej spelar roll i slutet. Jämför först med en av de och sedan den andra och se vilken väg som är billigast till slutgiltiga tabellen.
![[Pasted image 20230315121440.png|450]]


**24 - Dikjstras**
I bild 2 visas ett nätverk med 7 noder. Bredvid varje länk anges även dess kostnad. Antag att nätet använder sig av Link State och att alla noder precis har skickat ut en uppdatering. Skapa ett “spanning (shortest path) tree” från nod A till de andra noderna. Visa steg för steg (dvs. i kronologisk ordning) hur algoritmen fungerar. Ange A:s resulterande routingtabell.
![[Pasted image 20230315135733.png|350]]
Svar: Spanning -> Dikjstras algoritm
![[Pasted image 20230315203533.png|500]]
![[Pasted image 20230315203602.png]]

**25 - Dikjstras**
b) 
![[Pasted image 20230315174225.png|400]]
I bilden visas ett nätverk med 9 noder. Bredvid varje länk anges även dess kostnad. Samtliga noder kan hela topologin eftersom de precis fått “link state” informationen av varandra genom flooding. Tillämpa Dijkstras algoritm och skapa ett “spanning (shortest path) tree” från nod E till de andra noderna. Visa steg för steg (dvs i kronologisk ordning) hur algoritmen fungerar. Ange E:s resulterande routingtabell.
Svar:
![[Pasted image 20230315174631.png|600]]
![[Pasted image 20230315175441.png|400]]

## Transport Layer (L7)
- 10.1-3
- Lagret som hanterar kommunikation mellan applikationslagret och nätverkslagret. Säkerställer en pålitligt dataöverföring mellan applikationer som körs på olika värdar. Använder TCP och UDP.
- **Congestion control** - Congestion (överbelastning) control is a set of techniques and mechanisms used to manage and prevent congestion in computer networks. When the amount of traffic in a network exceeds the available network resources, congestion occurs. Congestion control techniques aim to ensure that network resources are used efficiently and fairly, while also avoiding network instability or collapse. Overall, congestion control is essential for maintaining the performance and stability of computer networks, especially in high-traffic environments.
	Some common techniques are: 
		- Traffic shaping: This involves controlling the rate at which data is sent to prevent the network from becoming congested.
		- Admission control: This involves limiting the number of connections that can be established to prevent the network from becoming overloaded.
		- Quality of Service (QoS): This involves prioritizing certain types of traffic over others to ensure that critical applications receive the necessary network resources.
		- Flow control: This involves controlling the rate at which data is transmitted between devices to prevent the network from becoming congested.
- **Flow control** (a type of congestion control) - Flow control is a mechanism used in communication networks to regulate the rate of data transmission between two devices to prevent overloading of the receiving device. It ensures that the sender does not transmit data at a faster rate than the receiver can handle. Flow control can be implemented using several techniques, such as buffering, windowing, and feedback-based mechanisms. By regulating the flow of data, flow control helps to prevent data loss and reduce network congestion.

#### TCP
- Transportprotokoll som används för en kontrollerad och tillförlitlig dataöverföring. Den är förbindelseorienterad och felfri. 
- TCP står för Transmission Control Protocol och är en av de viktigaste protokollen för datakommunikation över nätverk. TCP används för att säkerställa att data skickas på ett tillförlitligt sätt från en dator till en annan över internet eller andra nätverk. Protokollet hanterar flödet av information mellan datorer genom att kontrollera och övervaka överföringen av paket och säkerställa att alla paket når sin destination på rätt sätt och i rätt ordning. TCP används ofta i kombination med IP (Internet Protocol) och tillsammans bildar de TCP/IP, som är en grundläggande del av internet.
- Delar upp data i olika segment som sedan överförs. Sparar segment som kommer i fel ordning och sorterar dessa som sedan skickas till app.
- Innehåller felhantering och flödeskontroll
- Port 80
- Användningsområden: Web browsing och nedladdning av filer 
- Se nedan för "three way handshake" även kallad TCP-handshake
- **Uppkopplingsfas:**
 ![[Pasted image 20230316105711.png|450]]
 - **Nedkopplingsfas:**
 ![[Pasted image 20230316105741.png|450]]

#### UDP (User Datagram Protocol)
- Ett kommunikationsprotokoll som används för att skicka datagram (datasegment) över nätverket. 
- UDP används ofta för applikationer som kräver högre överföringshastigheter och mindre fördröjning, exempelvis videosändningar och röstöverföring (VoIP). Eftersom det inte finns någon tillförlitlig överföring av data, kan det emellertid leda till att vissa datasegment försvinner eller anländer i fel ordning, vilket kan påverka applikationens prestanda eller funktionalitet. Det är därför viktigt att applikationen själv hanterar eventuella fel som kan uppstå när den använder UDP.
- Ingen error hantering, men error check
- Ingen flow control, låg latency, ingen ACK
- Port 67 och 68
- Användningsområden: Live-streaming (realtidsapplikationer), där det är känsligt för fördröjningar. Även för broadcast situationer (youtube osv)

**Skillnader mellan UDP och TCP:**
Till skillnad från TCP är UDP ett icke-anslutningsorienterat protokoll, vilket innebär att det inte etablerar en pålitlig dataförbindelse mellan två enheter innan dataöverföringen påbörjas. 
- UDP förbindeslefritt, TCP förbindelseorienterat
- TCP har felhantering, inte UDP
- UDP kan skicka data i fel ordning
- UDP har fokus på snabbt och TCP på robusthet (korrekt data)

#### DHCP (Dynamic Host Configuration Protocol)
Används av en dator för att få en IP-adress. Samt information om närmaste router som kopplar ut mot Internet och DNS-server.
- Vid anrop på DHCP får man tillbaka en tilldelad ledig IP. 
- Använder UDP.

#### Data flow
- Direction in which data is transmitted between to devices or nodes.
- Simplex: flow only in one way. (television)
- Half-duplex: Both directions but only one can transmit at a time (walkie-talkie)
- Full-duplex: Both directions simultaneously (telephone)

#### Multiplexering
**Frekvensmultiplexering**: Bandbredden delas upp i frekvensband där varje kanal tilldelas ett frekvensband. Används för marksända tv och radio kanaler. P.g.a. detta kan varje kanal överföra information i sitt frekvensband.
**Synkron tidsmultipluxering**: Här delas länken upp genom att man turas om att skicka information. Tiden delas in i ramar med konstant längd, och varje ram innehåller "slots" som varje kanal blir tilldelad som är konstanta. För att underlätta med synkronisering brukar varje frame börja med en synkroniserings bit.
**Statistisk tidsmultiplexering**: Man delar länken, men man får en "slot" när man vill skicka data, istället för att den ska va indelade i statiska slots man får skicka. Man delar länken, men man får en "slot" när man vill skicka data, istället för att den ska va indelade i statiska slots man får skicka.

##### QUIC
- Ett överföringsprotokoll som förbättrar prestanda för förbindelseorienterade web-appar (som använder TCP).
- Flyttar även flow control till appskifkt ist för OS.
- QUIC är ett applikationsprotokoll som använder UDP. Används dock som ett transportprotokoll.
- **SCTP** - är ett annat alternativt protokoll som kombinerar UDP och TCP.

#### Exempeluppgifter på TCP och UDP (transport)

**26 - TCP och UDP**
Två viktiga protokoll på lager 4 är TCP och UDP.  
a) Beskriv tre viktiga skillnader mellan TCP och UDP.  
Svar: 1. TCP sätter upp en kanal för utbyte mellan två datorer medan UDP skickar varje paket individuellt. Alltså är *TCP förbindelseorienterat* till skillnad från UDP. 2. TCP har feldetektering. 3. TCP använder Go-back-N, medan för ett UDP är ett tappat paket borta. 4. TCP ser till att paket levereras till högre lager i rätt följd medan UDP skickar vidare ett paket oberoende av de övriga.

b) Ange två applikationer (eller typer av service) där du skulle föredra TCP framför UDP.  
Svar: Web browsing och nedladdning av filer (då den begärda filen måste komma fram felfritt). Nackdelen är att det kan förekomma fördröjningar.

c) Ange två applikationer (eller typer av service) där du skulle föredra UDP framför TCP.
Svar: Realtiddsapplikationer (live-streaming), då det är känsligt för fördröjningar (mer än att förlora ett paket). Även bättre i en broadcasting situation där material ska nå många mottagare.

**27 - Skicka fil, räkna bytes**
En dator, ansluten till ett 100BASE-T (100Mbps) Ethernet, skickar en större fil med hjälp av TCP över IPv6. Sändfönstret av TCP tillåter att 100 000 bytes skickas. Hur lång tid tar det att skicka alla byte i sändfönstret? Det förutsätts att segmentstorleken av TCP är anpassad till en fullständigt utnyttjad payload för en Ethernetram, att inga ACK emottages innan sändfönstret  
är helt utnyttjat samt att inga optioner används.
Svar: Utifrån header-fieln får vi:
- IPv6 header = 40 bytes, TCP header = 20 byte, Ethernet max payload = 1500 bytes, vilket fer 1500 - (40+20) = 1440 byte data per Ethernet-ram. 
- Antal ramar är $\frac{100000}{1440} = 70$, där varje ethernet-ram har 7 + 1 + 14 + 4 = 26 byte overhead. 
- Alltså måste det skickas $70 \cdot (1500 + 26) = 106 820$ bytes, vilket tar $\frac{8 \cdot 106820}{100 \cdot 10^{6}} = 8,55 \ millisekunder$. (måste multiplicera med 8 för att få det i bits)

**28 - Uppkoppling i nät (ny dator)**
I bilden visas ett nätverk. R är en router, S1 och S2 switchar, och H en hub. Dator A är en DHCP-server och DNS är en DNS-server. Antag att dator E nyligen har kopplats in på nätverket och att den ska precis ansluta sig till nätverket. Tips: Använd en tabell som visar Source (L3), Destination (L3), Protokoll (L4), Innehåll för varje paket i ditt svar till deluppgift C.
![[Pasted image 20230315195750.png|400]]
a) Vilka 4 viktiga parametrar behöver E veta från nätverket och varför behövs dessa? Beskriv hur E får reda på parametrarna. Ange vilka paket som skickas och till vem de är adresserade.
Svar: E behöver veta 
-  IP-adress för att kunna ansluta (på lager 3). 
- Subnet mask (för att veta vilka andra adresser som finns i det lokala nätet). 
- Default Gateway (för att hitta ut till omvärlden). 4. DNS server (för att översätta URL-namn till globala IP-adresser).
b) Vilka IP subnät kan identifieras i nätverket?
Svar: 3 olika
![[Pasted image 20230315203736.png|300]]
c) En stund senare ska dator E sätta upp en TCP-förbindelse med dator G för att skicka ett HTTP-anrop till och hämta en HTML-sida ifrån www.MyWeb.com som G är värd för. Antag att alla ARP-tabeller är fullständigt ifyllda. Vilka paket passerar routern R? Ange adressering (source, destination) på lager 3, protokoll på lager 4 samt paketens innehåll. Antag att DNS-anrop använder UDP.
Svar:
![[Pasted image 20230315203920.png|550]]

**29 - Control och routing**
a) Antag ett nätverk där, för varje länk, länkkapaciteten är högre än summan av samtliga slutnoders input rate. Behövs congestion control i detta nätverk? Varför? Behövs flow control i samma nätverk? Varför? 
Svar: 
- Congestion control behövs *inte*, eftersom summan av input rate to any queue är mindre än transmission rate så kommer köer inte bildas. Blir ej överbelastad eftersom länkkapaciteten är högre
- Flow control behövs dock fortfarande, eftersom en sändare kan överbelasta en mottagare med data. 
b) Beskriv kortfattat hur traceroute fungerar. Förklara syftet, vilka ICMP meddelanden som används steg för steg, samt logiken bakom hur dessa används.
Svar: Traceroute är ett sätt att trace paketets route från sändare till mottagare. Den använder ICMP för detta. Finns tre olika ICMP messages: Echo request, Time exceeded och destination unreachable. TTL count ökar vid varje echo request för att hitta en router (varje gång det passerar en router). t uses wrong port number to get DR from destination.

**30 - TCP/IP-modell**
a) Förklara kortfattat hur TCP/IP-modellen, som delas upp i olika skikt, fungerar. Ange en fördel och en nackdel med modellen.  
Svar: Divide and conquer! every layer has a specific purpose and passes a data unit to the next. (+) specialisation. IP is common, anything compatible with IP works with Internet. (-) overhead. every layer contributes with a header of its own. less efficient than a cross-layer approach.

b) Rita ett konceptuellt diagram som representerar Internets nätarkitektur. Se till att du visar hela hierarkin med olika aktörer från end-user till backbone. Förklara kortfattat bilden.
Svar:
**Internets konceptuella nätarkitektur**:
![[Pasted image 20230315212051.png|500]]
- **Backbone** - A high-speed network infrastructure that connects multiple LANs and other networks together to form larger network
- **Provider network** - Designed to provide network connectivity and services to customers who subscribe to the provider's services
- **Customer network** - refers to a network infrastructure that is owned and operated by an organisation or individual for their own use. 
- **NAP (Network Acces Point)** - The point from which an internet service provider (ISP)
		- **ISP** - a organisation that provides internet access to user or customers. ISPs are conneceted to the internet backbone through high-speed communication links

## Application Layer
Högsta nivån som är ansvarig för applikationer och tjänster som är tillgänglig för en användare. Detta lager gör det möjligt för användaren att kommunicera mellan program och annat som, installerade på andra datorer i nätverket. Lagret säkerställer även överföring av applikationsdata mellan datorer på ett korrekt (och effektivt) sätt. 

##### SMTP (Simple Mail Transfer Protocol)
Används för att skicka mail mellan två MTA (message transfer agent, transfers e-mails). Meddelanden skickas över TCP på port 25.

##### FTP (File Transfer Protocol)
Används när filer ska överföras mellan två datorer. Använder två parallella TCP uppkopplingar (en är kontrollmeddelanden och en för själva överflringen). Använder läsenord. Data krypterad.

##### p2p (peer to peer)
Här fungerar en användare som både klient och server. Användare hämtar data från varandra. Trafiken på accessnäten har en annan profil än i kllien/server modellen, den kan vara asymeterisk att mer trafik går ut från accessnätet än vad som kommer in. Här krävs inte MAC-adresser för att skicka data om alla datorer vet nästa hopp för varje destination.

##### HTTP (HyperText Transfer Protocol)
Används när en användare ska hämta en webbsida som finns på en annan server. Vanliga HTTP använder TCP port 80. HTTP som körs över TLS/SSH (HTTPS) använder sig av TCP port 443.
- Värddator vill hämta dokument skickar den ett HTTP Request 
- Servern svaraa med ett HTTP Response som innehåller dokumentet.

##### DNS (Domain Name System)
Convertar webaddresser till IP där IPn till DNS server är samma för nätverk (känd för alla datorer i nätet). Varje nätverk måste ha en DNS server.
![[Pasted image 20230316103117.png|300]]

##### SNMP (Simple Network Management Protocol)
A protocol for collecting and organizing information about managed devices on IP networks. Widely used for network monitoring.

##### Fjärrinloggning
För att komma åt en annan server hemifrån (t.ex skolan elr jobb). Man skapar förbindelse till en dator på ett annat nät
Säker Fjärrinloggning (och fsäker filöverföring) möjliggörs med **SSH** (secure shell), där man får en krypterad förbindelse.

###### Telnet (Terminal Network)
ISO standard för fjärrinloggning, som bygger på klient/server modellen. 
Om båda datorerna har olika OS, används Network virtual terminal (NVT) Character Set. Så användarens dator översätter lokala tecken till NVT, och fjärrdatorn översätter dom till serverns lokala tecken.


## Några fler exempeluppgifter
**31**
I en industrilokal finns ett antal temperaturgivare utplacerade i ett IoT-nät baserat på Bluetooth Low Energy (BLE). Givarna läses av med en minuts mellanrum och värdet skickas till en central server som samlar in all data. BLE-nätet är byggt enligt ett stjärnnät där servern är ansluten till centralnoden. I nätet är ramstrukturen enligt bild 2, där 
- Preamble består av en byte antingen 10101010 eller 01010101, beroende på vad första biten i adressfältet är. Om första biten är en nolla används den första varianten medan om det är en etta används den andra varianten. 
- Adressen är adressen till centralnoden. 
- PDU (Protocol Data Unit) är själva datan som skickas i ramen. Här används de två första byten som PDU header, vilket kan ses som kontrollbitar för lager 2 protokollet och alltså inte kan användas för användardata. 
-  Slutligen används en 24-bitars CRC. 
För att datan ska kunna sorteras in rätt i databasen i centralnoden behöver, förutom själva värdet som består av tre bytes, även givarens identitet (8 bytre) och en tidsstämpel (6 byte) skickas med, se bild 3. 
![[Pasted image 20230316182730.png|450]]

a) I det nuvarande systemet räcker batterierna i en temperaturgivare ungefär ett år. Man har kommit fram till att energiförbrukningen kan anses proportionell mot tiden som sändaren är igång. I ett försök att förlänga batteritiden ska man låta givaren samla in tio värden efter varandra innan alla tio skickas i en ram. Det innebär att ramen blir större men att den bara behöver skickas var tionde minut. I bild 4 visas den datastruktur som ska användas. Det startar med att givar-id (Device id) och den första tidsstämpeln läggs in. Efter det kommer de tio värdena, med var sitt löpnummer som upptar en byte var. Uppskatta hur länge batterierna kommer att vara med den nya ramstrukturen. (I beräkningarna kan du bortse från start- och stopptid av förstärkaren. Du kan också anta att sannolikheten för kollision eller fel på länken är försumbart liten.) 
*Svar:* Det nuvarande systemet använder 19B PDU (header 2B + device id 8B + date/time 6B + data 3B) för att skicka ett värde. Då blir den totala ramstorleken 27B, som skickas varje minut. Däremot använder det föreslagna systemet 56B PDU (header 2B + device id 8B + date/time 6B + sequence no (10 * 1B) + data (10 * 3B)) för att skicka tio värden med en gång. I detta fall blir den totala ramstorleken 64B, som skickas var tionde minut. Jämför 27B/min (som räcker 1 år) med 64B/10min, så blir det 4,21 år med det nya systemet. Nackdelen är att uppdateringen av temperaturvärden sker med större mellanrum.

b) Med motsvarande struktur som i a-uppgiften, hur många data kan skickas i samma ram, och vad skulle det innebära för den maximala batteritiden?
*Svar:* Max PDU är 257B. Minus header 2B, device id 8B, date/time 6B, så är max 241B kvar till (sequence no 1B + data 3B) * x. Dvs man kan stoppa in max $[241/4]$ = 60 värden i en ram. Då blir storleken på hela PDU 4B * 60 + 16B = 256B och den totala ramstorleken 264B. Dock man skickar en ram varje timme istället. Jämför 27B/min (som räcker 1 år) med 264B/60min, så blir det 6,14 år om man använder den maximala ramstorleken. Nackdelen är förstås att uppdateringen av temperaturvärden sker med ännu större mellanrum. Man får alltså optimera systemet utgående ifrån applikationens behov.

**Extra**
Beskriv vad som menas med 
a) TDMA, Time Division Multiple Access (Alternativt: Time Division Multiplex). 
Svar: En teknik för att dela upp en tillgänglig bandbredd i tidssegment och tilldela varje anslutning en specifik tidslucka i varje cykel. Anslutningarna kan använda sin tilldelade tidslucka för att överföra data under tiden de är aktiva.
b) FDMA, Frequency Division Multiple Access. 
Svar: En teknik för att dela upp en tillgänglig bandbredd i frekvensband och tilldela varje anslutning en specifik frekvenskanal. Anslutningarna kan använda sin tilldelade frekvenskanal för att överföra data.
c) OFDMA, Orthogonal Frequency Division Multiple Access. 
Svar: En teknik som liknar FDMA, men istället för att tilldela hela frekvenskanaler delas varje frekvenskanal upp i mindre subbärvågor som kan tilldelas olika anslutningar. OFDMA används i många moderna trådlösa kommunikationssystem, inklusive 4G och 5G-nätverk.
d) TDD, Time Division Duplex. 
Svar: En teknik för att använda samma frekvensband för både upplänk och nedlänk genom att dela upp tiden i perioder för varje riktning. Anslutningar kan överföra data antingen i upplänk- eller nedlänkperioder.
e) FDD, Frequency Division Duplex.
Svar: FDD (Frequency Division Duplex) är en teknik för att använda separata frekvensband för upplänk och nedlänk så att data kan överföras samtidigt i båda riktningarna.