# Inläsning och utläsning
-   **cin** är ett **fördefinierat objekt** av klassen **istream**
-   **cout** är ett **fördefinierat objekt** av klassen **ostream**


## Cin
-   **peek()**  
    tittar på nästa tecken i lagret utan att ta bort det. Precis som **get** returnerar **peek** en **int**.
-   **putback( char c )**  
    lägger tillbaka ett tecken till lagret. Detta är bra om vi upptäcker att vi inte skall ha tecknet. OBS! bara ett tecken.

## Cout
Att skriva är enklare eftersom vi har mer kontroll över vad som händer (ingen användare som kan t ex skriva helt fel saker). De största svårigheterna har vi redan sett: synkroniseringen av **cin** och **cout**:

-   Vi använder operatorn **<<** för att skriva vanliga tal eller strängar.
-   Några metoder i **ostream** kan vara bra att känna till:
    
    -   **width( int n )** - bestämmer hur många tecken nästa utskrift skall ta i anspråk.
    -   **precision( int n )** - anger antal siffror i reella tal
    -   **setf( long flag )** - sätter en flagga
    -   **unsetf( long flag )** - nollställer en flagga
    
    Det finns massor av olika flaggor, t ex **ios::fixed** som anger att vi skall skriva med fixt antal decimaler. Om denna flagga är satt betyder **precision** antal decimaler, annars antal siffror som visas.
-   Var och en av metoderna ovan motsvaras också av en manipulator (för att använda de flesta av dessa måste **<iomanip**> inkluderas):
    -   **setw( int n )**
    -   **setprecision( int n )**
    -   **setiosflags( long flag )**
    -   **resetiosflags( long flag )**

Det finns en metod **put(char c)** i **ostream** som man kan använda för skrivning av ett tecken (jämför **get(char& c)** i **istream**). Man klarar sig dock bra med **cout << c** som till skillnad från **cin >> c** kan hantera alla sorts tecken, även t ex blanka.

## Felhantering
-   **good()** - sann om inget fel inträffat (mer om detta senare)
-   **eof()** - sann om vi nått slutet av data (mer om detta senare)  
    OBS! metoden **eof** returnerar sant först _när man försökt läsa förbi filslutet_.



#prog 