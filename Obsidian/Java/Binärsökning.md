---
tags: [prog]
---
# Binärsökning 
Funkar endast om vektorn är sorterad. 
En teknik för att söka efter ett riktat värde eller t.ex en [[nyckel]] i en [[samling]]. 
- O(logn) i värsta fall

[[Algoritm]] för att söka efter ett element x i en vektor (sorterad i växande ordning):
Basfall:
- 0 element. Sökt element finns ej
- Jämför x med mittelement i vektorn. Om likhet, avbryt. 
Rekursiva steget:
- Om x är mindre än mittelementet, fortsätt sökningen i vänster halva av vektorn. 
- Om större, sök i höger halvan av vektorn. 

```java
public static int indexOf(int[] a, int x) {
	return binarySearch(a, x, 0, a.length - 1);
}

private static int binarySearch(int[] a, int x, int first, int last) {
	if (first > last) {
		return -1; //avslutar
	} else {
		int mid = first + ((last - first) / 2);
		if (x == a[mid]) {
			return mid;
		} else if (x < a[mid]) {
			return binarySearch(a, x, mid - 1, last);
		} else {
			return binarySearch(a, x, mid + 1, last);
		}
	}
}
```

För en generell metod:
Låt metoden vara [[generisk]] och deklarera en [[typparameter]]:
public static < E> int indefOf ( E[ ] a, E x ).
Använd [[generisk metod]]

## Generisk metod för binärsökning
- Använd comparable eller comparator (se [[jämföra objekt]]).

#### Med comparable (compareTo)
![[Pasted image 20230809171823.png]]
- Vi förutsätter att klassen som ersätter E implementerar Comparable. Dvs. om en vektor av typen Person ska sorteras måste klassen Person implementera Comparable. 
- Inuti metoden binarySearch måste vi använda typkonvertering vid anrop av compareTo: int compResult = ((Comparable) x).compareTo(a[mid]);
- Om man iställer kräver att klassen som ersätter E implementerar Comparable, alltså < E implements Comparable< E>> int indexOf(...).. så slipper vi typkonvertera. 
![[Pasted image 20231231124419.png|500]]
## Med comparator (compare)
![[Pasted image 20230809172028.png]]
![[Pasted image 20231231125302.png]]