---
tags: [prog]
---
# Fibonaccitalen
## Rekursivt (dålig lösning):
```java
public static long fib(int n) {
	if (n <= 1) {
		return n;
	} else {
		return fib(n-1) + fib(n-2);
	}
}
```
Detta är ett ineffektivt sätt att beräkna på. 
Det kommer bli en exponentiell [[Tidskomplexitet]], alltså $O(2^n)$

## iterativt
I detta fall blir en **iterativ lösning** smidigare, och kommer ge en linjär [[Tidskomplexitet]]:
```java
public static long fib(int n) {
	if(n <= 1) {
	return n;
	} else {
		long nbr1 = 0;
		long nbr2 = 1;
		long res = 0;
		for (int i = 2; i <= n; i++) {
			res = nbr1 + nbr2;
			nbr1 = nbr2;
			nbr2 = res;
		}
		return res;
	}
}
```

## Problemet kan dock lösas rekursivt genom [[Dynamisk programmering]]

En vektor där -1 betyder att resultat ej beräknats används (-1 eftersom fibonacci börjar på 0):
```java
public static long fib(int n) {
	long[] table = new long[n + 1]; //skapa en tabell
	Arrays.fill(table, -1);
	return fib(n, table);
}
//glöm ej long[] table, enkelt fel på tenta
private static long fib(int n, long[] table) {}
	if (table[n] == -1) {
		if (n <= 1) {
			table[n] = n;
		} else {
			table[n] = fib(n - 1, table) + fib(n - 2, table);
		}
	}
	return table[n];
}
```
Detta har linjär [[Tidskomplexitet]]

