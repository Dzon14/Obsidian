
# Filer

Att skriva filer är betydligt enklare än att läsa. Vi öppnar en fil för skrivning genom att skapa ett objekt av klassen **ofstream**, som finns definierat i biblioteket **fstream**. Objektet **ofstream** kan vi sedan behandla precis som **cout**, bara med den skillnaden att allting kommer att skrivas till filen i stället för till skärmen. Vi kan använda **<<**-operatorn för att skriva tal och strängar precis som vanligt.

![[Pasted image 20220726193003.png|1000]]

## Lägga till i en redan existerande fil
- Ange flaggan **ios::app** vid öppning.
![[Pasted image 20220726193104.png|1000]]

## Filer som parametrar till funktioner

![[Pasted image 20220726193340.png|1000]]
![[Pasted image 20220726193413.png|1000]]

#prog 