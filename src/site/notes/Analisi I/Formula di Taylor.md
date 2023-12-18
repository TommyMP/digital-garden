---
{"dg-publish":true,"permalink":"/analisi-i/formula-di-taylor/"}
---

### Definizione - Ordinata di Ordine C #def 
Sia $f:I\to\mathbb{R},c\in I$
diciamo che $f$ è derivabile $n$ volte in $c$ se la derivata di ordine $(n-1)$ è derivabile in $c$, e indichiamo con $f^{(n)}(c)$ la derivata in $c$
### Definizione - Polinomio di Taylor #def
Sia $I$ intervallo di $\mathbb{R}, f:I\to\mathbb{R},c\in I,n\in\mathbb{N}$
Supponiamo che $f$ sia derivabile $n$ volte
Chiamiamo **polinomio di Taylor** di $f$ di punto iniziale $c$ e ordine $n$, il polinomio:
$$T_{c,n}(x)=\sum_{k=0}^n\frac{f^{(k)}(c)}{k!}(x-c)^k$$

### Teorema - Formula di Taylor con Resto di Peano #teor
Sia $I$ intervallo di $\mathbb{R}, f:I\to\mathbb{R},c\in I,n\in\mathbb{N}$
Se $f$ è derivabile $n$ volte, allora:
$$f(x)=\underbrace{\sum_{k=0}^n\frac{f^{(k)}(c)}{k!}(x-c)^k}_{T_{c,n}(x)}+o(x-c)^n$$
##### Dimostrazione - Caso $c=0,n=2$ #dim 
Voglio dimostrare che, se $f$ è derivabile $2$ volte, allora
$$f(x)=f(0)+f'(0)\cdot x+\frac{f''(0)}{2}x^2+o(x^2)\ \ \ \ \text{ per }x\to0$$
Sia $R(x)$ la funzione **resto**:
$$R(x)=f(x)-f(0)-f'(0)x-\frac{f''(0)}{2}x^2$$
**Scopo:** $R(x)=o(x^2)$ per $x\to0$
Calcolo $R'(x)$
$$R'(x)=f'(x)-f'(0)-f''(0)x$$
Poiché $f$ è derivabile 2 volte, si ha che $f'$ è derivabile 1 volta, e dunque posso applicare il [[Analisi I/Calcolo Differenziale#Teorema - Caratterizzazione teor\|teorema di caratterizzazione]] a $f'$
$$f'(x)=f'(0)+f''(0)x+o(x)\ \ \ \ \ \text{ per }x\to0$$
$$\begin{split}R'(x)&=f'(0)+f''(0)x+o(x)-f'(0)-f''(0)x\\ &\Rightarrow R'(x)=o(x)\ \ \ \ \ \ \ \ \text{ per }x\to0\end{split}$$
Ora applico il [[Analisi I/Calcolo Differenziale#Teorema - Lagrange teor\|teorema di Lagrange]] a $R(x)$ nell'intervallo $[0,x]$
$$\exists d_x\in(0,x)\mbox{ t.c. } \frac{R(x)-R(0)}{x}=R'(d_x)$$
Divido per $x$
$$\frac{R(x)-\overbrace{R(0)}^0}{x^2}=\frac{R'(d_x)}{x}$$
Dunque
$$0\le\Big|\frac{R(x)}{x^2}\Big|=\Big|\frac{R'(d_x)}{x}\Big|\underbrace{\le}_{\text{poiché }|x|>|d_x|}\underbrace{\Big|\frac{R'(d_x)}{x}\Big|}_{0\text{ per }x\to0}$$
Per il [[Analisi I/Limiti#Teorema - Dei 2 Carabinieri teor\|teorema dei due carabinieri]] deduco che
$$\frac{R(x)}{x^2}\underset{x\to0}{\longrightarrow}0$$
### Formule di Taylor di Funzioni Elementari
per $x\to0$:
$$e^x\sum^n_{k=0}\frac{1}{k!}+o(x^n)=1+x+\frac{x^2}{2}+\frac{x^3}{3!}+\frac{x^4}{4!}+\dots+\frac{x^n}{n!}+o(x^n)$$
$$\sin x=x-\frac{x^3}{3!}+\frac{x^5}{5!}-\frac{x^7}{7!}+\dots+(\pm1)\frac{x^{2n+1}}{(2n+1)!}+o(x^{2n+1})$$
$$\cos x=x-\frac{x^2}{2}+\frac{x^4}{4!}-\frac{x^6}{6!}+\dots+(\pm1)\frac{x^{2n}}{(2n)!}+o(x^{2n})$$
$$\begin{split}\log(1+x)&=f(0)+f'(0)x+\frac{f''(0)}{2}x^2+\frac{f^{(3)}(0)}{3!}x^3+\frac{f^{(4)}(0)}{4!}x^4+\frac{f^{(n)}(0)}{n!}x^n+o(x^n)\\&=x-\frac{x^2}{2}+\frac{x^3}{3}-\frac{x^4}{4}+\dots\pm\frac{x^n}{n}+o(x^n)\end{split}$$
##### Osservazione
Il polinomio di Taylor $T_{c,n}$ è l'unico polinomio con la seguente proprietà:
$$T_{c,n}^{(k)}(c)=f^{(k)}(c)\ \ \ \ \ \ \ \forall\ k=0,...,n$$