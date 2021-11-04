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

#prog 