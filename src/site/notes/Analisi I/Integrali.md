---
{"dg-publish":true,"permalink":"/analisi-i/integrali/"}
---

Sia $f\colon [a, b] \to \mathbb{R}$ limitata e $\mbox{t.c.} \ f(x)\geq0 \ \forall x \in [a,b]$ chiamiamo **sottografico** di $f$ l'insieme:
$$ \Gamma_{f} = \{\ (x,y) \in \mathbb{R}\times\mathbb{R} \mid x \in [a,b], 0\leq y \leq f(x)\ \} $$
 Osserviamo che:
 $$\underbrace{(b-a)\inf_{[a,b]} f}_\text{area} \leq \text{Area}(\Gamma_f) \leq \underbrace{(b-a)\sup_{[a,b]}f}_\text{area}$$
Analogamente, se suddivido $[a,b]$ in $n$ parti uguali $[x_{i-1}, x_i]$, posso dire che:
 $$\sum_{i=1}^n{(x_i-x_{i-1})} \inf_{[x_{i-1}, x_i]}f\leq \text{Area}(\Gamma_f)\leq \sum_{i=1}^n{(x_i-x_{i-1})} \sup_{[x_{i-1}, x_i]}f$$
 
## Integrale di Funzioni Continue (Riemann)
Sia $f:[a,b]\to\mathbb{R}$ continua, suddivido $[a,b]$ in $n$ intervalli della forma $[x_{i-1}, x_i]$ dove<
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

### Teorema - Media Integrale #teor 
Sia $f\in C([a,b],\mathbb{R})$, allora:
1) 
$$\underset{[a,b]}\min f\le\underbrace{\frac{1}{b-a}\int_a^bf(x)\,dx}_{\text{media integrale}}\le\underset{[a,b]}\max f$$
2) $\exists c\in[a,b]:$
$$\frac{1}{b-a}\int_a^bf(x)\,dx=f(c)$$
##### Dimostrazione #dim 
###### 1)
$\max f$ e $\min f$ esistono per il [[Analisi I/Continuità#Teorema di Weierstrass teor\|teorema di Weierstrass]]
Si ha:
	$$\begin{split}\int_a^b\underset{[a,b]}\min{f}\,dx&\le\int_a^bf(x)\,dx\le\int^b_a\underset{[a,b]}\max{f}\,dx\\=(b-a)\cdot\underset{[a,b]}\min{f}&\le\int_a^bf(x)\,dx\le(b-a)\cdot\underset{[a,b]}\max{f}\end{split}$$
	divido per $(b-a)$ e ottengo $1$

###### 2)
Dal punto 1) so che:
$$\underset{[a,b]}\min{f}\le\frac{1}{b-a}\int_a^bf(x)dx\le\underset{[a,b]}\max{f}$$
D'altra parte, per il [[Analisi I/Continuità#Teorema dei Valori Intermedi teor\|teorema dei valori intermedi]] ho che:
$$\begin{split}\underbrace{f([a,b])}_{\text{insieme immagine}}=\Big[\underset{[a,b]}\min{f},\underset{[a,b]}\max{f}\Big]\\\Rightarrow\frac{1}{b-a}\int_a^bf(x)\,dx\in f([a,b])\end{split}$$
Cioè
$$\exists c\in[a,b]\mbox{ t.c. } f(c)=\frac{1}{b-a}\int^b_af(x)\,dx$$
### Teorema Fondamentale del Calcolo Integrale I #teor 
Sia 
$$f\in \underbrace{C^1([a,b],\mathbb{R})}_{=\Big\{f:[a,b]\to\mathbb{R} \text{ derivabile e t.c. } f'\text{ continua}\Big\}}$$
Allora:
$$\int_a^bf'(x)\,dx=f(b)-f(a)$$
#### Dimostrazione #dim 
Ricordiamo la definizione di integrale:
Suddivido $[a,b]$ in $n$ sotto-intervalli:
$$[x_{i-1},x_i]\text{ con }\begin{cases}x_0=a\\x_n=b\end{cases}\ \ \ \ \ x_i-x_{i-1}=\frac{b-a}{n}$$
Si ha che:
$$f(b)-f(a)=\sum^n_{i=1}\Big(f(x_i)-f(x_{i-1})\Big)$$
Per il [[Analisi I/Calcolo Differenziale#Teorema - Lagrange teor\|teorema di Lagrange]]: $\exists c_i\in[x_{i-1},x_i]$ t.c.
$$f(b)-f(a)=\sum_{i=1}^n\Big(f(x_i)-f(x_{i-1})\Big)=\underbrace{\sum_{i=1}^nf'(c_i)(x_i-x_{i-1})}_{\text{def Somma di Riemann}=S_R(f',c_1,...,c_n)}$$
Passando al limite per $n\to\infty$, concludo
$$f(b)-f(a)=\int_a^bf'(x)\,dx$$
#### Definizione - Primitiva #def 
Sia $f\in C([a,b],\mathbb{R})$
Diciamo che $F:[a,b]\to\mathbb{R}$ è una **primitiva** di $f$ se 
$$F'(x)=f(x)\ \ \forall x\in[a,b]$$
Posso scrivere il teorema fondamentale del calcolo come:
> Sia $f\in C([a,b],\mathbb{R})$ e sia $F$ una sua primitiva, allora:
> $$\int_a^bf(x)\,dx=F(b)-F(a)$$

### Teorema - Integrazione per Parti #teor 
Sia $F$ una primitiva di $f$
Allora:
$$\int_a^bf(x)\cdot g(x)\,dx=\Big[F(x)\cdot g(x)\Big]_a^b-\int_a^xF(x)\cdot g'(x)\,dx$$
#### Dimostrazione #dim
Considero
$$(Fg)'(x)=F'(x)g'(x)+F(x)g'(x)$$
Integro:
$$\underbrace{\int_a^bf(x)g(x)\,dx}_{\Big[F(x)g(x)\Big]_a^b}=\int_a^b\overbrace{F'(x)}^{f(x)}g(x)\,dx+\int_a^bF(x)g'(x)\,dx$$

### Teorema - Integrazione per Sostituzione #teor 
Siano $I,J$ intervalli di $\mathbb{R}, f\in C(I,\mathbb{R}),\varphi\in C^1(J,I)$ 
Allora:
1) Se $\alpha,\beta\in J$:
$$\int_\alpha^\beta f(\varphi(t))\cdot\varphi'(t)\,dt=\int_{\varphi(\alpha)}^{\varphi(\beta)}f(x)\,dx$$
2) Se $\varphi:J\to I$ è invertibile, siano $a,b\in I$
$$\Rightarrow\int_a^bf(x)\,dx=\int_{\varphi^{-1}(a)}^{\varphi^{-1}(b)}f(\varphi(t))\varphi'(d)\,dt$$

#### Dimostrazione #dim
###### 1)
Sia $F$ una primitiva di $f$ (che esiste per il II teorema fondamentale)
Considero $F\circ\varphi$ e la derivo:
$$(F\circ\varphi)'(t)=F'(\varphi(t))\cdot\varphi'(t)=f(\varphi(t))\cdot\varphi'(t)$$
Integro tra $\alpha$ e $\beta$:
$$\int_{\varphi(\alpha)}^{\varphi(\beta)}f(x)\,dx\underset{*}{=}F(\varphi(\beta))-F(\varphi(\alpha))\underset{*}{=}\int_\alpha^\beta (F\circ\varphi)'(t)\,dt=\int_\alpha^\beta f(\varphi(t))\cdot\varphi'(t)\,dt$$
[[Analisi I/Integrali#Teorema Fondamentale del Calcolo Integrale I teor\|* teorema fondamentale del calcolo integrale I]]
### Teorema Fondamentale del Calcolo Integrale II
Sia $f:[a,b]\to\mathbb{R}$ continua
Sia $F(x)=\int_a^xf(t)\,dt$ funzione integrale
Allora $F$ è derivabile e $F'(c)=f(c)\ \ \ \forall c\in[a,b]$
#### Dimostrazione #dim
Sia $c\in[a,b]$
$$\lim_{x\to c}\frac{F(x)-F(c)}{x-c}=\lim_{x\to c}\frac{\int_a^xf(t)\,dt-\int_a^cf(t)\,dt}{x-c}=\lim_{x\to c}\underbrace{\frac{\int_c^xf(t)\,dt}{x-c}}_\text{media integrale}$$
Per il [[Analisi I/Integrali#Teorema - Media Integrale teor\|teorema della media integrale]]:
$$\exists d_x\in\underset{\text{o }(x,c)}{(c,x)}\mbox{ t.c. }\frac{1}{x-c}\int_c^xf(t)\,dt=f(dx)$$
Passando al limite
$$\lim_{x\to c}\frac{F(x)-F(c)}{x-c}=\lim_{x\to c}\frac{1}{x-c}\int_c^xf(t)\,dt=\lim_{x\to c}f(dx)$$
### Integrazione di Funzioni Razionali
$$\int_a^b\frac{P_n(x)}{Q_m(x)}\,dx\ \ \ \ \ \text{ dove }\ \ \ \ \ \begin{split}&P_n(x)=\text{polinomio di grado }n\\ &Q_m(x)=\text{polinomio di grado }m\end{split}$$
Consideriamo solo il caso $m>n$ (perché altrimenti si fa la divisione tra polinomi)
Studiamo in particolare il caso $m=2,n<2$
Dato $Q_2(x)=ax^2+bx+c$, ho 3 possibili casi:
1) $\Delta=b^2-4ac>0$ ($Q$ ha 2 radici distinte)
2) $\Delta=0$
3) $\Delta=b^2-4ac<0$ ($Q$ non si scompone)
#### Caso $\Delta>0$ 
$$\int_4^5\frac{x+1}{x^2-4x+3}\,dx$$
Osservo che $x^2-4x+3=(x-3)(x-1)$
Cerco $A,B\in\mathbb{R}$ t.c.
$$\frac{x+1}{(x-3)(x-1)}=\frac{A}{x-3}+\frac{B}{x-1}$$
Si ha:
$$\begin{split}
&\frac{x+1}{(x-3)(x-1)}=\frac{A(x-1)+B(x-3)}{(x-3)(x-1)}\\
\Leftrightarrow \ &x+1=Ax-A+Bx-3B\\
\Leftrightarrow \ &x+1=x(A+B)-A-3B\\
\Leftrightarrow \ &\begin{cases}A+B=1\\-A-3B=1\end{cases}\Leftrightarrow\ \begin{cases}A=1-B\\-2B=2\end{cases}\Leftrightarrow\begin{cases}A=2\\ B=-1\end{cases}
\end{split}$$
Quindi:
$$\int_4^5\frac{x+1}{(x-3)(x-1)}\,dx=\int_4^5\frac{2}{x-3}\,dx-\int_4^5\frac{1}{x-1}\,dx=\Big[2\log(x-3)-log(x-1)\Big]_4^5$$
#### Caso $\Delta=0$ 
$$\int_1^2\frac{x+1}{x^2-6x+9}\,dx=\int_1^2\frac{x+1}{(x-3)^2}\,dx$$
Pongo $t=x-3, dt=dx$
$$\int_{-2}^{-1}\frac{t+4}{t^2}\,dt=\int_{-2}^{-1}\Big(\frac{1}{2}+\frac{4}{t^2}\Big)=\Big[\log|t|-\frac{4}{t}\Big]_{-2}^{-1}$$
#### Caso $\Delta<0$ 
$$\int_1^2\frac{2x+1}{2+x^2}\,dx=\int_1^2\Big(\underbrace{\frac{2x}{2+x^2}}_{\Big[\log(2+x^2)\Big]_1^2}+\underbrace{\frac{1}{2+x^2}}_*\Big)$$
$*$:
$$\int_1^2\frac{1}{2+x^2}\,dx=\int_1^2\frac{1}{2}\Big(\frac{1}{1+(\frac{x}{\sqrt{2}})^2}\Big)\,dx=\int_1^2\frac{1\cdot\sqrt{2}}{2}\Big(\frac{1\cdot\frac{1}{\sqrt{2}}}{1+(\frac{x}{\sqrt{2}})^2}\Big)\,dx=\Big[\frac{\sqrt{2}}{2}\arctan(\frac{x}{\sqrt{2}}\Big]_1^2$$
