---
tags: [prog]
---
# Jämföra objekt


## Equals
För ett objekt kan man ej använda equals, då denna refererar till två olika objekt, precis som att använda "= =". Det man istället kan göra är att skugga (override) equalsmetoden i superklass Object - att skriva om den.
"= =" jämför referenser och kollar om det jämförs till samma objekt. 
- Man måste ha Object som parameter eftersom den annars ej kommer skuggas och Objects egen equalsmetod kommer användas. Sen får man typomvandla parametern till objektet man faktiskt vill jämföra (t.ex: ((Person) obj).id)
- Använd @Override
- Vi behöver använda "instanceof" för att returnera fel om argumentet har fel typ. 
En färdig metod kan se ut enligt: 
![[Pasted image 20230809120030.png|500]]
- Uttrycket obj instanceof Person returnerar true om obj:s typ är Person eller någon subklass till Person.
- Uttrycket obj instanceof Person returnerar false om obj har värdet null.
Förenklad version med Java 16:
![[Pasted image 20230809120404.png|450]]

- Note: När man skuggar equals bör man också skugga hashcode, vilket används för [[Hashtabeller|hashtabell]]: public int hashCode() { return id; }
- Man kan även skugga toString: public String toString() { return name + " " + id; }

## Comparable - compareTo
- Kräver att man implementerar interfacet Comparable. Används för att exempelvis sortera en Array med Person-objekt. Utan denna implementering genereras ClassCastException.
- klassnamn implements comparable< Person>
- I compareTo bestämmer man hur elementen ska jämföras (större, lika, mindre).
![[Pasted image 20230809134425.png|500]]
- Note: Om man exempelvis jämföra om namn är samma kan man i den klassen sätta if(p1.compareTo(p2) == 0) ...

## Comparator - compare
- När man vill jämföra objekt på olika sätt eller om klassen redan implementerar comparable och compareTo används på ett annat sätt.
- Klassnamn implements comparator< Person>
- Kan implementeras på olika sätt beroende på vad man vill jämföra:
![[Pasted image 20230809134921.png]]
- Här används compareTo i klassen string. 
- Vill man sortera än vektor kan man använda Arrays.sort(persons, new klassnamn());
- Man kan använda [[Lambdauttryck]] för smidigheten. 
- Om man ska jämföra stora tal som kan ha olika tecken bör man istället för lambda, jämföra dem med:
```java
Integer.compare(p2.getId(), p1.getID());
```
För att undvika overflow. 