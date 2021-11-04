# Backtracking
Strategi för att lösa vissa typer av problem. Problemet bryts ned i ett antal steg
Ex:
- Hitta den kortaste vägen genom en labyrint
- Placera ut åtta damer på ett shackbräde
- Lös ett Sudoku-pussel

Idé:
- Prova en hypotes
		- Notera detta i någon datastruktur
- Undersök rekursivt lösningarna som återstår
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

## Exempel: Åttadamersproblemet
SKRIV om dam-exemplet seda 


#prog 