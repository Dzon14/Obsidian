# Funktioner
- Används i C++, precis som i andra språk
- Görs en metod, som sedan kan anropas vid användning.

## Exempel, hypotenusa
![[Pasted image 20220626200737.png|500]]

- Glöm ej parametrar vid anrop

## Funktionsdeklaration
- I C++ läses filen uppifrån och ner. Alltså: Om funktion a anropar b, måste b vara ovanför a.
- Deklarera därför funktion (t.ex hjälpmetoder) före main. 

 **Ordningen blir:**
 1. Funktionsdeklarationer
 2. Huvudprogram (main)
 3. Funktionsdefinitioner, dvs hela hela funktionerna. Kallas även _implementation_ av funktionen.
Alt. gör som tidigare i java ...

## Referensparameter
Till skillnad från "värdeparameter" (lämnar en kopia av värdet, som gjort i java), så följer parametern in i funktionen och ändras/uppdateras.
- Det gör med ett "&" efter datatypen. T.ex:
```c
void funktion(int &tal1, int &tal2);
```
#prog 