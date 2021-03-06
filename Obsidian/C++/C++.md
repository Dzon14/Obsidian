

# C++

- C++ är en "extension" av C. 
- Det är ett objektorienterat språk.
- Man kommunicerar med [[Terminalen]]

Moduler:
- [[C++ tal och tecken]]
- [[C++ Datatyper]]
- [[Manipulatorer]]
- [[Formatflaggor]]
- [[Switch-satsen]]
- [[C++ funktion]]
- [[Array]]
- 

## [[Syntax]]
Snyggt att ha:
//---------------------------------------------  
// Filnamn: sum_for.cpp  
// Syfte:   Läser in ett visst antal tal.   
//          Beräknar summa och medel.  
// Indata:  Antal samt antal st heltal.  
// Utdata:  sum, dvs summan av talen, samt medel (medelvärdet).  
//  
// Programmerare: Nisse Nilsson  
// Datum: 000204  
// Version: 5.3  
//---------------------------------------------
Måste alltid innehålla:
```C
#include <iostream>      
using namespace std;
```

Kan använda endl ist för \n för radbyte.

Main-metod deklareras enligt
```c
int main() //alt. void inom parantes
```

**Utskrift:**
```c
cout << "Text som du vill skriva \n";
```
Lägg till ytterligare "<<" för fler saker, t.ex
```c
cout << "Summan= "<< sum << endl;
```

- Man kan styra utskrifter med "iomanip"

**Inskrift**
```c 
cin >> a >> b;
```
Här matas två tal in som skrivs i terminalen.

**Identifierare**
- Variabel-, konstant- eller funktionsnamn.
- Engelska a-z, siffror 0-9 och understryckstecken _ .
- Använd EJ mellanslag. 


#prog 