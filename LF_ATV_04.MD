## 1-

A) ((aa+ab+ba+bb))*(a+b)
B) ((a+b)(a+b)(a+b)(a+b))*
C) b*(ab*ab*)*
D) a*ba*(a*ba*ba*)*

## 2-
Resposta Correta: d. (b*ab*ab*)* 

## 3-
a. Somente as igualdades I e II são verdadeiras.

## 4- 
A Gramática Regular G = (V, T, P, S) é definida como:
V = {q0, q1, q2, q3, q4, q5} (Não-terminais)
T = {a, b} (Terminais)
S = q0 (Símbolo inicial)
P (Produções):
1.  `q0 → a q1`
2.  `q0 → b q4`
3.  `q1 → a q2`
4.  `q1 → b q4`
5.  `q2 → a q3`
6.  `q2 → b q4`
7.  `q3 → a q3`
8.  `q3 → b q4`
9.  `q3 → ε` (pois q3 é um estado de aceitação)
10. `q4 → a q1`
11. `q4 → b q5`
12. `q5 → a q1`
13. `q5 → b q5`
14. `q5 → ε` (pois q5 é um estado de aceitação)

## 5- 
-
digraph AFN_E {
	rankdir=LR
	node [shape=circle]
	S0
	S1 [shape=doublecircle]
	S2
	S3
	S4
	S5
	S6
	start [shape=point]
	start -> S0
	S0 -> S1 [label=a]
	S1 -> S2 [label=c]
	S2 -> S3 [label=a]
	S3 -> S1 [label="ε"]
	S1 -> S4 [label=d]
	S4 -> S5 [label=e]
	S5 -> S6 [label=f]
	S6 -> S1 [label="ε"]
}

-digraph AFD {
	rankdir=LR
	node [shape=circle]
	A [label="{S0}" shape=circle]
	B [label="{S1}" shape=doublecircle]
	C [label="{S2}" shape=circle]
	D [label="{S4}" shape=circle]
	E [label="{S1,S3}" shape=doublecircle]
	F [label="{S5}" shape=circle]
	G [label="{S1,S6}" shape=doublecircle]
	start [shape=point]
	start -> A
	A -> B [label=a]
	B -> C [label=c]
	B -> D [label=d]
	C -> E [label=a]
	D -> F [label=e]
	E -> C [label=c]
	E -> D [label=d]
	F -> G [label=f]
	G -> C [label=c]
	G -> D [label=d]
}
-
* A → aB
* B → cC
* B → dD
* B → ε (porque B é um estado final: {S1})
* C → aE
* D → eF
* E → cC
* E → dD
* E → ε (porque E é um estado final: {S1,S3})
* F → fG
* G → cC
* G → dD
* G → ε (porque G é um estado final: {S1,S6})


