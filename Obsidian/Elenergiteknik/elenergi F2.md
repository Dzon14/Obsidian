# Elenergi F2 - Synkronmaskinen
- En elmaskin är både generator och motor
- Den mest grundläggande av roterande elektriska maskiner.

#### Repetition
**Strömförande ledare i magnetfält - kraft**
- Strömmen i en ledare med längd l ger upphov till en kraft $\vec{F} = q \vec{v} \times \vec{B}$
- Rörelsen är vinkelrät mot fältet: $F=qvB = q \frac{l}{t} B = \frac{q}{t} lB = ilB$
			- HHR: F-i-B
![[Pasted image 20230117082903.png|200]]
- När en ledare med längd l i ett magnetfält B leder strömmen i, påverkas ledaren av en kraft $F = Bil$ 
**Rörlig ledare i magnetfält: Induktion**
- Genom ledaren har vi flödet $\Phi = BA = Bxl$.
- När ledaren rör sig induceras: $\lvert e \rvert = \frac{d \Phi}{dt}=B \frac{dx}{dt}l = Bvl$
			- elektromotorisk kraft
			- HHR: e-v-B
- Elektromotorisk kraft emk är derivatan av flödet

## Nodes
- [[synkronmaskin]]
- [[tomgång]]
- [[Poltal]]
- [[torque|vridmoment]]

## Sammanfattning
1. En synkronmaskin har en roterande magnetiserad **rotor** i en **stator** med lindningar 
2. Roterande fält i lindningar riktade 0, 120, 240° ger **trefasspänningar** med fas 0, -120, -240° 
3. Trefasiga sinusströmmar summeras till **noll** så återledare **behövs inte** 
4. Roterande **vektorer** kan representera flöde, spänningar och strömmar i trefasmaskin 
5. Momentet på axeln i en trefas synkrongenerator är **konstant**, oberoende av $\theta$ 
6. Synkrongeneratorns ekvivalenta schema i en fas: AC-källa $E_{m}$, reaktans $X_{ar}$, $E_{i} = E_{m}-jX_{ar}I_{a}$
7. Lastvinkeln d är både en **elektrisk** vinkel $\angle E_{m} - \angle E_{i}$ och en **mekanisk** vinkel $\angle \Phi_{m} - \angle \Phi_{res}$ 
8. Vridmoment $T \propto sin \delta$ Tre driftfall: $\delta > 0$ **generatordrift**, $\delta = 0$ **tomgång**, $\delta < 0$ **motordrift** 
9. Vinkelhastighet på rotor och spänning är kopplade via antal polpar p: $\omega_{el} = \left(\frac{p}{2}\right)\omega_{mek}$
