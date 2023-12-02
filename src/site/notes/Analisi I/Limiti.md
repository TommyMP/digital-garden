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
Diciamo che $$\exists\lim_{x\to c}f(x)=l$$se $$\forall(a_n)_{n\in\mathbb{N}}\text{ successione in } I\setminus\{c\} \mbox{ t.c. } a_n\xrightarrow[n\to+\infty]{}c \ \ \ \text{ si ha } \ \ \ f(a_n)\to l$$
- **convergente:** $l\in\mathbb{R}$
- **divergente:** $l=\pm\infty$
- **infinitesima:** $l=0$

## Definizione 2 (intorno) - Limite #def
Sia $I$ intervallo o intervallo forato,
Sia $f:I\to\mathbb{R}$, sia $c\in\Big[\inf I, \sup I\Big]$,
$l\in\overline{\mathbb{R}}$.
Diciamo che $$\exists\lim_{x\to c}f(x)=l$$se $$\forall\ V \text{ intorno di } l,\exists\ U_V \text{ intorno di } c \mbox{ t.c } \forall x\in U_V\setminus\{0\}\ \ \text{ si ha }\ \ f(x)\in V$$
##### Osservazione
Esempio caso $l,c\in\mathbb{R}$ $$\forall\varepsilon>0,\exists\delta_\varepsilon>0\mbox{ t.c. se } \underset{(x\neq0)}{|x-c|}<\delta_\varepsilon\ \ \ \text{ si ha } \ \ \ |f(x)-l|<\varepsilon$$ 
> $\varepsilon$ è il raggio dell'intorno di $l$
> $\delta_\varepsilon$ è il raggio dell'intorno di $c$

