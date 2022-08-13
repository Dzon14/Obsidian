# TreeMap
En typ av datatypen [[Map]]

- Implementerar en map (nyckel-värde tabell). Nycklarna är unika.
- Balanserat binärt sökträd (röd-svarta-träd)
- [[Tidskomplexitet]] för sökning, insättning och borttagning är O(log(n))

I en TreeMap är det nyckelklassen som ska implementera Comparable(om man inte använder konstruktorn med parameter av Comparator)

**Map.Entry** är ett inre interface som är nästlat i interfacet Map. 
```java
//Representerar ett nyckel-värdepar
public interface Entry<K,V> {
	K getKey();
	V getValue();
	V setValue(); //Ändrar värdet till V och returnar det gamla värdet
}
```
- Operatinen entrySet returnera en mängd (set) av Entry-objekt.
		- dvs objekt av en klass som implementerar interfacet Map.Entry


![[Pasted image 20211120141513.png|200]]
#prog 