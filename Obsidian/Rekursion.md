---
aliases: [rekursivt, rekursiv]
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

Se även:
[[Rekursiv metod]]
[[Rekursion och listor]]
[[Divide and conquer]]
[[Fibonaccitalen]]

## När ska rekursion användas?
Många exemplen (t.ex n!) kan lösas icke-rekursivt. Ibland leder även rekursion till ineffektiva algoritmer.
Det ska användas när:
- Svårt att uttrycka lösningen icke-rekursivt
- Finns en icke-rekursiv lösning men den rekursiva är effektivare. (t.ex sortering)
- När en rekursiv lösning är enklare att förstå, implementera osvosv. (t.ex binärsökning)

#prog 

