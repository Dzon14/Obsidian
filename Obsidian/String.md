---
aliases: [strings, sträng, strängar, strängen]
---

# Datatypen string
- Massa tecken

## C++
**Operationer:**
![[Pasted image 20220725193316.png|500]]

### Inläsning
För att få med ord efter mellanslag etc skriver man getline(cin, namn), ist för cin >> namn.
T.ex
```c
#include <string>  
#include <iostream>  
using namespace std;  
  
int main()  
{  
  string namn;  
  
  cout << "Ge namn: ";  
  getline(cin, namn);  
  cout << namn << endl;  
  
  return 0;  
}
```
Vid blandad inläsning (när man har både tal och strängar t.ex) kan man skriva enligt 
```c
#include <iostream>  
#include <string>  
using namespace std;  
  
int main()  
{  
  string ord1, ord2;  
  int tal;  
  
  cout << "Ge tal: ";  
  cin >> tal;  
  cin.get();  
  cout << "Skriv något: ";  
  getline( cin, ord1 );  
  cout << "Skriv något igen: ";  
  getline( cin, ord2 );  
  cout << endl << "Tal= " << tal   
       << " Ord1= " << ord1   
       << " Ord2= " << ord2 << endl;  
  
  return 0;  
}
```