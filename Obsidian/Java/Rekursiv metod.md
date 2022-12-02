## Rekursiv metod:
En rekursiv metod måste ha:
- [[Parameter|parametrar]] 
- [[Basfall]]
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

#prog 