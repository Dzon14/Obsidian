---
tags: [komsys]
aliases: [link layer protocols]
---
# Länkprotokoll
Används för att [[applikationsprotokoll]] inte ska behöva veta vilket slags länk som används i dataöverföringen. Länkprotokollet tar emot data från applikationen och ser till att denna kommer fram korrekt till mottagaren.

Här brukar termen [[datapaket|ram]] användas istället för [[datapaket|paket]].

Först är det en startflagga som säger att en ny ram startar och i vissa [[protokoll]] är det även en slutflagga. Flaggan består av ett antal bitar som sändare och mottagare kommit överrens om, dessa får ej finnas innanför flaggorna.

The flag/SFD(Start Frame Delimiter) is to provide a unique and reliable way for the receiver to identify the beginning of a new frame of data in the incoming signal. The SFD is a known sequence of symbols or bits that is transmitted immediately after the preamble/Head.

Head/preamble: We use preamble/head, which is a sequence of bits/symbols, to synchronize the receiver to the incomnig pulse train. The preamble contain information for the corresponding protocol. When the reciever detects the preamble from the transmitter, it can align its clock to the same as the timing of the pulse.

-  $\text{Physical layer } \rightarrow \text{ bitstream }$
- $\text{ Link layer } \rightarrow \text{ frames }$
![[Pasted image 20230123152454.png|600]]
- adressera både mottagare och sändare
- If the data has same pattern as flag we have a problem
Solution: [[bit stuffing]]

De flesta länkprotokoll har [[feldetektering]] och [[felhantering|felhantering]].