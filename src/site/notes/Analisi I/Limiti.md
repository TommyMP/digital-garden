---
{"dg-publish":true,"permalink":"/analisi-i/limiti/"}
---

### Definizione - Intervallo Forato #def 
Diciamo che $J\subseteq\mathbb{R}$ è un **intervallo forato** se $\exists c\in\mathbb{R}\setminus J \mbox{ t.c. } J\cup\{c\}$ è un intervallo 

### Definizione - Intorno #def 
- Dato $c\in\mathbb{R}$, chiamiamo **intorno di $c$** un qualsiasi intervallo della forma $(c-r,c+r)$ per un qualche $r>0$
- Chiamiamo **intorno di $\begin{array}.+\infty\\-\infty\end{array}$** un qualsiasi intervallo della forma $\begin{array}.(a,+\infty)\\(-\infty,b)\end{array}$
##### Osservazione
- $U$ è un intorno di $c$ se $\exists r>0\mbox{ t.c. }U=(c-r,c+r)$ cioè $x\in U\Leftrightarrow|x-c|<r$
- $U$ è un intorno di $+\infty$ se $\exists a\in\mathbb{R}\mbox{ t.c. }U=(a,+\infty)$ cioè $x\in U\Leftrightarrow x>a$

## Teorema Ponte #teor
Le successive due definizioni di limite (tramite successione e tramite intorno) sono **equivalenti**
## Definizione 1 (succcessione) - Limite #def 
Sia $I$ intervallo o intervallo forato,
Sia $f:I\to\mathbb{R}$, sia $c\in\Big[\inf I, \sup I\Big]$,
$l\in\overline{\mathbb{R}}$.
Diciamo che 
$$\exists\lim_{x\to c}f(x)=l$$
se 
$$\forall(a_n)_{n\in\mathbb{N}}\text{ successione in } I\setminus\{c\} \mbox{ t.c. } a_n\xrightarrow[n\to+\infty]{}c \ \ \ \text{ si ha } \ \ \ f(a_n)\to l$$
- **convergente:** $l\in\mathbb{R}$
- **divergente:** $l=\pm\infty$
- **infinitesima:** $l=0$

## Definizione 2 (intorno) - Limite #def
Sia $I$ intervallo o intervallo forato,
Sia $f:I\to\mathbb{R}$, sia $c\in\Big[\inf I, \sup I\Big]$,
$l\in\overline{\mathbb{R}}$.
Diciamo che
$$\exists\lim_{x\to c}f(x)=l$$
se
$$\forall\ V \text{ intorno di } l,\exists\ U_V \text{ intorno di } c \mbox{ t.c } \forall x\in U_V\setminus\{0\}\ \ \text{ si ha }\ \ f(x)\in V$$
##### Osservazione
Esempio caso $l,c\in\mathbb{R}$ 
$$\forall\varepsilon>0,\exists\delta_\varepsilon>0\mbox{ t.c. se } \underset{(x\neq0)}{|x-c|}<\delta_\varepsilon\ \ \ \text{ si ha } \ \ \ |f(x)-l|<\varepsilon$$ 
> $\varepsilon$ è il raggio dell'intorno di $l$
> $\delta_\varepsilon$ è il raggio dell'intorno di $c$

## Definizione - Limiti Unilaterali #def 
Sia $I$ intervallo o intervallo forato, $c\in[\inf{I},\sup{I}] \cap\mathbb{R}, l\in\overline{\mathbb{R}}$.
Diciamo che $f$ ha limite per $x\to c$ 
- da **sinistra** (e scriviamo $x\to c^-$) se
$$\lim_{x\to c}f(x)_{\restriction{I\cap(-\infty,c)}}=l$$
- da **destra** (e scriviamo $x\to c^+$) se
$$\lim_{x\to c}f(x)_{\restriction{I\cap(c,+\infty)}}=l$$
## Teorema - Cambio di Variabile #teor 
Siano $I, J$ intervalli o intervalli forati, $f:I\to\mathbb{R},g:J\to\mathbb{R},f(I)\subseteq J$
Siano $x_0\in[\inf{I},\sup{I}], l\in[\inf{J},\sup{J}]$
Se $\lim_{x\to x_0}f(x)=l$ e $\lim_{y\to l}g(y)=k$
Supponiamo $\exists$ un intorno $U$ di $x_0 \mbox{ t.c. } f(x)\neq l$ in $U\setminus\{x_0\}$
Allora:
$$\lim_{x\to x_0}g(f(x))=k$$

## Teorema - Unicità del Limite #teor 
Sia $I$ intervallo o intervallo forato,
$f: I\to\mathbb{R}, c\in[\inf{I},\sup{I}], m,l\in\overline{\mathbb{R}}$
Se $\lim_{x\to c}f(x)=l$ e $\lim_{x\to c}f(x)=m$
allora $l=m$

## Teorema - Permanenza del segno #teor 
Sia $I$ intervallo o intervallo forato,
$f:I\to\mathbb{R}, c\in[\inf{I},\sup{I}], l\in\overline{\mathbb{R}}$
supponiamo $\lim_{x\to c}f(x)=l$
Allora:
1) Se $l>0\Rightarrow\exists$ un intorno $U$ di $c \mbox{ t.c. } f(x)>0 \ \ \ \forall x\in U\cap I \setminus\{c\}$
2) Se $l<0\Rightarrow\exists$ un intorno $U$ di $c \mbox{ t.c. } f(x)<0 \ \ \ \forall x\in U\cap I \setminus\{c\}$

## Teorema - Dei 2 Carabinieri #teor 
Sia $I$ intervallo o intervallo forato di $\mathbb{R}$,
$f,g,h:I\to\mathbb{R}, c\in[\inf{I},\sup{I}], l\in\mathbb{R}$
Se $\lim_{x\to c}f(x)=l$ e $\lim_{x\to c}h(x)=l$
e $\exists$ un intorno $U$ di $c\mbox{ t.c. } f(x)\le g(x)\le h(x) \ \ \ \forall x \in U\cap I\setminus\{c\}$ allora: $\lim_{x\to c}g(x)=l$

## Calcolo dei limiti
- **Polinomi:** $lim_{x\to\pm\infty}$ come per le successioni
- **Funzioni Razionali:** $\frac{p(x)}{q(x)}$ con $p,q$ polinomi
	- $\lim_{x\to+\infty}$ come per le successioni
	- $\lim_{x\to c}$ con $c\in\mathbb{D}\ (q(c)\neq0)$, come per le successioni
	- $\lim_{x\to c}$ con $q(c)=0$:
		- $\lim_{x\to c}\frac{1}{(x-c)^A}=+\infty$ con $A$ **pari**
		- $\lim_{x\to c}\frac{1}{(x-c)^B}=\ \nexists$ con $B$ **dispari**
			- $\lim_{x\to c^+}\frac{1}{(x-c)^B}=+\infty$
			- $\lim_{x\to c^-}\frac{1}{(x-c)^B}=-\infty$
- **Funzioni Esponenziali**:
	- $a>1$
		- $\lim_{x\to+\infty}a^x=+\infty$
		- $\lim_{x\to-\infty}a^x=0$
		- $\lim_{x\to c}a^x=a^c$
	- $0<a<1$
		- $\lim_{x\to+\infty}a^x=0$
		- $\lim_{x\to-\infty}a^x=+\infty$
		- $\lim_{x\to c}a^x=a^c$
- **Funzioni Logaritmiche:**
	- $a>1$
		- $\lim_{x\to+\infty}\log_ax=+\infty$
		- $\lim_{x\to0^+}\log_ax=-\infty$
		- $\lim_{x\to c}\log_ax=\log_ac$
	- $0<a<1$
		- $\lim_{x\to+\infty}\log_ax=-\infty$
		- $\lim_{x\to0^+}\log_ax=+\infty$
		- $\lim_{x\to c}\log_ax=\log_ac$
- **Funzioni Trigonometriche:**
	- $\lim_{x\to\pm\infty}\sin x = \nexists$  (analogo per $\cos x$)
	- $\lim_{x\to c}\sin x=\sin c$ (analogo per $\cos x$)
	- $\lim_{x\to\frac{\pi}{2}^-}\tan x=+\infty$ 
	- $\lim_{x\to\frac{\pi}{2}^+}\tan x=-\infty$ 
	- $\lim_{x\to\pm\infty}\arctan x=\pm\frac{\pi}{2}$  
### Operazioni e Forme Indeterminate
$$\lim_{x\to+\infty}\frac{x^p}{a^x}=0 \ \ \ \ \ \ \ \ \ \ \ p>0, a>1$$
$$\lim_{x\to-\infty}|x^p|a^x=0 \ \ \ \ \ \ \ \ \ \ \ p>0, a>1$$
$$\lim_{x\to+\infty}x^pa^x=0 \ \ \ \ \ \ \ \ \ \ \ p>0, 0<a<1$$
$$\lim_{x\to-\infty}\frac{a^x}{|x|^p}=+\infty \ \ \ \ \ \ \ \ \ \ \ p>0, 0<a<1$$
$$\underset{\text{usando il cambio di variabile } y=\log_ax}{\lim_{x\to+\infty}\frac{\log_ax}{x^p}=0} \ \ \ \ \ \ \ \ \ \ \ p>0, a>1$$
### Limiti Notevoli
Sapendo che
$$\lim_{n\to+\infty}\Big(1+\frac{1}{n}\Big)^n=e\ \ \ \ \ (n\in\mathbb{N})$$
Si può mostrare che 
$$\lim_{x\to\pm\infty}\Big(1+\frac{1}{x}\Big)^x=e \ \ \ \ \ \ (x\in\mathbb{R}\setminus\{0\})$$
Ponendo $y=\frac{1}{x}$ si ottiene
$$\lim_{x\to0}(1+x)^\frac{1}{x}=e$$
Applicando $\log$ da entrambe le parti si ha che
$$\lim_{x\to0}\log\Big[(1+x)^\frac{1}{x}\Big]=1\Leftrightarrow\lim_{x\to0}\frac{\log(1+x)}{x}=1$$
Partendo da quest'ultimo e ponendo $y=\log(1+x)$ si può trovare:
$$\lim_{y\to0}\frac{y}{e^y-1}=1\Leftrightarrow\lim_{y\to0}\frac{e^y-1}{y}=1$$
$\sin x$ e $\cos x$ non ho voglia di farli

### o-Piccoli
Siano $f,g:I\to\mathbb{R}, c\in[\inf I, \sup I]$
Diciamo che $f$ è trascurabile rispetto a $g$ e scriviamo $f(x)=o(g(x))$ per $x\to c$ se
$$\lim_{x\to c}\frac{f(x)}{g(x)}=0$$
Riscriviamo i limiti notevoli usando gli o-piccoli
$$\begin{split}&\lim_{x\to0}\frac{\log(1+x)}{x}=1\\&\Leftrightarrow\frac{\log(1+x)-x}{x}=0\\&\Leftrightarrow\log(1+x)-x=o(x)\ \ \ \ \text{ per } x\to0\\&\Leftrightarrow\log(1+x)=x+o(x)\ \ \ \ \text{ per } x\to0\end{split}$$
$$\begin{split}&\lim_{x\to0}\frac{e^x-1}{x}=1\\&\Leftrightarrow\lim_{x\to0}\frac{e^x-1-x}{x}=0\\&\Leftrightarrow e^x-1-x=o(x)\ \ \ \ \text{ per }x\to0\\&\Leftrightarrow e^x=1+x+o(x)\ \ \ \ \text{ per }x\to0\end{split}$$
