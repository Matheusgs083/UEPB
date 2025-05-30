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
