---
{"dg-publish":true,"permalink":"/analisi-i/numeri-complessi/"}
---

Insieme dei numeri complessi $\mathbb{C}$

$$\mathbb{C}=\mathbb{R}\times\mathbb{R}=\mathbb{R}^2$$
$$=\Big\{(a,b)\mid a\in\mathbb{R},b\in\mathbb{R}\Big\}$$
dotato delle seguenti operazioni:
- $(a,b)+(c,d):=(a+c,b+d)$
- $(a,b)\cdot(c,d):=(ac-bd,ad+bc)$

- **elemento neutro** di $+$ è $(0,0)$
- **elemento neutro** di $\cdot$ è $(1,0)$
- **opposto** per $+$ è $(-a,-b)$
- **opposto** per $\cdot$ è $(\frac{a}{a^2+b^2},-\frac{b}{a^2+b^2})$

- Posso identificare: $(a,0)\leftrightarrow a$
- Osservazione: $(0,1)\cdot(0,1)=\underbrace{(-1,0)}_{-1}$ 
	Quindi ho trovato che $(0,1)^2=-1$ 
	chiamo $(0,1)$ **unità immaginaria** e la indico con $i$
#### Forma Algebrica:
$z\in\mathbb{C}$
$z=(a,b)=a\underbrace{(1,0)}_1+b\underbrace{(0,1)}_i=a+ib$
$a$: parte reale, $b$: parte immaginaria
##### Coniugato e Modulo
$z=a+ib$
**Coniugato:** $\overline{z}=a-ib$
- $\text{Re}z=\frac{z+\overline{z}}{2}=a$    
- $\text{Im}z=\frac{z-\overline{z}}{2i}=b$    
- $\overline{z_1}+\overline{z_2}=\overline{z_1+z_2}$
- $\overline{z_1}\cdot\overline{z_2}=\overline{z_1\cdot z_2}$
- $z\cdot\overline{z}=(a+ib)(a-ib)=a^2+b^2$
- $\underbrace{|z|}_{\text{modulo}}=\sqrt{z\cdot\overline z}=\sqrt{a^2+b^2}$
###### Proprietà
- $|z|\ge0, |z|=0\Leftrightarrow z=0$ù
- $|z|=|\overline{z}|$
- disuguaglianza triangolare:
	- $|z_1+z_2|\le|z_1|+|z_2|$
	- $|z_1-z_2|\ge||z_1|-|z_2||$

#### Forma Trigonometrica
Introduciamo le coordinate polari: $(\rho,\theta)$ con $\rho\in\mathbb{R^+},\theta\in[0,2\pi)$
![Pasted image 20231208122054.png](/img/user/Pasted%20image%2020231208122054.png)

$\begin{cases}a=\rho\cdot\cos\theta\\ b=\rho\cdot\sin\theta\end{cases}$
$|z|=\rho=\sqrt{a^2+b^2}$
$\theta=\underbrace{\text{arg}z}_\text{argomento principale}$
$$\begin{cases}\cos\theta=\frac{a}{\sqrt{a^2+b^2}}\\ \sin\theta=\frac{b}{\sqrt{a^2+b^2}}\end{cases}\Rightarrow\tan\theta=\frac{b}{a}$$
#### Formule di De Moivre

$$z_1=\rho_1(\cos\theta_1+i\sin\theta_i),\ \ z_2=\rho_2(\cos\theta_2+i\sin\theta_2)$$

$$\begin{split}z_1\cdot z_2&=\rho_1\rho_2(\cos\theta_1\cos\theta_2-\sin\theta_1\sin\theta_2+i(\sin\theta_1\cos\theta_2+\cos\theta_1+\sin\theta_2))\\&=\rho_1\rho_2(\cos(\theta_1,\theta_2)+i\sin(\theta_1+\theta_2))\end{split}$$
Cioè $|z_1\cdot z_2|=|z_1|\cdot|z_2|$
$\arg{(z_1\cdot z_2)}=\arg{z_1}+\arg{z_2}$
#### Notazione
$\rho(\cos\theta+i\sin\theta)=\rho e^{i\theta}$
$z_1=\rho_1e^{i\theta_1},\ z_2=\rho_2e^{i\theta_2}\Rightarrow z_1\cdot z_2=\rho_1\cdot\rho_2\cdot\underbrace{e^{i\theta_1}\cdot e^{i\theta_2}}_{e^{i(\theta_1+\theta_2)}}$
**Osservazione:** $-1=e^{i\pi}\Leftrightarrow e^{i\pi}+1=0$
## Radici N-Esime
Sia $\omega\in\mathbb{C}$, chiamo **radice n-esima** di $\omega$ una qualsiasi soluzione $z$ dell'equazione: $z^n=\omega\ \ \ (n\in\mathbb{N})$
Voglio risolverla:
	Sia $\omega=r(\cos\varphi+i\sin\varphi)=re^{i\varphi}$
	Sia $z=\rho e^{i\theta}\Rightarrow z^n=\rho^ne^{in\theta}$
	Dunque, devo imporre
	$\underbrace{z_k}_\text{soluzione}=\begin{cases}\rho^n=r\\ n\theta_k=\varphi+2k\pi\end{cases}\ \ \ \ \ k=0,...,n-1$
	$= \begin{cases}\rho^n=r\\\theta_k=\frac{\varphi+2k\pi}{n}\end{cases}\ \ \ \ \ k=0,...,n-1$
	Sono $n$ soluzioni $z_0,z_1,...,z_{n-1}$
**Osservazione:** vale sempre che le radici n-esime di $\omega$ sono i vertici di un poligono regolare di n-lati inscritto in una circonferenza di raggio $\sqrt[n]{|\omega|}$
