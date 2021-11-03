---
aliases: [rekursivt]
---
# Rekursion #prog 
Att tänka rekursivt: "Jag fyller ett år mer än förra året"
[[metoder]] som anropar sig själva.
Det går att definiera många [[Datastruktur|datastrukturer]] rekursivt, t.ex: [[Lista|listor]] och [[träd]].

### Ex: Rekursiv beräkning av n! ($n! = n \cdot (n-1)!$)
```java
public static long factorial (int n) {
	if (n == 0) {
		return 1; //basfall
	} else {
		return n * factorial(n-1); //rekursivt anrop
		}
}
```

### [[Exekvering]] och [[metodanrop]]:
![[Pasted image 20211102103234.png | 500]]

## Rekursiv metod:
En rekursiv metod måste ha:
- [[Parameter|parametrar]] 
- [[basfall]]
- rekursiva anrop

### Exempel: Beräkna potenser
```java
public static double power(double x, int n) {
	if (n == 0) {
		return 1;
	} else {
		return x * power(x, n-1);	
	}
}
```

### Exempel: Skriv ut ett tal baklänges
```java
public static void reverse(int n) {
	if (n < 10) { //kan även kolla negativa tal, dvs throw new IllegalArgumentException("Argument < 0")
		System.out.print(n);
	} else {
		System.out.print(n % 10);
		reverse(n / 10);
	}
}
```


## Rekursion och listor
Här blir [[Basfall|basfallet]] om [[Lista|listan]] är tom, dvs $n == 0$ och listan består sedan av ett första [[element]] följt av en lista med $n-1$ element.
![[Pasted image 20211102105830.png | 300]]

### Skriv ut elementen i en lista i omvänd ordning
```java 
public void printReverse() {
	printReverse(first); //skriver ut första 
}

private void printReverse(ListNode<E> p) {
	 if (p != null) { //basfall
	 	printReverse(p.next); //resten av listan förutom första
		System.out.println(p.element);
	 }
}
```
Man kan tänka att man första följer metoder nedåt, för att sedan gå upp igen i motsatt ordning för att skriva ut allting (gäller generellt alla rekursiva uppgifter med flera metoder)
