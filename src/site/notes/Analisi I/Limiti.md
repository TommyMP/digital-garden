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

## Teorema - Dei 2 Carabinieri/Confronto #teor 
Sia $I$ intervallo o intervallo forato di $\mathbb{R}$,
$f,g,h:I\to\mathbb{R}, c\in[\inf{I},\sup{I}], l\in\mathbb{R}$
Se $\lim_{x\to c}f(x)=l$ e $\lim_{x\to c}h(x)=l$
e $\exists$ un intorno $U$ di $c\mbox{ t.c. } f(x)\le g(x)\le h(x) \ \ \ \forall x \in U\cap I\setminus\{c\}$ allora: $\lim_{x\to c}g(x)=l$
