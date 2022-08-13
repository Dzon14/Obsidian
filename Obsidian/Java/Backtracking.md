# Backtracking
Strategi för att lösa vissa typer av problem. Problemet bryts ned i ett antal steg
Ex:
- Hitta den kortaste vägen genom en labyrint
- Placera ut åtta damer på ett shackbräde
- Lös ett Sudoku-pussel

Idé:
- Prova en hypotes
		- Notera detta i någon datastruktur
- Undersök [[Rekursion|rekursivt]] lösningarna som återstår
- Basfall: lyckad eller misslyckad lösning

## Pseudokod för backtracking
allmän backtracking som kontrollerar om det finns minst en lösning:
boolean solve(v)
	if v is a solution
		return true
	for each promising choice c
		make choice c
		if  (solve(v with c))
			return true
		unmake choice c
	return false

## Exempel: Åttadamersproblemet (Schack)
Mn vill placera ut 8 damer på ett shackbräde utan att de hotar varandra.
**Algoritm:**
- Placera första damen så tidigt som möjligt på första raden, sen andra raden osvosv..
- Om damen ej kan placeras på en rad, gå tillbaka till föregående och finn ny plats. Om plats finns forsätt att placera damer framåt, annars gå till föregående rad.
- När sista raden har en dam har vi löst problemet.

[[Rekursion|rekursiv]] lösning till problemet:
```java
private boolean solver(int row) {
	if (row == 8) {
		return true;
	}
	for (int col = 0; col < 8; col++) {
		if (board.tryAddQueen(row, col)) {
			if (solve(row + 1)) {
				return true;
			}
			board.removeQueen(row, col);
		}
	}
	return false;
}
```


#prog 