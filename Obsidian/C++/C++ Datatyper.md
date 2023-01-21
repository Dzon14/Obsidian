# Datatyper
- char
- signed char, unsigned char (positiv)
- int, unsigned int
- short int, unsigned short int
- long int, unsigned long int
- float
- double, long double
- bool

Notera att man kan instansiera "Konstanter" som ej får ändras under programmets gång. Enligt
```c
const double PI = 3.1415;
```

Oftast gäller:
![[Pasted image 20220623220137.png]]
- Unsigned char 0-255
- signed char -128-127
- Operatorn "sizeof" ger strlk på någonting, t.ex "sizedof(int)" ger storleken på en int. 

## Typkonvertering
Ändrar datatyp.
![[Pasted image 20220623220537.png|1000]]

## Avrundningar
![[Pasted image 20220623220713.png]]

#prog 