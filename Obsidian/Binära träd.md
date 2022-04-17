---
aliases: [binära träden, binära trädet, binärt träd]
---
# Binära träd 
Binär träd är en [[Datastruktur]] och ett [[träd]] där varje nod har max två "barn". Går uppifrån ner. 
![[Pasted image 20211112140426.png]] 

## Terminologi
I datavetenskap ritas träden upp och ned, dvs roten överst.
- **Rot** - den enda nod som saknar förälder
- **Löv** - noder som saknar barn
- **Gren** - en serie noder förbundna med varandra. 

#### [[Rekursion|Rekursiv]] definition 
- Ett binärt träd är antingen tomt eller består av roten 0, 1 eller 2 subträd	

## Implementering av binära träd
```java
public class BinaryTree<E> {
	private Node<E> root;
	private int size;
	
	public BinaryTree() {
		root = null:
	}

	private static class Node<E> {
		private E data;
		private Node<E> left;
		private Node<E> right;
		
		private Node(E data) {
			this.data = data;
			left = right = null:
		}
	}
}
```

## Rekursiva traverseringar av binära träd
Ordning noder skrivs ut beror på var vi placerar utskriftssatsen i förhållande till de rekursiva anropen:
- **Preorder** - roten, vänster subträd, höger subträd
- **Inorder** - vänster subträd, roten, höger subträd
- **Postorder** - vänster subträd, höger subträd, roten

## Skriv ut alla noder (Traversering)
- Antag att vi ska besöka alla noderna i träder, t.ex. för att skriva ut innehåller i träder.
### Preoder
- Vi kan börja med att besöka ut roten, sedan vänster subträd, sedan höger subträd
```java
public void print() {
	print(root);
}

private void print(Node<E> m) {
	if (n != null) {
	System.out.println(n.data);
	print(n.left)
	print(n.right);
	}
}
```

### inorder
```java
public void print() {
	print(root);
}

private void print(Node<E> n) {
	if (n != null) {
		print(n.left);
		System.out.println(n.data);
		print(n.right);
	}
}
```

### postorder
```java
public void print() {
	print(root);
}

private void print(Node<E> n) {
	if (n != null) {
		print(n.left);
		print(n.right);
		System.out.println(n.data);
	}
}
``` 

#prog 