# Sortering
För att göra sökning effektivare. (binärsökning exempelvis)
För att förenkla vissa algoritmer.

## Sortering i Java
Sortera vektorer:
public static sort(int[] items)
public static void sort(Object[] items)
	- Dessa jämförs med compareTo. (comparable ..)
Public static < T > void sort(T[] items, Comparator< ? super T> comp)
	- jämförs med comp.compare
	
T.ex arrays.sort(lambdauttryck)
	
## Insättningssortering (insert sort)
Sätt in element i redan sorterad följd upprepade gånger.
Långsam, kvadratisk [[Tidskomplexitet]] (O(n^2))
passar bra i speciella sammanhang och är enkla att implementera (två nästlade for-loopar)
![[Pasted image 20211202142757.png|500]]
```java
public static void sort(int[] a) {
	for (int pos = 1; pos < a.length; pos++) {
		int nextVal = a[pos]; //nästa element att sortera in
		int nextPos = pos;
		while (nextPos > 0 && nextVal < a[nextPos - 1]) {
			a[nextPos] = a[nextPos - 1];
			nextPos--;
		}
		a[nextPos] = nextVal;
	}
}

```

## Urvalssortering (selection sort)
Välj minst upprepade gånger
Långsam, kvadratisk [[Tidskomplexitet]] (både för medelfall och värsta fall)
passar bra i speciella sammanhang och är enkla att implementera (två nästlade for-loopar)
![[Pasted image 20211202142426.png|400]]

## [[Mergesort]]
Snabb metod
Sortera vänstra halvan, sen högra halvan och sedan samsortera (merge) de båda sorterade halvorna

Nedan används [[Divide and conquer]] tekniken i [[mergeSort]].
```java
public static void sort(int[] a) {
	int[] tmpArray = new int[a.length];
	mergeSort(a, 0, a.length - 1);
}

private static void mergeSort(int[] a, int first, int last) {
	if (first < last) {
		int mid = first + (last - first) / 2;
		mergeSort(a, first, mid);
		mergeSort(a, mid+1, last);
		//samsortera de båda halvorna:
		merge(a, tmpArray, first, mid + 1, last); 

	}
}

```
- Att samsortera två sorterade delvektorer av sammanlagt storlek n kostar O(n)
- På varje nivå samsorteras n element
- Antal nivåer är logn
- T(n) = O(nlogn)
- Mergesort kan göras stabil (ordning ändras ej för lika element)

## Quicksort
- Välj ut ett element (pivotelement)
- Partitionera vektorn: Flytta om elementen så att element <= pivot hamnar till vänster och element >= pivot hamnar till höger
- Upprepa [[Rekursion|rekursivt]] på de båda delvektorerna till vänster respektive till höger om pivotelement
```java
public static void sort(int[] a) {
	quickSort(a, 0, a.length - 1);
}

private static void quickSort(int[] a, int first, inte last) {
	if (first < last) {
		int pivIndex = partition(a, first, last);
		quickSort(a, first, pivIndex - 1);
		quickSort(a, pivIndex + 1, last);
	}
}
```

### Partitionering
- Sök från vänster upp ett element som är >= pivot
- Sök från höger upp ett element som är <= pivot
- Byt plats på dessa
- Fortsätt tills hela vektorn genomletats.
- Pivotelementet kan sättas in mellan de båda vektordelarna som uppstår
- Arbetet blir proportionellt mot vektorns längd
[[Tidskomplexitet]] i bästa fall är O(logn) (och medelfall)
I värsta fall blir det O($n^2$)
Quicksort behöver inget extra minnesutrymme för temporär vektor

## Quicksort vs Mergesort
Quicksort:
- Snabb i medelfall (O(nlogn)), men O(n^2) i värsta fall. 
- Behöver inget extra minnesutrymme för temporär vektor

Mergesort:
	- O(nlogn) i både medel- och värsta fall.
	- Stabil 

#prog 
	
## Stabila sorteringsalgoritmer
![[Pasted image 20220112202604.png]]


	
	