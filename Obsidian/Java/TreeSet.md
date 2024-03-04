---
tags:
  - "#prog"
---
# TreeSet
En typ av [[interface|interfacet]] [[Set]]
Kan lite mer än en vanligt mängd som implementerar set.

- Implementerar en mängd, elementen är unika
- Balanserat binärt sökträd (röd-svarta träd)
- Tidskomplexitet för sökning, insättning och borttagning är O(log(n))

- Det finns flera konstruktorer i klassen, T.ex:
		- public TreeSet();
		- public TreeSet(Comparator < ? super E> c);
- Viktigaste metoderna:
		- add(element)
		- remove(element)
		- contains(element) - undersöker om ett element finns i mängden.

![[Pasted image 20211120141454.png|400]]

