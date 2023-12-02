---
{"dg-publish":true,"permalink":"/analisi-i/funzioni/"}
---

#### Definizione #def
Siano $A,B \neq \varnothing$, chiamiamo **funzione** da $A$ a $B$ una legge $f$ che ad ogni elemento di $A$ associa uno ed un solo elemento di $B$: 
$$f\colon A\to B$$
$$\forall x \in A, \exists! y \in B \ \mbox{t.c.}\ y=f(x)$$
##### Insieme Immagine
$$f(A) = \{\ y \in B \mid \exists x \in A\colon f(x)=y \ \}$$
##### Funzione Suriettiva
$f(A)=B$, cioè se: 
$$\forall y \in B, \exists x \in A \ \mbox{t.c.} \ f(x)=y$$
##### Funzione Iniettiva
$$ \forall y \in f(A), \exists! x \in A \ \mbox{t.c.} \ f(x)=y$$
##### Funzione Invertibile/Biettiva/Biunivoca
Funzione sia [[Analisi I/Funzioni#Funzione Suriettiva\|su]] sia [[Analisi I/Funzioni#Funzione Iniettiva\|I-I]] 

##### Funzione Inversa:
Sia $f\colon A \to B$ invertibile, chiamiamo **funzione inversa** di $f$ la funzione $f^{-1}\colon B \to A$ definita come segue:
$$\forall y \in B, f^{-1}(y) \text{ è l'unica soluzione dell'equazione } f(x)=y$$
##### Composizione
Siano $f\colon A\to B,\ g\colon C \to D$ supponiamo che $f(A)\subseteq C$, chiamiamo **funzione composta**
$$g\circ f\colon A \to D$$

la funzione:

$$\forall x \in A\colon (g\circ f)(x) = g\Big(f(x)\Big)$$

**Osserviamo** che non è detto che possa fare $f\circ g$. 
$$g \circ f \neq f \circ g$$
##### Funzione Identità
$$Id_A: \begin{align*}{A\to A} \\ {x \mapsto x} \end{align*} $$ 
**Osservazione:** invertibile

$$
\begin{align*}
		(f \circ f^{-1})(x) = x \ \ \ \ \ \forall x \in B \\
		(f^{-1} \circ f)(x) = x \ \ \ \ \ \forall x \in A \\
\end{align*}
				$$

cioè

$$
\begin{align*}
f\circ f^{-1} = Id_B \\
f^{-1}\circ f = Id_A
\end{align*}
$$
## Funzioni Monotone
Siano $A\subseteq\mathbb{R},f:A\to\mathbb{R}$
- Diciamo che $f$ è **crescente** se $\forall x_1,x_2\in A$ con $x_1<x_2$ si ha che $f(x_1)\le f(x_2)$
- Diciamo che $f$ è **decrescente** se $\forall x_1,x_2\in A$ con $x_1\le x_2$ si ha che $f(x_1)\ge f(x_2)$
##### Definizione - Strettamente #def 
Diciamo che $f$ è **strettamente** crescente se $\forall x_1,x_2\in A$ con $x_1<x_2$ si ha che $f(x_1)<f(x_2)$
### Teorema #teor
Siano $f:A\to\mathbb{R},g:B\to\mathbb{R}$, $f(A)\subseteq B$
Se $f$ e $g$ sono monotone, allora anche $g\circ f$ è monotona. In particolare:
- $g\circ f$ è $\nearrow$ se $f$ e $g$ hanno la stessa monotonia
- $g\circ f$ è $\searrow$ se $f$ e $g$ hanno monotonia diversa
### Teorema #teor
Sia $f:A\to\mathbb{R}$
Se $f$ è strettamente monotona $\Rightarrow f$ è [[Analisi I/Funzioni#Funzione Iniettiva\|iniettiva]]
e $f^{-1}:f(A)\to A$ è strettamente monotona della stessa monotonia
#### Dimostrazione #dim 
Voglio verificare che se $f(x_1)=f(x_2)\Rightarrow x_1=x_2$ 
Supponiamo $f$ strettamente $\nearrow$, se fosse $x_1<x_2\Rightarrow f(x_1)<f(x_2)$ ma ciò non è possibile

_dimostrazione non completa..._
## Funzioni Pari e Dispari
Sia $A\subseteq\mathbb{R}$ simmetrico rispetto all'origine (se $x\in A\Rightarrow-x\in A$)
Sia $f:A\to\mathbb{R}$
- Diciamo che $f$ è **pari** se $f(x)=f(-x)$
- Diciamo che $f$ è **dispari** se $\forall x\in A, f(x)=-f(-x)$
## Periodicità
### Definizione - Insieme Periodico #def 
Sia $T\in\mathbb{R^+}\setminus\{0\}$, diciamo che $A\subseteq\mathbb{R}$ è $T\text{-Periodico}$ se $\forall x\in A,\forall k\in\mathbb{Z}$ si ha che $x+kt\in A$
### Definizione - Funzione Periodica #def 
Sia $A\subseteq\mathbb{R}$ $T\text{-Periodico}, f:A\to\mathbb{R}$
Diciamo che $f$ è $T\text{-Periodico}$ se $\forall x\in A:f(x)=f(x+T)$

