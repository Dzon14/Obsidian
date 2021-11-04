# Binärsökning 
Titta här innan lab 5
Funkar endast om vektorn är sorterad. 
En teknik för att söka efter ett riktat värde eller t.ex en [[nyckel]] i en [[samling]]. 

[[Algoritm]] för att söka efter ett [[element]] x i en vektor (sorterad i växande ordning):
[[Basfall]]:
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
 
 #prog 
