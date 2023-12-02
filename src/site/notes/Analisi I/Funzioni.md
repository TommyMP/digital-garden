---
{"dg-publish":true,"permalink":"/analisi-i/funzioni/"}
---

#### Definizione #def
Siano $A,B \neq \varnothing$, chiamiamo **funzione** da $A$ a $B$ una legge $f$ che ad ogni elemento di $A$ associa uno ed un solo elemento di $B$: $$f\colon A\to B$$$$\forall x \in A, \exists! y \in B \ \mbox{t.c.}\ y=f(x)$$
##### Insieme Immagine
$$f(A) = \{\ y \in B \mid \exists x \in A\colon f(x)=y \ \}$$
##### Funzione Suriettiva
$f(A)=B$, cioè se: $$\forall y \in B, \exists x \in A \ \mbox{t.c.} \ f(x)=y$$
##### Funzione Iniettiva
$$ \forall y \in f(A), \exists! x \in A \ \mbox{t.c.} \ f(x)=y$$
##### Funzione Invertibile/Biettiva/Biunivoca
Funzione sia [[Analisi I/Funzioni#Funzione Suriettiva\|su]] sia [[Analisi I/Funzioni#Funzione Iniettiva\|I-I]] 

##### Funzione Inversa:
Sia $f\colon A \to B$ invertibile, chiamiamo **funzione inversa** di $f$ la funzione $f^{-1}\colon B \to A$ definita come segue:
$$\forall y \in B, f^{-1}(y) \text{ è l'unica soluzione dell'equazione } f(x)=y$$
##### Composizione
Siano $f\colon A\to B,\ g\colon C \to D$ supponiamo che $f(A)\subseteq C$, chiamiamo **funzione composta** $$g\circ f\colon A \to D$$ la funzione: $$\forall x \in A\colon (g\circ f)(x) = g\Big(f(x)\Big)$$ **Osserviamo** che non è detto che possa fare $f\circ g$. $$g \circ f \neq f \circ g$$
##### Funzione Identità
$$Id_A: \begin{align*}{A\to A} \\ {x \mapsto x} \end{align*} $$ **Osservazione:** invertibile
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


## Funzioni Pari e Dispari


