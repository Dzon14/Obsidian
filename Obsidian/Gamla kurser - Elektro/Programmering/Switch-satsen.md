---
aliases: [switch-sats]
---

# Switch-satsen
Om man har en [[selektion]] med många alternativ kan man använda switch-satsen. Ett alternativ till att göra en mängd nästlade if-satser.
- Glöm inte att ha med en "default".
- Glöm ej break (viktigt).
## Syntax
![[Pasted image 20220625174353.png]]

## Exempel
```c
//Variabeldeklaration  
char val;            
  
// Läs in svaret  
cout << "Välj ja (j) eller nej (n): ";  
cin >> val;  
  
// Utför olika saker beroende på värdet av val  
switch(val)  
{  
  case 'j':     // Jämför med värdet av j, därav 'j'  
    cout << "Du har svarat ja" << endl;  
    break;  
  
  case 'n':  
    cout << "Du har svarat nej" << endl;  
    break;  
  
  default:  
    cout << "Du har angivit ett ogiltigt svar" << endl;  
    break;  
}
```

#prog