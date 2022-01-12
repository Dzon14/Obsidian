---
aliases: [Binära sökträden, binära sökträdet]
---
# Binära sökträd
En [[Datastruktur]] som passar för sökning.
Användbart i program med stort antal element. Binära sökträd och [[Hashtabeller]] är bättre än att t.ex söka med en sorterad vektor osv. 

Det är ett [[Binära träd|binärt träd]] där:
- Alla värden som finns i noder i vänster subträd till n är mindre än värdet som finns i n. 
- Alla värden som finns i norder i höger subträd till n är större än värdet som finns i n 
- Dubletter tillåts alltså inte

## Inordertraversering av binära sökträd 
- Genomgång av trädet i **inorder** besöker noderna i växande ordning. 
**Exempel:**
![[Pasted image 20211120130310.png|200]]'
Här är ordningen: 2, 4, 5, 6, 8, 9

## Sökning
- Börja i roten, jämför med sökt element x, om likhet är vi klara
- Om x är mindre än rotens element: gå till vänster barn annars gå till höger barn.
- Fortsätt på samma sätt tills vi hittar det sökta, eller tills den nod som står i tur att undersökas är null (misslyckad sökning)

## Insättning
- Om talet x man vill sätta in är mindre än roten, gå till vänstra grenen och sätt in vid misslyckad sökning. 
- Vid insättning ska ordningen för trädet bevaras
- Dubletter får ej förekomma

## Borttagning
- För borttagning av ett element måste vi söka upp det
- När det tas bort måste föräldern kopplas ihop med något av barnen (alltså måste man hålla reda på referens till föräldern vid sökning)
**Noll barn:**
- Börja med att söka efter noden (och föräldern)
- Noden, act, som ska bort är ett löv. Sätt den referens i parent som som refererar till act till null
**Ett barn:**
- Börja med att söka efter noden (och föräldern)
- Noden, act, som ska bort har ett barn. Sätt den referens i parent som referar till act till att referera till acts barn.
**Två barn (svårare):**
- Noden act som ska bort har två barn:
 		- Sök upp minsta noden (min) i acts högra subträd
 		- Flytta data från denna till act
 		- Tag bort min
 ![[Pasted image 20211120131916.png|450]]
 
## Binära sökträd - [[Tidskomplexitet]]
- En traversering genom alla noderna i ett träd med n noder har [[Tidskomplexitet|tidskomplexiteten]] O(n). (varje nod besöks en gång)
- Den längst grenen i träder har h noder (h är trädets höjd)
- Man kan visa att 2_log(n + 1) <= Höjden <= n
- De tre operationerna har [[Tidskomplexitet|tidskomplexiteten]] O(2_log(n)) i bästa fall och O(n) o värsta fall.

Den idealiska formen på ett binärt sökträd:
- Alla nivåer utom möjligen den högsta, har så många noder som möjligt.
- Noderna ligger alltså så nära roten som möjligt
- Då blir höjden garanterat O(2_log(n)).

![[Pasted image 20211120140826.png|500]]

För att rätta till ett träd och göra det balanserat måste man arbeta med rotationer.
En enskild rotation kostar O(1).
Om ett binärt sökträd hålls balanserata kommer sökning, insättning och borttagning därmed att kosta O(2_log(n)) i värsta fall. 

### AVL-träd - Balanserade binära träd
- Ett binärt träd är balanserat om det för varje nod i trädet gäller att höjdskillnaden mellan dess båda subträd är högst ett
- I balanserade träd är höjden <= 1.44 * 2_log(n).

## Klasserna [[TreeSet]] och [[TreeMap]]
#prog 

## Implementering av binära sökträd
```java
public class BimarySearchTree<E> {
	private Node<E> root;
	private int size;
	//Skapar tomt träd
	public BinaryTree() {
		root = null;
		size = 0:
	}
	
	private static class Node<E>
		private E data;
		private Node<E> left;
		private Node<E> right;
		
		private Node(E data) {
			this.data = data;
			left = right = null;
		}
	
	//En metod find, behöver ej vara rekursiv. Använder compareTo i interfacet Comparable (Används också i add och remove för att jämföra)
	public E find(E x) {
		return find(root, x);
	}
	
	private E find(Node<E> n, E x) {
		if (n == null) {
			return null;
		}
		//skapar compResult för att endast anropa comparable en gång, annars fel
		int compResult = ((Comparable<E>) x).compareTo(n.data); 
		if (compResult == 0) {
			return n.data; //Observera att n.data returneras och inte x ...
		} else if (compResult < 0) {
			return find(n.left, x);
		} else {
			return find(n.right, x);
		}
	}		
}
```
Man kan även använda [[interface|interfacet]] Comparator för att jämföra element i trädklassen. 
Det ger oss möjlighet att jämföra objekt av en klass på flera olika sätt. Man kan använda lambauttryck för att skapa detta. (compare-metod).
En parameter behövs då i konstruktorn. och följande deklareras i konstruktorn:
comp = (e1, e2) -> ((Comparable<E>) e1).compareTo(e2);

I private E find skrivs istället:
int compResult = comp.compare(x, n.data);

**Överkurs:** 
- ""? super E" betyder "ökänd superklass till E (inklusive E)"
- Använd istället typen Comparator< ? super E > istället för Comparator<E>






