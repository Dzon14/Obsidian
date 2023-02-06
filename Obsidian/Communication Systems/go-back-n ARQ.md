---
tags: [komsys]
---
# Go-Back-N ARQ
- Sändaren kan skicka flera paket åt gången. Varje paket ska bekräftas men sändaren behöver ej vänta på detta.
- Sändaren använder sig istället av ett **sändfönster** (sliding window) för att hålla reda på vilket paket som ska skickas och vilka som är skickade men ej bekräftade.
![[Pasted image 20230124120114.png|600]]

## Normal operation
![[Pasted image 20230124120252.png|600]]

## [[datapaket|frames]] lost
![[Pasted image 20230124120326.png]]

