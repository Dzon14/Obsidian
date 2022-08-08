# Pekare
-   En pekare är en adress till en minnescell.
-   Datatypen är **inte** ett vanligt heltal, utan en **egen datatyp** som är beroende av vad den pekar på.
-   En pekare är inte samma sak som en minnescell.
-   Man kan deklarera en pekare, men den är oanvändbar tills man har satt den att peka på något.
-   När en pekare pekar på något, kan man använda den unära (till skillnad från multiplikationsoperatorn) *-operatorn för att hämta ut innehållet.  
    Exempel: tilldela värdet 6 till det som pekaren **myptr** pekar på skrivs på detta vis: ***myptr = 6;**
-   För att sätta en pekare att peka på något, kan man använda **&** -operatorn (också kallad **adressoperatorn**). Blanda inte ihop denna operator med **referensoperatorn** som ser likadan ut.

```c++
int myint;       // En int-cell allokeras, och   
                 // "myint" associeras med adressen.   
int *myptr;      // En pekare till int deklareras.  
                 // Den pekar inte på något.  
myptr = &myint;  // "myptr" pekar på variabeln "myint".   
myint = 5;       // Vi fyller cellen med värdet 5.   
*myptr = 6;      // Vi fyller cellen med värdet 6. 
cout << myint;   // Utskriften blir '6', inte '5'.  
cout << myptr;   // Adressen till cellen skrivs ut   
                 // (jämför förra exemplet).   
cout << *myptr;  // Innehållet i cellen skrivs ut,   
                 // dvs '6'.
```


## Pekare måste initieras
![[Pasted image 20220807124934.png|]]


## Pekare som pekar på ingenting (null-pekaren)
Helst bör alltså pekare sättas att peka på något redan när de deklareras. Kan man inte göra detta _ska_ de ges värdet 0:

```c++
int *ipekaren = 0; 
double *dpekare = 0;
```


![[Pasted image 20220807125111.png|700]]


![[Pasted image 20220807125211.png|700]]

![[Pasted image 20220807125256.png]]
#prog 