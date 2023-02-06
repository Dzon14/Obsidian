# Trefas

## Synkrongeneratorn tre växelspänningskällor
![[Pasted image 20230119082502.png]]

- Vid symmetri räcker det att studera en y-fas
		- Ge övriga fasers ström och spänning samma amplitud
		- Försjkut övriga fasers fasläge $-120 \degree$ respektive $-240 \degree$
		- Trefas effekt = 3 x enfaseffekt

## [[Y-koppling och deltakoppling]]
![[Pasted image 20230119082810.png]]

## Komplexa storheter 
- Exempel: Symmetrisk trefasspänning - var noga med fasföljden
![[Pasted image 20230119083145.png]]
- Kallas [[phasors]] på engelska
- kan se som en rotation - **a,b,c**. (tvärtom positiv riktning som tidigare)

## Y-koppling eller stjärn-koppling
![[Pasted image 20230119083438.png|650]]
- Fasspänning $U_{f} =$ rms-spänning mellan fas och nolla
- Huvudspänning $U_{h} =$ rms-spänning mellan två faser
- Huvudspänning $U_{h} = \sqrt{3}$ Fasspänning $U_{f}$
	  - Exempel: $400 \ V = \sqrt{3} \ 230 \ V$ , $380 \ V = \sqrt{3} \ 220 \ V$
- Default-mässigt anges: Effektivvärde, huvudspänning

## Symmetri: Trefasströmmars summa = 0
![[Pasted image 20230119083919.png]]
- Symmteri $\Rightarrow$ Ingen ström i nolledaren
- Nolledare/återledare behövs ej
		- Kraftledningar har bara tre ledare
		- Tre faser minimum för att uppnå detta

## Trefaseffekt
- Symmetri: Trefaseffekt = 3 x enfaseffekt
		- Skenbar trefaseffekt $$S = 3U_{f}I = \sqrt{3}U_{h}I = \lvert \bar{S} \rvert$$
		- Komplex trefaseffekt $\bar{S} = 3 \bar{U}_{f}\bar{I}^{*}$
		- Spänning i trefassystem anges normalt med huvudspänning $\Rightarrow \sqrt{3}U_{h}...$ standard även om $3U_{f}...$ enklare att förstå:
$$\begin{align} P = Scos \varphi = ... = 3R_{s}I^{2} \\ Q = Ssin \varphi = ... = 3X_{s}I^{2} \end{align}$$

Exempel på en beräkning i kursen som man kan få fel på:
$$3 \frac{U_{f}^{2}}{R}=\frac{(\sqrt{3}U_{f})^{2}}{R}= \frac{U_{h}^{2}}{R}$$Se även härledning av uttrycken för P och Q ovan:![[Pasted image 20230119084518.png|500]]


## $p(t) = u(t) i_{R}(t)$ för trefas
![[Pasted image 20230119103039.png|400]]
- Med $p_{R}(t)= u_{fas}(t) i_{R}(t)$ fås $p_{R1}(t) + p_{R2}(t) + p_{R3}= Konstant = 3P_{1}$ 
$\rightarrow$ Konstant moment i trefas växelströmsmaskin (SM och AM)
- Definition: Aktiv trefaseffekt = $3P_{1}$, vilket verkar självklart

## $p(t) = u(t)i_{L}(t)$ för trefas
- Med $p_L(t)=u_{fas}(t)i_L (t)$ blir $p_{L1}(t)+p_{L2}(t) + p_{L3}(t) = 0$
- Definition: Reaktiv trefaseffekt = $3Q_{1}$ (analogt med P, men $P_{1}$ är medelvärde och $Q_{1}$ toppvärde)

## Enfaslast ger osymmetri
![[Pasted image 20230119084928.png]]
Ansluts mellan fas och nolla
	- All mindre hushållslast
Faserna olika belastade $\rightarrow$ ström i nolledaren