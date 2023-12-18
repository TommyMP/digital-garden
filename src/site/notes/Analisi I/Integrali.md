---
{"dg-publish":true,"permalink":"/analisi-i/integrali/"}
---

Sia $f\colon [a, b] \to \mathbb{R}$ limitata e $\mbox{t.c.} \ f(x)\geq0 \ \forall x \in [a,b]$ chiamiamo **sottografico** di $f$ l'insieme:
$$ \Gamma_{f} = \{\ (x,y) \in \mathbb{R}\times\mathbb{R} \mid x \in [a,b], 0\leq y \leq f(x)\ \} $$
 Osserviamo che:
 $$\underbrace{(b-a)\inf_{[a,b]} f}_\text{area} \leq \text{Area}(\Gamma_f) \leq \underbrace{(b-a)\sup_{[a,b]}f}_\text{area}$$
Analogamente, se suddivido $[a,b]$ in $n$ parti uguali $[x_{i-1}, x_i]$, posso dire che:
 $$\sum_{i=1}^n{(x_1-x_i)} \inf_{[x_{i-1}, x_i]}f\leq \text{Area}(\Gamma_f)\leq \sum_{i=1}^n{(x_1-x_i)} \sup_{[x_{i-1}, x_i]}f$$
 
## Integrale di Funzioni Continue (Riemann)
Sia $f[a,b]\to\mathbb{R}$ continua, suddivido $[a,b]$ in $n$ intervalli della forma $[x_{i-1}, x_i]$ dove:
 $$\begin{cases} x_0=a \\ x_n=b \\ x_i-x_{i-1} = \frac{b-a}{n} \end{cases}$$
 Sia $C_i\in[x_{i-1}, x_i] \forall i=1,\ldots,n$, chiamiamo **somma di Riemann** di $f$:
 $$S_R(f,c_1,c_2,\ldots,c_n)=\sum^n_{i=1}f(c_i)\underbrace{\frac{b-a}{n}}_{(x_i-x_{i-1})}$$
#### Teorema - Integrale #teor
Sia $f\colon[a,b]\to\mathbb{R}$ continua, allora

$$\exists \lim_{n\to+\infty} S_R(f,c_1,\ldots,c_n) \in \mathbb{R}$$
e non dipende dalla scelta dei $c_i$
{ #6570d0}

#### Definizione - Integrale #def
Chiamiamo [[Analisi I/Integrali#^6570d0 \|tale limite]] **integrale** di $f$ in $[a,b]$ e lo indichiamo con 
$$\int_a^bf(x)\,dx$$

#### Proprietà
Siano 
$$f,g\in\underbrace{C([a,b],\mathbb{R})}_{=\{f:[a,b]\to\mathbb{R}\text{ continue}\}}$$
Allora:
1) **Linearità:**
	- $\int_a^b(f(x)+g(x))\,dx=\int_a^bf(x)\,dx+\int_a^bg(x)\,dx$
	- Sia $k\in\mathbb{R}$: $\int_a^bkf(x)\,dx=k\int_a^bg(x)\,dx$
2) **Monotonia:**
	Supponiamo $f(x)\le g(x)\ \forall x\in[a,b]$
	$\Rightarrow\int_a^bf(x)\,dx\le\int_a^bg(x)\,dx$
3) **Additività:**
	Sia $c\in(a,b)$
	$\Rightarrow\int_a^bf(x)\,dx=\int_a^cf(x)\,dx+\int_c^bd(x)\,dx$
4) **Disuguaglianza Triangolare:**
	$\Big|\int_a^bf(x)\,dx\Big|\le\int_a^b|f(x)|\,dx$
###### Significato dell'integrale per $f$ che cambia segno
- **Osservazione:** per la proprietà di additività:
$$\begin{split}0&=\int_a^af(x)\,dx=\int_a^bf(x)\,dx+\int_b^af(x)\,dx\\&\Rightarrow\int_a^bf(x)\,dx=-\int_b^af(x)\,dx\end{split}$$
- Siano
	- $f^+(x)=\max\{0,f(x)\}$ parte positiva
	- $f^-(x)=\max\{0,-f(x)\}$ parte negativa
	Vale che:
	- $\rightarrow f(x)=f^+(x)-f^-(x)$
		per linearità: $\Rightarrow\int_a^bf(x)\,dx=\int_a^bf^+(x)\,dx-\int_a^bf^-(x)\,dx$
	- $\rightarrow |f(x)|=f^+(x)+f^-(x)$

#### Teorema - Media Integrale #teor 
Sia $f\in C([a,b],\mathbb{R})$, allora:
1) 
$$\underset{[a,b]}\min f\le\underbrace{\frac{1}{b-a}\int_a^bf(x)\,dx}_{\text{media integrale}}\le\underset{[a,b]}\max f$$
2) $\exists c\in[a,b]:$
$$\frac{1}{b-a}\int_a^bf(x)\,dx=f(c)$$
##### Dimostrazione #dim 
###### 1)
$\max f$ e $\min f$ esistono per il [[Analisi I/Continuità#Teorema di Weierstrass teor\|teorema di Weierstrass]]
Si ha:
	$$\begin{split}\int_a^b\underset{[a,b]}\min{f}\,dx&\le\int_a^bf(x)\,dx\le\int^b_a\underset{[a,b]}\max{f}\,dx\\=(b-a)\cdot\underset{[a,b]}\min{f}&\le\int_a^bf(x)\,dx\le\underset{[a,b]}\max{f}\end{split}$$
	divido per $(b-a)$ e ottengo $1$

###### 2)
Dal punto 1) so che:
$$\underset{[a,b]}\min{f}\le\frac{1}{b-a}\int_a^bf(x)dx\le\underset{[a,b]}\max{f}$$
D'altra parte, per il [[Analisi I/Continuità#Teorema dei Valori Intermedi teor\|teorema dei valori intermedi]] ho che:
$$\begin{split}\underbrace{f([a,b])}_{\text{insieme immagine}}=\Big[\underset{[a,b]}\min{f},\underset{[a,b]}\max{f}\Big]\\\Rightarrow\frac{1}{b-a}\int_a^bf(x)\,dx\in f([a,b])\end{split}$$
Cioè
$$\exists c\in[a,b]\mbox{ t.c. } f(c)=\frac{1}{b-a}\int^b_af(x)\,dx$$