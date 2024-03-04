---
tags:
  - affärsanalys
---
# Analystekniker 

## Conjointanalys

#### Produkt: attribut och alternativ
![[Pasted image 20240202133101.png|550]]

##### Val av attribut och alternativ
- Hur ska produkten definieras eller beskrivas? Ur vilket perspektiv?
	- Produktutveckling - teknisk eller image
- Attribut = vilka egenskaper är relevanta? 
	- användbar (actionable) 
	- ortogonal (oberoende; förutom pris) 
- Alternativ = vilka nivåer är intressanta? 
	- täckning; variation; funktion 
- Kvalitativa undersökningar vid val av attribut & alternativ 
	- (grupp diskussion, djup intervju, mm) 
	- kan användas för att få inputs till lista över attribut och alternativ

#### Vad är conjointanalys?
En statistisk metod som används för att kvantifiera hur konsumenterna värderar egenskaper (attribut/alternativ) som utgör eller beskriver en viss produkt. 
**Syfte:** räkna fram ett nyttovärde för varje alternativ. Dessa nyttovärden återspeglar respondenternas preferenser.
- CONJOINT står för CONsider JOINTly
- Utvärdering av produktkombinationer

#### Conjoint scenario
![[Pasted image 20240202133934.png|500]]

#### Exempel - läkemedelsprodukt
![[Pasted image 20240202134058.png|400]]
**Output: Nyttovärden:**
![[Pasted image 20240202134116.png|500]]
**Output: nyttovärden & viktighetsgrader:**
![[Pasted image 20240202134219.png|500]]
**Simulering av selekterade produktkombinationer: preferensandel**
![[Pasted image 20240202134454.png|500]]

##### Ytterligare exemplem
**Choice-based conjoint (CBC)/ACBC:**
![[Pasted image 20240202134710.png|400]]
**Menu-based conjoint (MBC)**:
![[Pasted image 20240202134734.png|500]]
![[Pasted image 20240202134822.png|550]]

## Multidimensional scaling (MDS)
Respondenternas uppfattning om de olika produkterna omvandlas till en grafisk representation av produkter där avstånden mellan punkterna indikerar likheter mellan dessa produkter .
Uppfattningar av produkterna $\Rightarrow$ Grafisk representation av produkterna
![[Pasted image 20240202134951.png|500]]
![[Pasted image 20240202135742.png|500]]
##### MDS Direct approach
![[Pasted image 20240202140052.png|500]]
##### MDS derived approach
![[Pasted image 20240202140131.png|500]]
![[Pasted image 20240202140159.png|500]]
##### Preference data
- Rangordning efter preferens
![[Pasted image 20240202140238.png|500]]

##### SPSS ALSCAL
- Alternative Least Squares approach to scaling
![[Pasted image 20240202140554.png|400]]
![[Pasted image 20240202140609.png|500]]

#### MDS procedures
**MDS Procedures:**
- Nonmetric MDS
	- Ordinal dataskala
- Metric MDS
	- Minst interval dataskala
**Analysnivå:**
- Individnivå
- Aggregerad nivå

## Korrespondensanalys
En multivariat statistisk metod som används för att transformera en korstabell till en låg-dimensionell representation (oftast en 2-dim graf av raderna och kolumnerna)
- Korstabell $\Rightarrow$ 2-dim bild

![[Pasted image 20240202141048.png|500]]

#### Korrespondensanalysis - multiple frequencies
![[Pasted image 20240202141223.png|500]]
**Input:**
![[Pasted image 20240202141254.png|500]]
**Output:**
![[Pasted image 20240202141329.png|500]]
![[Pasted image 20240202141347.png|500]]

## Attributspositioneringsanalys (AP)
**Marknadsundersökning:** varumärke och attribut
![[Pasted image 20240205141722.png|500]]
**Syfte:** utvärdera dessa attribut; prioriteringsstruktur; förbättringsmöjligheter

![[Pasted image 20240205142242.png|500]]
![[Pasted image 20240205142318.png|500]]

- Används för att identifiera problem och förbättringsmöjligheter genom att positionera attributen i ett 2-dim diagram.
- AP-analysen är till största del en grafisk presentation av variabler eller egenskaper på basis av viktighets- och tillfredsställelsegrad. 
- **Viktighetsgrad** = ett index som indikerar respondenternas bedömning på attributens viktighet vid valet/inköp av produkt/service 
- **Tillfredsställelsegrad** = ett index som indikerar hur nöjda respondenterna är

#### Diagram
- Ett tvådimensionellt diagram skapas där x- och y axeln är tillfredsställelse- respektive viktighetsgrad. 
- Skärningspunkten är medianen. 50 % av punkterna ligger under medianen 50% av punkterna ligger över medianen
#### Kvadranter: klassificering av attribut på basis av tillfredsställelse- och viktighetsgrad
![[Pasted image 20240205141855.png|500]]
-  som hamnar i Major och Negative är förhållandevis **viktigare**. 
- Skillnaden mellan Major och Negative är att en större del av respondenterna säger att de är nöjda med Major än Negative variabler. 
- Major variabler är något att bibehållas medan Negative variabler är något som måste förbättras.
- Plus och Minor är de variabler som är förhållandevis ”mindre viktiga”. 
- Respondenterna ger bättre tillfredsställelsebetyg på Plus variabler än Minor variabler. 
- I kvadranten Minor hittar man de variabler som förhållandevis har låga indexvärde för både viktighet och tillfredsställelse.
**Action:**
- Major $\rightarrow$ Maintain
- Negative $\rightarrow$ Improve
- Plus $\rightarrow$ Less emphasis
- Minor $\rightarrow$ No panic
**Exempel på ett bra diagram (alla attribut i Major och Minor):**
![[Pasted image 20240205143325.png|400]]

##### Att mäta viktigthet (1) - Direkt fråga
![[Pasted image 20240205143844.png|500]]
**Tillfredsställelsegrad:**
![[Pasted image 20240205143913.png|400]]

##### Viktighets- och tillfredsställelsegrad
1) Medelvärde
2) Topp 2 box (procentsats)
3) Modifierat medelvärde (100-gradig skala)
![[Pasted image 20240205144006.png|500]]

##### Att mäta viktighet (2): Indirekt mått - korrelation mellan attribut och referensvariabel
![[Pasted image 20240205144111.png|550]]

**Korrelationskoefficient**
- Parametrisk:
	- Intervall- eller kvotskala $\Rightarrow$ Pearsons koefficient
- Icke-parametrisk:
	- Ordinal $\Rightarrow$ Spearman rangkorrelationskoefficient; Kendall tau-koefficient
	- Nominal $\Rightarrow$ Cramer koefficient
**Viktighetsgrad**
- Koefficienten används som viktighetsgrad, eller sambandskoefficient X 100
**Tillfredsställelsegrad:**
Samma som Viktighetsgrad (1) - direkt fråga. 

##### Modifierat medelvärdeindex
- Transformering av skala till index 5-gradig skala 
	- (1=-10) (2=-8) (3=1) (4=6) (5=10) 
- Medelvärde på transformerade siffror används

## Van Westendorp-metoden / Priskänslighetsmätare

#### Grundläggande teknik
Priskänslighetsmätning (PSM) består av fyra grundläggande frågor som besvaras av respondenter (ställs efter beskrivningen på produkten): 
1) Vid vilket pris börjar du uppfatta produkten som BILLIG? 
2) Vid vilket pris börjar du uppfatta produkten som DYR? 
3) Vid vilket pris börjar du uppfatta produkten som FÖR DYR – dvs. så dyr att du aldrig själv skulle överväga att köpa den? 
4) Vid vilket pris börjar du uppfatta produkten som FÖR BILLIG – dvs. så billig att du skulle tänka att ”till detta pris kan kvaliteten inte vara bra”?

#### Analys och definitioner
De fyra frågorna ger fyra **kumulativa** fördelningar. 

Likgiltig prispunkt eller **Likgiltighetspris**: priset vid skärningspunkten mellan kumulativa fördelningar av BILLIGT och DYRT (eller EJ BILLIGT och EJ DYRT) 

Optimal prispunkt eller **Optimumpris**: priset vid skärningspunkten mellan kumulativa fördelningar av FÖR BILLIGT och FÖR DYRT. 

**Räckvidd för acceptabla priser**: Marginell billighetspunkt = skärningspunkt för kumulativa fördelningar mellan FÖR BILLIGT och EJ BILLIGT Marginell dyrhetspunkt= skärningspunkt för kumulativa fördelningar mellan FÖR DYRT och EJ DYRT

**Figur 1: Likgiltihetspris, optimumpris och acceptabelt prisintervall (Produkt X)**
![[Pasted image 20240205145838.png]]

## TURF-analys
TURF - Total Unduplicated Reach and Frequency
Ett enkelt statistiskt verktyg utvecklat för att maximera antalet potentiella kunder baserat på ett urval av ett begränsat antal produkter.

**Används för:**
1) Beräkna inkrementella värden för produkterna i sortimentet 
2) Fastställa det optimala produktutbudet 
3) Attrahera många konsumenter med få produkter 
4) Maximera "täckning" samtidigt minimera reklamkostnader (val av mediekanaler)
##### Fryst färdigmat
![[Pasted image 20240205150414.png|550]]

##### Iterativa frekvensfördelningar
![[Pasted image 20240205150531.png|550]]
**Resultaten för Turfmodellen blir:**
![[Pasted image 20240205150637.png|300]]

#### Line Optimization - Optimal number of items
![[Pasted image 20240205150908.png|550]]
![[Pasted image 20240205151021.png]]
