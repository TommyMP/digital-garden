---
{"dg-publish":true,"permalink":"/analisi-i/funzione-esponenziale/","dgPassFrontmatter":true}
---

### Definizione #def 
Sia $a\in\mathbb{R^+}\setminus\{0,1\}$, chiamiamo **funzione esponenziale** in base $a$ la funzione
$$\exp_a:\begin{array}.\mathbb{R}\longrightarrow\mathbb{R}\\ x\to a^x\end{array}$$
### Proprietà
- $a^x>0\ \ \forall x \in \mathbb{R}$
- $a^{x+y}=a^x\cdot a^y \ \ \forall x,y\in\mathbb{R}$
- $(a^x)^y=a^{xy}\ \ \forall x,y\in\mathbb{R}$
- $a,b\in\mathbb{R^+}\setminus\{0,1\}\ \ \ \ a^x\cdot b^x=(ab)^x \ \ \forall x\in\mathbb{R}$
- se $a>1$           $\exp_a$ è strettamente $\nearrow$
- se $0<a<1$    $\exp_a$ è strettamente $\searrow$
- $\text{exp}_a:\mathbb{R}\xrightarrow{\textsf{S}}\mathbb{R^+}\setminus\{0\}$ è invertibile 
# Funzione Logaritmica
### Definizione #def 
Sia $a\in\mathbb{R^+}\setminus\{0,1\}$, chiamiamo **logaritmo** $m$ base $a$, la funzione inversa di $\text{exp}_a$ e la indico con
$$\log_a:=(\exp_a)^{-1}$$$\Big[\log_a:\mathbb{R^+}\setminus\{0\}\xrightarrow{\textsf{B}}\mathbb{R}\Big]$$
### Proprietà
- $\log_a(x\cdot y)=\log_ax+\log_ay\ \ \ \ \forall x,y\in\mathbb{R^+}\setminus\{0\}$ 
- $\log_a\Big(\frac{x}{y}\Big)=\log_ax-\log_ay\ \ \ \ \forall x,y\in\mathbb{R^+}\setminus\{0\}$ 
- $\log_ax^\alpha=\alpha\log_ax\ \ \ \ \forall\alpha\in\mathbb{R}$
- se $a>1$           $\log_a$ è strettamente $\nearrow$
- se $0<a<1$    $\log_a$ è strettamente $\searrow$
### Dimostrazione (proprità 1) #dim 
Voglio dimostrare che $log_a(x\cdot y)=\log_ax+\log_ay$
Infatti: 
$$\begin{split}a^{\log_a{xy}}&=xy=a^{\log_ax}\cdot a^{\log_ay}\\&=a^{\log_ax+\log_ay}\end{split}$$ Poiché $\exp_a$ è iniettiva $\Rightarrow \log_a(x\cdot y)=\log_ax+\log_ay$
### Formula Cambio Base
$$\log_b{y}=\frac{\log_ay}{\log_ab}$$
