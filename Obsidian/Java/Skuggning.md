---
aliases: [skugga, skuggas, overriding, override]
---
# Skuggning
- **Skuggning** (eng. overriding) betyder att vi skriver om en metod som klassen ärvt så att den får ett nytt beteende.
## Skugga equals
```java
public boolean equals(Object obj) {
	if (obj instanceOf Person) {
		return id == ((Person) obj).id;
	} else {
		return false;
	}
}
```

## Skugga HashCode

- Måste göras i klasser som implementerar metod som använder HashCode. 

## Exempel
![[Pasted image 20220814142116.png]]
#prog 