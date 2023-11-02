---
tags: [komsys]
---
# Stop-and-wait ARQ
- ARQ - automatic-repeat-request

- När ett paket skickas, måste sändaren få en bekräftelse för detta paket innan den kan skicka nästa. Alltså vänta på ACK.
- Nackdel är att endast ett [[datapaket|paket]] kan skickas åt gången.

## Normal operation
![[Pasted image 20230124115840.png|400]]

## Frame lost
![[Pasted image 20230124115910.png]]

## ACK lost
![[Pasted image 20230124115927.png]]