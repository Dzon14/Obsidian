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
- Tillåter inte fragmentering hos rounter, men har fragmenteringsmekanism själv. Den fragmenterar automatiskt. Om en väg inte klarar längden får paketet kastas, drf måste sändaren veta hur paketet ska skickas genom nätet.
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


