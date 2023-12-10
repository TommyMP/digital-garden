---
{"dg-publish":true,"permalink":"/analisi-i/calcolo-differenziale/"}
---

## Derivate
Sia $f:(a,b)\to\mathbb{R}$, siano $c,d\in(a,b)$
Chiamo **rapporto incrementale** di $f$ tra $c$ e $d$:
$$\frac{f(d)-f(c)}{d-c}$$

#### Definizione #def 
Sia $f:(a,b)\to\mathbb{R}$, sia $c\in(a,b)$
Diciamo che $f$ è **derivabile** in $c$ se
$$\exists\lim_{x\to c}\frac{f(x)-f(c)}{x-c}\in\mathbb{R}$$
e in tal caso indichiamo tale limite con $f'(c)$ (derivata di $f$ in $c$)
###### Interpretazione Geometrica
$f'(c)$ è il coefficiente angolare della retta tangente al grafico di $f$ in $c,f(c)$

## Derivate di Funzioni Elementari
$f(x)=x^n\ \ \ \ \ \ \ \ n\in\mathbb{N}$
> **Formula del Binomio di Newton**
> $$(a+b)^n=\sum_{k=0}^{n}{n\choose k}a^{n-k}b^k$$
> dove:
> $${n\choose k}=\frac{n!}{k!(n-k)!}\ \ \ \text{ e }\ \ \ 0!=1$$

*I CALCOLI NON SONO RIPORTATI, LEZIONE 30/10/23*
- $f(x)=x^n\ \ \ \ \ \ \ \ f'(c)=nc^{n-1}$
- $f(x)=e^x\ \ \ \ \ \ \ \ f'(c)=e^c$
	- $f(x)=a^x\ \ \ \ \ \ \ \ f'(x)=\log a\cdot a^x$
- $f(x)=\sin x\ \ \ \ \ \ \ \ f'(c)=\cos c$
- $f(x)=\cos x\ \ \ \ \ \ \ \ f'(c)=-\sin c$

## Teorema - Caratterizzazione #teor
Sia $f:I\to\mathbb{R}$, sia $c\in I$
Allora le due seguenti affermazioni sono equivalenti:
1) $f$ è derivabile in $c$
2) $\exists\ l\in\mathbb{R}\mbox{ t.c. }f(x)=f(c)+l(x-c)+o(x-c)$ per $x\to c$ (e si ha $l=f'(c)$)
**Osservazioni:**
- $f$ derivabile in $c\Rightarrow f$ continua in $c$
	Infatti da 2), passando al limite, si ha:
	$$\lim_{x\to c}f(x)=\lim_{x\to c}(f(x)+\underbrace{l(x-c)}_0+\underbrace{o(x-c)}_0)=f(c)$$
- $f$ continua in $c$ $\nRightarrow f$ derivabile in $c$
	**es:** $f(x)=|x|$ (continua in $\mathbb{R}$ ma non derivabile in $0$)
	
#### Dimostrazione $1\Rightarrow 2$ #dim
Sia $f$ derivabile in $c$:
$$\begin{split}
&\lim_{x\to c}\frac{f(x)-f(c)}{x-c}=l\ \ \ (=f'(l))&(l\in\mathbb{R}) \\
\Leftrightarrow&\frac{f(x)-f(c)}{x-c}-l=o(1)&\ \ \ \ \ \ \ \ \ \ \ \ \text{ per }x\to c \\ \Leftrightarrow
&\frac{f(x)-f(c)}{x-c}=l+o(1)&\text{ per }x\to c\\ \Leftrightarrow
&f(x)-f(c)=l(x-c)+o(x-c)&\text{ per }x\to c\\ \Leftrightarrow&f(x)=f(c)+l(x-c)+o(x-c)&\text{ per }x\to c
\end{split}$$

#### Dimostrazione $2\Rightarrow1$ #dim 
Supponiamo $\exists\ l\in\mathbb{R}\mbox{ t.c. }$
$$\begin{split}
&f(x)=f(c)+l(x-c)+o(x-c)\ \ \ \ \ \ \ \ \ \ &\text{ per }x\to c\\\Leftrightarrow
&\frac{f(x)-f(c)}{x-c}=l+\frac{o(x-c)}{x-c}&\text{ per }x\to c\\ \Leftrightarrow
&\frac{f(x)-f(c)}{x-c}=l+o(1)&\text{ per }x\to c\\ \Leftrightarrow
&\lim_{x\to c}\frac{f(x)-f(c)}{x-c}=l\in\mathbb{R}
\end{split}$$

## Teorema - Algebra delle derivate #teor
Sia $I$ intervallo di $\mathbb{R}, f,g:I\to \mathbb{R},c\in I,k\in \mathbb{R}$
Se $f$ e $g$ sono derivabili in $c$, allora:
1) $\begin{cases}(f+g)'(c)=f'(c)+g'(c)\\(kf)'(c)=kf'(c)\end{cases}$
2) $(f\cdot g)'(c)=f'(c)\cdot g(c)+f(c)\cdot g'(c)$
3) $\Big(\frac{f}{g}\Big)'(c)=\frac{f'(c)\cdot g(c)-g'(c)\cdot f(c)}{(g(c))^2} \ \ \ \ \ \ g(c)\neq0$
#### Dimostrazione (2) #dim 
$$\begin{split}
&\frac{(fg)(x)-(fg)(c)}{x-c}=\\
=\ &\frac{f(x)g(x)-f(x)g(c)+f(x)g(c)-f(c)g(c)}{x-c}\\
=\ &\frac{f(x)(g(x)-g(c))}{x-c}+\frac{g(c)(f(x)-f(c))}{x-c}
\end{split}$$
Passo al limite per $x\to c$, quindi:
$$(f\cdot g)'(c)=f'(c)g(c)+f(c)g'(c)$$

## Teorema - Derivata Composizione #teor
Siano $I,J$ intervalli di $\mathbb{R},c\in I$
$f:I\to \mathbb{R},g:J\to \mathbb{R}, f(I)\subseteq J$
Supponiamo $f$ derivabile in $c$ e $g$ derivabile in $f(c)$.
Allora: $(g\circ f)'(c)=g'(f(c))\cdot f'(c)$
#### Dimostrazione #dim 
$$\frac{(g\circ f)(x)-(g\circ f)(c)}{x-c}=\frac{g(f(x))-g(f(c))}{x-c}$$
Per ipotesi $g$ è derivabile in $f(c)$ e dunque (per il [[Analisi I/Calcolo Differenziale#Teorema - Caratterizzazione teor\|teorema di caratterizzazione]]) si ha:
$$g(y)=g(f(c))+g'(f(c))(y-f(c))+o(y-f(c))\ \ \ \ \ \ \text{ per } y\to f(c)$$
Posso scegliere $y=f(x)$ (infatti $f(x)\to f(c)$ per $x\to c$ poiché $f$ è continua)
$$g\Big(f(x)\Big)=g\Big(f(c)\Big)+g'\Big(f(c)\Big)\Big(f(x)-f(c)\Big)+o\Big(f(x)-f(c)\Big)\ \ \ \ \ \ \ \ \ \ \ \ \ \text{ per }x\to c$$
Dunque:
$$\begin{split}
&\lim_{x\to c}\frac{(g\circ f)(x)-(g\circ f)(c)}{x-c}=\\
=&\lim_{x\to c}\frac{g\Big(f(c)\Big)+g'\Big(f(c)\Big)\Big(f(x)-f(c)\Big)+o\Big(f(x)-f(c)\Big)-g\Big(f(c)\Big)}{x-c}\\
=&g'\Big(f(c)\Big)\cdot f'(c)
\end{split}$$
>$$\begin{split}
&\frac{o\Big(f(x)-f(c)\Big)}{x-c}\longrightarrow0\ \ \ \ \ \text{ per }x\to c\\
=\ &\underbrace{o(1)\underbrace{\frac{\Big(f(x)-f(c)\Big)}{x-c}}_{f'(c)}}_{0\text{ per }x\to c}
\end{split}$$

## Teorema - Derivata dell'Inversa #teor
Sia $I$ intervallo di $\mathbb{R}, f:I\to \mathbb{R}$ invertibile e derivabile in $c\in I$
Supponiamo $f'(c)\neq0$
Allora, posto $y=f(c)$, si ha
$$(f^{-1})'\underbrace{(y)}_{f(c)}=\frac{1}{f'(\underbrace{f^{-1}(y)}_c)}$$

## Estremanti Locali
#### Definizione #def 
Sia $I$ intervallo di $\mathbb{R}$, sia $f:I\to\mathbb{R}$, sia $c\in I$
- Diciamo che $c$ è **punto di minimo locale** per $f$ se $\exists\ \delta>0\mbox{ t.c. }\forall x\in(c-\delta,c+\delta)\cap I$ si ha $f(c)\le f(x)$
- Diciamo che $c$ è **punto di massimo locale** per $f$ se $\exists\ \delta>0\mbox{ t.c. }\forall x\in(c-\delta,c+\delta)\cap I$ si ha $f(c)\ge f(x)$

## Teorema - Fermat #teor
Sia $I$ intervallo di $\mathbb{R}$, sia $f:I\to\mathbb{R}$ 
Sia $c$ punto interno di $I$ ($c\in I\setminus\{\inf I,\sup I\}$)
Supponiamo $f$ derivabile in $c$ e $c$ estremante locale
Allora: $f'(c)=0$
#### Dimostrazione #dim 
Sia $c$ punto di minimo locale, dunque $\exists\ \delta\mbox{ t.c. } f(c)\le f(x)\ \forall x\in(c-\delta,c+\delta)\cap I$
Considero il rapporto incrementale
1) $\frac{\overbrace{f(x)-f(c)}^{\ge0}}{\underbrace{x-c}_{\ge0}}\ge0$
		$\forall x\in(c,c+\delta)\cap I$, scegliendo $\delta$ sufficientemente piccolo posso supporre $(c,c+\delta)\subset I$  $\longrightarrow$ sto usando che $c$ è punto interno
2) $\frac{\overbrace{f(x)-f(c)}^{\ge0}}{\underbrace{x-c}_{<0}}\le0$      $\forall x\in(c-\delta,c)$
Passando al limite:
1) $\lim_{x\to c^+}\frac{f(x)-f(c)}{x-c}\ge0$
2) $\lim_{x\to c^-}\frac{f(x)-f(c)}{x-c}\le0$
Poiché $f$ è derivabile in $c$ deve essere $f'(c)=\lim_{x\to c}\frac{f(x)-f(c)}{x-c}=0$

## Teorema - Rolle #teor
Sia $f:[a,b]\to\mathbb{R}$ continua in $[a,b]$ e derivabile in $(a,b)$
Supponiamo $f(a)=f(b)$
Allora: $\exists c\in(a,b)\mbox{ t.c. }f'(c)=0$
#### Dimostrazione #dim 
Dato che $f$ è continua su $[a,b]$, per il [[Analisi I/Continuità#Teorema di Weierstrass teor\|teorema di Weierstrass]] esistono $\max$ e $\min$ di $f$.
Ho 2 possibilità:
1) Se $\max f$ e $\min f$ sono entrambi assunti negli estremi (es. $f(a)=\max f$ e $f(b)=\min f$) allora, dall'ipotesi $f(a)=f(b)$ si deduce che $f$  è costante e dunque $f'(x)=0\forall x\in[a,b]$
2) Se almeno uno tra $\max$ e $\min$ è assunto all'interno di $(a,b)$ allora, in tale punto $c$. posso applicare il [[Analisi I/Calcolo Differenziale#Teorema - Fermat teor\|teorema di Fermat]] e dedurre che $f'(c)=0$

## Teorema  - Lagrange #teor
Sia $f:[a,b]\to\mathbb{R}$ continua in $[a,b]$ derivabile in $(a,b)$.
Allora: $\exists c\in(a,b):$
$$\underbrace{f'(c)}_{\begin{split}\text{coefficiente angolare }\\\text{della retta tangente }\\\text{al grafico di }f\ \ \ \ \ \ \\\text{nel punto }(c,f(c))\ \ \ \end{split}}=\underbrace{\frac{f(b)-f(a)}{b-a}}_{\begin{split}\text{coefficiente angolare}\\\text{della retta passante }\ \\\text{per }(a,f(a))\text{ e }(b,f(b))\end{split}}$$
#### Dimostrazione #dim 
Considero la funzione:
$$g(x)=f(x)-f(a)-\frac{f(b)-f(a)}{b-a}(x-a)$$
Osserviamo che $g$ è continua in $[a,b]$ e derivabile in $(a,b)$
Inoltre 
$$\begin{split}g(a)=f(a)-f(a)=0 \\ g(b)=f(b)-f(a)-\frac{f(b)-f(a)}{\cancel{b-a}}\cdot\cancel{(b-a)}=0\end{split}$$
Posso applicare il [[Analisi I/Calcolo Differenziale#Teorema - Rolle teor\|teorema di Rolle]] a $g$ e deduco che $\exists c\in(a,b)\mbox{ t.c. }$
$$g'(c)=0\Leftrightarrow f'(c)=\frac{f(b)-f(a)}{b-a}$$
## Teorema - Test di Monotonia #teor
Sia $I$ intervallo di $\mathbb{R}, f:I\to\mathbb{R}$ derivabile.
Allora:
1) $f$ è $\nearrow$ in $I\Leftrightarrow f'(x)\ge0\ \forall x\in I$
2) $f$ è $\searrow$ in $I\Leftrightarrow f'(x)\le0\ \forall x\in I$
#### Dimostrazione #dim
##### Punto 1)
###### $\Rightarrow$
Supponiamo $f\nearrow$ in $I$
Siano $x,c\in I\ (x\neq c)$, si ha per definizione di $f\nearrow$:
$$\frac{f(x)-f(c)}{x-c}\ge0$$
Passando al limite per $x\to c$, deduco per il teorema del Confronto:
$$f'(c)=\lim_{x\to c}\frac{f(x)-f(c)}{x-c}\ge0$$
###### $\Leftarrow$
Assumiamo per ipotesi $f'(x)\ge0\ \forall x\in I$
Siano $x_1,x_2\in I$ con $x_1\le x_2$,
allora si ha che $f_{\restriction{[x_1,x_2]}}:[x_1,x_2]\to\mathbb{R}$ soddisfa le ipotesi del [[Analisi I/Calcolo Differenziale#Teorema - Lagrange teor\|teorema di Lagrange]], dunque:
$$\exists c\in(x_1,x_2):\frac{f(x_2)-f(x_1)}{x_2-x_1}=f'(c)\ge0$$
Ciò implica $f(x_2)\ge f(x_1)$ (cioè $f\nearrow$) (e $x_1,x_2$ sono arbitrari)

##### Punto 2)
Analogo al [[Analisi I/Calcolo Differenziale#Punto 1)\|#Punto 1)]]
#### Osservazione
In generale **non** vale lo stesso risultato di equivalenza tra $f\nearrow$ strettamente e $f'(x)>0\ \forall x\in I$
Continua a valere che $f'(x)>0\ \forall x\in I\Rightarrow f\nearrow$ strettamente (si dimostra come prima)
## Funzioni Convesse
#### Definizione #def 
Sia $f:I\to\mathbb{R}$ derivabile
- Diciamo che $f$ è **convessa** in $I$ se 
	$\forall c,x\in I: f(x)\ge f(c)+f'(c)(x-c)$
- Diciamo che $f$ è **concava** in $I$ se
	$\forall c,x\in I:f(x)\le f(c)+f'(c)(x-c)$

### Teorema - Test di Convessità I #teor
Sia $f:I\to\mathbb{R}$, $I$ intervallo di $\mathbb{R}$, $f$ derivabile
Allora:
- $f$ convessa su $I\Leftrightarrow f'\nearrow$ su $I$
- $f$ concava su $I\Leftrightarrow f'\searrow$ su $I$
##### Dimostrazione (primo punto) #dim
###### $\Rightarrow$
Assumo $f$ convessa su $I$:
$$\begin{split}\forall x,y\in I:\ &f(x)\ge f(y)+f'(y)(x-y)\\& f(y)\ge f(x)+f'(x)(y-x)\end{split}$$
Sommando membro a membro si ha
$$\begin{split}&\ \cancel{f(x)}+f(y)\ge\cancel{f(x)}+f(y)+(x-y)(f'(y)-f'(x))\\\Leftrightarrow &\ (f'(y)-f'(x))(y-x)\ge0\Leftrightarrow f'\nearrow\end{split}$$

###### $\Leftarrow$
Assumo $f'\nearrow$ in $I$
$\forall c,x\in I,\ c<x$
$f$ soddisfa le ipotesi del [[Analisi I/Calcolo Differenziale#Teorema - Lagrange teor\|teorema di Lagrange]] in $[c,x]$, e dunque $\exists d\in(c,x):$
$$f(x)-f(c)=f'(d)(x-c)$$
Poiché $f'\nearrow$
$$f(x)-f(c)\ge f'(d)(x-c)\Rightarrow f \text{ convessa}$$
### Definizione - Funzione derivabile 2 volte #def 
Sia $f:I\to\mathbb{R}$ derivabile, sia $c\in I$
Diciamo che $f$ è **derivabile 2 volte** in $c$ se $f'$ è derivabile in $c$
Indichiamo con $f''(c)=(f')'(c)$
### Teorema - Test di Convessità II #teor
> Si ottiene combinando [[Analisi I/Calcolo Differenziale#Teorema - Test di Monotonia teor\|Test di Monotonia]] e [[Analisi I/Calcolo Differenziale#Teorema - Test di Convessità I teor\|Test di Convessità I]]

Sia $f:I\to\mathbb{R}$, $I$ intervallo, $f$ derivabile 2 volte su I
Allora:
- $f$ convessa $\Leftrightarrow f''(x)\ge0\ \forall x\in I$
- $f$ concava $\Leftrightarrow f''(x)\le0\ \forall x\in I$
### Punti di Flesso
Punti in cui $f$ cambia convessità

### Teorema - Condizioni Sufficienti per gli Estremanti Locali #teor
Sia $f:I\to\mathbb{R}$, sia $c\in I$
1) Se $\exists a,b\in I,\ a<c<b\mbox{ t.c. }$ 
	$f\nearrow$ in $(a,c)$ 
	e $f\searrow$ in $(c,b)$  
		$\Rightarrow$ $c$ è punto di $\max$ locale
2) Se $\exists a,b\in I,\ a<c<b\mbox{ t.c. }$
	$f\searrow$ in $(a,c)$ e
	$f\nearrow$ in $(c,b)$
		$\Rightarrow c$ è punto di $\min$ locale

Sia $I$ intervallo di $\mathbb{R}$, $f:I\to\mathbb{R}$, sia $c\in I$, supponiamo $f$ derivabile 2 volte in $c$
1) Se $f'(c)=0$ e $f''(c)<0\Rightarrow c$ è punto di $\max$ locale
1) Se $f'(c)=0$ e $f''(c)>0\Rightarrow c$ è punto di $\min$ locale