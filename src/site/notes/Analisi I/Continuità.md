---
{"dg-publish":true,"permalink":"/analisi-i/continuita/"}
---

## Definizione - Continuità #def 
Sia $I$ intervallo di $\mathbb{R}, f:I\to\mathbb{R}$
Sia $c\in I$
Diciamo che $f$ è **continua** in $c$ se $\exists\lim_{x\to c}f(x)$ e vale $f(c)$
Diciamo che $f$ è **continua** in $I$ se è continua in ogni suo punto

## Teorema degli Zeri #teor 
Sia $f:[a,b]\to\mathbb{R}$ continua e supponiamo $f(a)\cdot f(b)<0$
Allora
$$\exists \ c\in(a,b)\mbox{ t.c. } f(c)=0$$
#### Dimostrazione #dim 
Assumiamo $f(a)<0<f(b)$
Sia $c_0=\frac{a+b}{2}$ punto medio di $(a,b)$
Continuo a dividere a metà:
- Trovo lo $0\longrightarrow$ teorema dimostrato
- Vado avanti indefinitivamente:
	1) $a\le a_n\le b_n\le b\ \ \ \ \forall n\in\mathbb{N}$
	2) $a_{n+1}\ge a_n\ \ \ \forall n\Rightarrow a_n\nearrow$
	3) $b_{n+1}\le b_n\ \ \ \forall n\Rightarrow b_n\searrow$
	4) $b_n-a_n=\frac{b-a}{2^n}$
	5) $f(a_n)<0<f(b_n)\forall n\in\mathbb{N}$
	Da 2) e 3) segue che $\exists \ \lim_{n\to+\infty}a_n$ e $\exists \ \lim_{n\to+\infty}b_n$.
	Inoltre da 1) si ha che tali limiti sono numeri reali.
	Da 4) ho che $b_n-a_n=\frac{b-a}{2^n}\to0$ per $n\to+\infty$ 
	quindi $\lim_{n\to+\infty}a_n=\lim_{n\to+\infty}b_n=c$ .
	Infine da 5) e usando il teorema del confronto deduco che
	$\lim_{n\to+\infty}f(a_n)\le0$, analogamente $\lim_{n\to+\infty}f(b_n)\ge0$
	Poiché $f$ è continua, si ha che:
	$\lim_{n\to+\infty}f(a_n)=f(c)\le0$ e $\lim_{n\to+\infty}f(b_n)=f(c)\ge0$
	$\Rightarrow f(c)=0$

## Teorema dei Valori Intermedi #teor 
Sia $I$ intervallo di $\mathbb{R}$, sia $f:I\to\mathbb{R}$ continua
Allora $f(I)$ è un intervallo (eventualmente degenere)
> **Intervallo Degenere:** _un solo punto_
#### Dimostrazione #dim
- Se $f$ è costante $=k\Rightarrow f(I)=\{K\}\longrightarrow$ intervallo degenere
- Se $f$ non è costante:
	$\exists\ y_1,y_2\in f(I)$ con $y_1\neq y_2$
	Devo mostrare che $\forall y:y_1<y<y_2$ si ha che $y\in f(I)$
	Siano $x_1,x_2\in I\mbox{ t.c. } f(x_1)=y_1, f(x_2)=y_2$ ($x_1\neq x_2$ poiché $f$ è una funzione)
	Supponiamo $x_1<x_2$
	Introduco una funzione $g:[x_1,x_2]\to\mathbb{R}, g(x)=f(x)-y\ \ \ \ (y_1<y<y_2)$ 
	Verifichiamo che $g$ soddisfa le ipotesi del [[Analisi I/Continuità#Teorema degli Zeri teor\|Teorema degli Zeri]] 
	Infatti:
	- $g(x_1)=f(x_1)-y=y_1-y<0$
	- $g(x_2)=f(x_2)-y=y_2-y>0$
	- $g$ è continua in $[x_1,x_2]$ (perché lo è su $I$)
	Applico il Teorema degli Zeri a $g$ è deduco che
	$\exists c\in(x_1,x_2)\mbox{ t.c. }g(c)=0\Leftrightarrow f(c)-y=0\Leftrightarrow f(c)=y\Rightarrow y\in f(I)$

## Teorema di Weierstrass #teor 
Sia $f:[a,b]\to\mathbb{R}$ continua
Allora $f$ ammette **massimo** e **minimo**
## Teorema - _operazioni su funzioni continue_ #teor 
Siano $f,g:I\to\mathbb{R}$ continue
allora:
$$\begin{cases}
f+g &\text{è continua}\\
f\cdot g &\text{è continua}\\
{f}/{g} &\text{è continua }(g\neq0)
\end{cases}$$
Inoltre $f:I\to\mathbb{R},g:J\to\mathbb{R}$ e $f(I)\subset J$. 
Se $f$ è continua su $I$ e $g$ è continua su $J$
Allora $g\circ f$ è continua su $I$.
Se $f:I\to f(I)$ è invertibile e continua $\Rightarrow f^{-1}$ è continua
Denotiamo
$$C(I,\mathbb{R})=\Big\{f:I\to\mathbb{R}\mid f\text{ continua}\Big\}$$