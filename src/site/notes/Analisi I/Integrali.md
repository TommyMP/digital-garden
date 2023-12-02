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
Sia $f\colon[a,b]\to\mathbb{R}$ continua, allora $$\exists \lim_{n\to+\infty} S_R(f,c_1,\ldots,c_n) \in \mathbb{R}$$e non dipende dalla scelta dei $c_i$
{ #6570d0}

#### Definizione - Integrale #def
Chiamiamo [[Analisi I/Integrali#^6570d0 \|tale limite]] **integrale** di $f$ in $[a,b]$ e lo indichiamo con $$\int_a^bf(x)dx$$
 