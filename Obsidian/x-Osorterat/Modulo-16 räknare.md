---
tags: [el]
---
# Modulo-16 räknare

Exempel: Konstruktion av mod-16 räknare med [[Adder]], [[Register]] och [[mux|Multiplexer]]: 

```VHDL
if (r1 = 0 && r2 = 0)
	Q = 0
else if (r1 = 1)
	if (r2 = 1)
		Q += 1
	else 
		Q += 3
else
	Q += 2
end
```


![[Pasted image 20211101134841.png | 600]]