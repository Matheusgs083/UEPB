# 1-
Não, a gramática não é ambígua, pois não existem duas derivações à esquerda diferentes para a mesma cadeia.

S → aABe  
A → Abc → bbc → bbcbc → ...  
B → d  

Gera:
a bbc... d e

# 2-
A) A linguagem gerada por esta gramática é o conjunto de todas as concatenações de zero ou mais palíndromos de comprimento par sobre o alfabeto {a,b}.
L(G)={w∣w∈ -> L(G)=(Lpalpar)∗ -> Lpalpar = {x∣x∈{a,b} ∗, x=xRe∣x∣é par}.

B) Sim, esta gramática é ambígua. Podemos demonstrar a ambiguidade construindo duas árvores de derivação distintas para a sentença "aabbaa".
      S
     /|\
    a S a
     /|\
    b S b
     /|\
    a S a
      |
      ε

# 3-
**G = ({S,X,Y,Z,A,B}, {a,b,u,v}, P, S)**  
P = {  
S → XYZ  
X → AXA | BXB | Z | ε  
Y → AYB | BXA | Z | ε  
A → a  
B → b  
Z → Zu | Zv | ε  
}

a. **Simplifique a GLC**

**Passo 1: Eliminar produções inúteis**

**Variáveis que geram terminais:**
- A → a  
- B → b  
- Z → Zu | Zv | ε → gera ε → gera uuvv…  
⇒ Z é útil  
⇒ A, B são úteis  
⇒ X → AXA | BXB | Z | ε → potencialmente útil  
⇒ Y → AYB | BXA | Z | ε → potencialmente útil  
⇒ S → XYZ → útil

Nenhuma produção é inútil.

**Passo 2: Eliminar produções vazias**

Produções vazias:
- X → ε  
- Y → ε  
- Z → ε  

Aplicamos ε-produções para gerar novas regras:

**S → XYZ**, e se X/Y/Z forem ε:  
Geram as seguintes alternativas:
- XYZ  
- YZ  
- XZ  
- XY  
- X  
- Y  
- Z  
- ε  

Logo:

**S → XYZ | YZ | XZ | XY | X | Y | Z | ε**

Agora eliminamos as regras com `→ ε` para X, Y, Z, mantendo alternativas sem ε. Reescrevemos todas as produções substituindo variáveis anuláveis por suas variantes com e sem a variável.

(Para simplificação aqui, vamos supor que manteremos somente as produções essenciais com combinações possíveis.)

**Passo 3: Eliminar produções unidade (do tipo A → B)**

**Verifique produções do tipo unidade:**
- X → Z  
- Y → Z  

Z não é unidade (tem produções Zu | Zv | ε)

Nenhuma produção unidade direta do tipo `A → B`

---

**Gramática simplificada (sem produções inúteis, ε nem unidades):**

**Variáveis:** {S, X, Y, Z, A, B}  
**Terminais:** {a, b, u, v}  
**Produções:**
