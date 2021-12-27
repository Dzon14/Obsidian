# Arv
- superklass, subklass
- Abstrakta klasser och metoder 
- dynamisk bindning

En klass kan bara ärva från EN klass

Shape är superklassen och innehåller gemensamma attribut och metoder. Dessa ärvs av subklasserna.
![[Pasted image 20211222141921.png|500]]

subklasserna måste kalla på superklassens konstruktor genom "super()"
"protected" ger fortfarande åtkomst till subklasser. 

Klassen shape har en [[abstrakt metod]] draw. En abstrakt metod behövs implementeras i subklasserna. 

Klassen "Object" är en superklass till alla klasser i Java. Alla klasser ärver toString() och equals() från Object.
#prog 

