---
aliases: [generiska metoden]
---
# Generisk metod #prog 

Generiska metoder kan anropas utan att man explicit anger vad typen T är.
Om vi har en metod med [[Parameter|parametern]] (T [] a) så kan man själv välja vilket typ man vill ha.
T.ex:
```java
public class Utilities {
	public static <T> void fill(T[] a, T x) {
		for (int i = 0; i < a.length; i++) {
			a[i] = x;
		}
	}
	Integer[] nbrs = new Integer[10];
	Utilities.fill(nbrs, -1);
	
	String[] a = new String[5];
	Utilities.fill(a, "abc");
}
