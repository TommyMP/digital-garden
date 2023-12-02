---
{"dg-publish":true,"permalink":"/analisi-i/successioni/"}
---


#### Definizione #def
Sia $A\neq \varnothing$, chiamiamo **successione in $A$** una qualsiasi funzione $f\colon \to A$.
$$\underbrace{a_n}_{\text{termine della successione}}:= a(n)$$
## Limite di Successione
#### Definizione - Successione Infinitesima #def
Sia $(a_n)_{n\in \mathbb{N}}$ una successione in $\mathbb{R}$, diciamo che $(a_n)_{n\in \mathbb{N}}$ è **infinitesima** (o che tende a 0) per $$n\to +\infty \text{ se } \forall \varepsilon \in \mathbb{R^+} \setminus \{0\}, \exists m_\varepsilon \in \mathbb{N} \mbox{ t.c. } \forall n \ge m_\varepsilon \text{ si ha } |a_n|\leq \varepsilon$$
##### Esempio
$a_n=\frac{1}{n}$, verifichiamo che $$\lim_{n\to +\infty} \frac{1}{n}=0$$ Devo verificare che $$\forall \varepsilon \in \mathbb{R^+} \setminus \{0\}, \exists m_\varepsilon \in \mathbb{N} \mbox{ t.c. } \forall n\ge m_\varepsilon \text{ si ha } |\frac{1}{n}|\leq \varepsilon$$
Posso scegliere $m_\varepsilon = [\frac{1}{\varepsilon}]+1$ 
#### Definizione - Limite di Successione #def
Sia $(a_n)_{n\in\mathbb{N}}$, sia $l\in\mathbb{R}$, diciamo che 
$$
\begin{align*}
a_n\longrightarrow l \ \\
n\to +\infty
\end{align*}
$$
$$\Big(\lim_{n\to+\infty} a_n = l\Big)$$
Se $$\forall \varepsilon>0, \exists m_\varepsilon \in \mathbb{N} \mbox{ t.c. } |a_n-l|\le\varepsilon \ \forall n\ge m_\varepsilon$$
#### Teorema - Unicità del Limite #teor
Sia $(a_n)_{n\in \mathbb{N}}$ in $\mathbb{R}$, siano $l,m\in\mathbb{R}$, supponiamo 
$$
\begin{array}
\ a_n\longrightarrow l \\
n\to +\infty
\end{array} \ \ \ \ \ \text{ e } \ \ \ \ \
\begin{array}
\ a_n\longrightarrow l \\
n\to +\infty
\end{array}
$$
Allora $l=m$
###### Dimostrazione #dim
Per ipotesi, ho che: 
$$\forall\varepsilon>0,\exists p_\varepsilon\in\mathbb{N}\mbox{ t.c. } |a_n-l|\le\varepsilon \ \forall n \ge p_\varepsilon$$
$$\forall\varepsilon>0,\exists q_\varepsilon\in\mathbb{N}\mbox{ t.c. } |a_n-m|\le\varepsilon \ \forall n \ge q_\varepsilon$$
Sia $n\ge\max\{p_\varepsilon,q_\varepsilon\}$ 
$$|l-m| = |l-a_n+a_n-m|\le^*\underbrace{|l-a_n|}_{\leq\varepsilon}+\underbrace{|a_n-m|}_{\leq\varepsilon} \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \forall\varepsilon>0$$ [[Analisi I/Operazioni#Modulo / Valore Assoluto\|*Proprietà del Modulo]]
$$\Rightarrow |l-m|\le2\varepsilon$$
Da ciò si deduce che deve essere necessariamente $l=m$, infatti se fosse $|l-m|>0$, potrei trovare $\varepsilon>0 \mbox{ t.c } |l-m|>\varepsilon$ 
**Osservazione:** $$\text{Sia }(a_n)_{n\in \mathbb{N}} \mbox{ t.c. } \begin{array}\ a_n\longrightarrow l \\ n\to +\infty\end{array} \ , \  (l\in\mathbb{R}) \text{ Allora } \ \begin{array}\ |a_n|\longrightarrow |l| \\ n\to +\infty\end{array}$$ Ma non è vero che $$\text{se }\begin{array}\ |a_n|\longrightarrow |l| \\ n\to +\infty\end{array}\ \text{ Allora } \ \begin{array}\ a_n\longrightarrow l \\ n\to +\infty\end{array}$$

#### Definizione - Limite di Successione a $\pm\infty$ #def
$$\lim_{n\to+\infty}a_n=+\infty \text{ se } \forall k\in\mathbb{R},\exists m_k\in\mathbb{N}\mbox{ t.c. } a_n\ge k \ \forall n\ge m_k$$
$$\lim_{n\to+\infty}a_n=-\infty \text{ se } \forall k\in\mathbb{R},\exists m_k\in\mathbb{N}\mbox{ t.c. } a_n\le k \ \forall n\ge m_k$$

#### Classificazione delle successioni in base al limite
- Se  $\begin{array}. a_n\to\pm\infty \\ n\to\infty\end{array}\Rightarrow$ **DIVERGENTE**
- Se  $\begin{array}. a_n\to l \\ n\to\infty\end{array}, l\in\mathbb{R} \Rightarrow$ **CONVERGENTE**

$a_n$ si dice **REGOLARE** se ha limite (conv/div)
Denoto l'insieme di tutti i possibili limiti di successioni:  $\overline{\mathbb{R}} = \mathbb{R} \cup \{+\infty,-\infty\}$  

#### Successioni Limitate/Illimitate
##### Definizione #def 
Sia $(a_n)_{n\in \mathbb{N}}$ in $\mathbb{R}$, diciamo che $a_n$ è limitata se lo è l'insieme dei suoi termini.
Indichiamo:
- $\sup(a_n)_{n\in\mathbb{N}}:=\sup\{a_n\mid n\in\mathbb{N}\}$
- $\inf(a_n)_{n\in\mathbb{N}}:=\inf\{a_n\mid n\in\mathbb{N}\}$
##### Teorema - Relazione tra avere limite ed essere limitata #teor 
1) $(a_n)_{n\in\mathbb{N}}$ è **convergente** $\Rightarrow (a_n)_{n\in\mathbb{N}}$ è **LIMITATA**
2) $\begin{array}.a_n\longrightarrow+\infty \\ n\to+\infty\end{array}\Rightarrow a_n$ è **ILLIMITATA SUPERIORMENTE** (e limitata inferiormente)
2) $\begin{array}.a_n\longrightarrow-\infty \\ n\to+\infty\end{array}\Rightarrow a_n$ **è ILLIMITATA INFERIORMENTE** (e limitata superiormente)
**Osservazioni:**
- $a_n$ limitata $\nRightarrow a_n$ convergente ( es. $a_n=(-1)^n$ )
- $a_n$ illimitata superiormente $\nRightarrow \begin{array}.a_n\longrightarrow+\infty \\ n\to+\infty\end{array}$ ( es. $a_n=\begin{cases}n&\text{se }n \text{ pari}\\ 0&\text{se }n\text{ dispari}\end{cases}$    )
#### Teorema del Confronto #teor 
Siano $(a_n)_{n\in \mathbb{N}}, (b_n)_{n\in \mathbb{N}}$ **successioni regolari**,
siano $l,m \in \overline{\mathbb{R}} \mbox{ t.c }\begin{array}. a_n\longrightarrow l \\ n\to+\infty\end{array}\text{ , } \ \begin{array}. b_n\longrightarrow m \\ n\to+\infty \end{array}$  
	supponiamo $a_n\ge b_n \ \forall n\in\mathbb{N}$ allora $l\ge m$ 
##### Dimostrazione #dim
Consideriamo solo il caso $l, m \in \mathbb{R}$ poiché tutti gli altri casi si deducono usando il [[Analisi I/Successioni#Teorema teor\|teorema precedente]].
Voglio mostrare $l\ge m$.
Assumo per assurdo $l<m$
Scelgo $\varepsilon>0\mbox{ t.c. }l<l+\varepsilon<\frac{l+m}{2}<m-\varepsilon<m$
Ma per ipotesi:$$\exists p_\varepsilon\in\mathbb{N}\mbox{ t.c. }l-\varepsilon\le a_n\le l+\varepsilon \ \forall n\ge p_\varepsilon$$ $$\exists q_\varepsilon\in\mathbb{N}\mbox{ t.c. }m-\varepsilon\le b_n\le m+\varepsilon \ \forall n\ge q_\varepsilon$$Quindi $\forall n\ge\max\{p_\varepsilon,q_\varepsilon\}$ si ha:$$a_n\le l+\varepsilon<\frac{l+m}{2}<m-\varepsilon\le b_n \Rightarrow a_n<b_n$$che è una contraddizione poiché doveva essere $a_n\ge b_n$ 
#### Operazioni
Siano $(a_n)_{n\in \mathbb{N}}, (b_n)_{n\in \mathbb{N}},\ l,m\in\mathbb{R}$
supponiamo $\begin{array}. a_n\longrightarrow l \\ n\to+\infty\end{array}\text{ , } \ \begin{array}. b_n\longrightarrow m \\ n\to+\infty \end{array}$ 
Allora:
- $\begin{array}.a_n\pm b_n \longrightarrow l\pm m \\ n\to+\infty\end{array}$
- $\begin{array}.a_n\cdot b_n \longrightarrow l\cdot m \\ n\to+\infty\end{array}$
- $\begin{array}.\frac{a_n}{b_n} \longrightarrow \frac{l}{m} \\ n\to+\infty\end{array} \ \ \ b_n\neq0, m\neq0$
- $\Big[ \ \ \begin{array}.\frac{a_n}{b_n} \longrightarrow 0 \\ n\to+\infty\end{array} \ \ \text{ se } m=\pm\infty, l\in\mathbb{R}$  
- Se $l$ o $m$ sono $\pm\infty$, si ha $\begin{cases}+\infty+\infty=+\infty \\ -\infty-\infty=-\infty \\ l+\infty=+\infty \\ l-\infty=-\infty\end{cases}$
#### Forme Indeterminate
- $0\cdot\pm\infty$
- $\frac{0}{0}$
- $\frac{\pm\infty}{\pm\infty}$
- $a_n\to l, b_n\to0 \ \ \frac{a_n}{b_n}$ in generale non diverge (può convergere o non avere limite)

## Successioni Monotone
### Definizione #def
Sia  $(a_n)_{n\in \mathbb{N}}$ in $\mathbb{R}$:
- diciamo che $a_n$ è **CRESCENTE** se $a_n\le a_{n+1} \ \forall n\in\mathbb{N}$
- diciamo che $a_n$ è **DECRESCENTE** se $a_n\ge a_{n+1} \ \forall n\in\mathbb{N}$
**Osservazione:**
- Se $a_n \nearrow \ \Rightarrow$  $a_n$ è inferiormente limitata e $\inf{a_n}=a_0$
- Se $a_n\searrow \ \Rightarrow$  $a_n$ è superiormente limitata e $\sup{a_n}=a_0$

### Teorema - Limiti di Successioni Monotone #teor
Sia  $(a_n)_{n\in \mathbb{N}}$ in $\mathbb{R}$ monotona, allora $a_n$ è regolare.
Più precisamente:
1. Se $a_n\nearrow \ \Rightarrow \ \lim_{n\to+\infty}{a_n}=\sup{a_n}$
2. Se $a_n\searrow \ \Rightarrow \ \lim_{n\to+\infty}{a_n}=\inf{a_n}$  

### Definizione di $e$
$$(f_n)_{n\in\mathbb{R}} = \Big(1+\frac{1}{n}\Big)^n$$
#### Dimostrazione che $f_n\nearrow$ #dim 
devo mostrare che
$$\frac{f_{n+1}}{f_n}\ge1 \ \ \forall n\in\mathbb{N}\setminus\{0\}$$
$$\begin{split}\frac{f_{n+1}}{f_n}&=\frac{(1+\frac{1}{n+1})^{n+1}}{(1+\frac{1}{n})^n}=\frac{(\frac{n+2}{n+1})^{n+1}}{(\frac{n+1}{n})^n}=\Big(\frac{n+2}{n+1}\Big)^{n+1}\cdot\Big(\frac{n}{n+1}\Big)^n=\\&=\Big(\frac{n+2}{n+1}\Big)^{n+1}\cdot\Big(\frac{n}{n+1}\Big)^{n+1}\cdot\Big(\frac{n+1}{n}\Big)=\\&=\Big(\frac{n^2+2n}{(n+1)^2}\Big)^{n+1}\cdot\Big(\frac{n+1}{n}\Big)=\Big(\frac{(n+1)^2-1}{(n+1)^2}\Big)^{n+1}\cdot\Big(\frac{n+1}{n}\Big)=\\&=\Big(1-\frac{1}{(n+1)^2}\Big)^{n+1}\cdot\Big(\frac{n+1}{n}\Big)\ge^* \Big(1-\frac{(n+1)}{(n+1)^2}\Big)\Big(\frac{n+1}{n}\Big)=\\&=\Big(\frac{n}{n+1}\Big)\Big(\frac{n+1}{n}\Big)=1\end{split}$$
[[Analisi I/Principio di Induzione#Disuguaglianza di Bernoulli\|*Disuguaglianza di Bernoulli]]

Sia $h_n=\Big(1+\frac{1}{n}\Big)^{n+1}$, si può mostrare in modo simile a prima che $h_n \searrow$ 
$$\begin{split}h_n&=\Big(1+\frac{1}{n}\Big)^{n+1}=\Big(1+\frac{1}{n}\Big)^n=\\&=f_n\cdot\Big(1+\frac{1}{n}\Big)\ge f_n\end{split}$$Quindi: $$2=f_1\le f_n\le h_n\le h_1=4\ \ \ \ \forall n\in\mathbb{N}\setminus\{0\}$$Quindi $f_n$ e $h_n$ sono regolari e limitate, quindi sono convergenti.
Inoltre, poiché $h_n=f_n\underbrace{\Big(1+\frac{1}{n}\Big)}_{\begin{array}. 1 \\ n\to+\infty\end{array}}$ 
si ha: $$\lim_{n\to+\infty}h_n=\lim_{n\to+\infty}f_n$$ e per il [[Analisi I/Successioni#Teorema del Confronto teor\|teorema del confronto]] tale valore è compreso tra $2$ e $4$ e lo chiamiamo $$e:=\lim_{n\to+\infty}\Big(1+\frac{1}{n}\Big)^n$$
### Teorema - Criterio del Rapporto #teor 
Sia $(a_n)_{n\in\mathbb{N}}$ in $\mathbb{R^+}\setminus\{0\}$ e supponiamo che $\Big(\frac{a_{n+1}}{a_n}\Big)_{n\in\mathbb{N}}$  sia regolare.
Allora:
1. Se $\lim_{n\to+\infty}\frac{a_{n+1}}{a_n}=l>1\Rightarrow \begin{array}. a_n\longrightarrow+\infty \\ n\to+\infty\end{array}$ 
2. Se $0<l<1\Rightarrow \begin{array}. a_n\longrightarrow0 \\ n\to+\infty\end{array}$
#### Dimostrazione (punto 2) #dim
Assumo $$\lim_{n\to+\infty}\frac{a_{n+1}}{a_n}=l<1$$Sia $m \mbox{ t.c. } l<m<1$, per il teorema della permanenza del segno (applicato a $\frac{a_{n+1}}{a_n}-m$) $$\exists \ \overline n\in\mathbb{N}\mbox{ t.c. } \forall n\ge\overline n$$si ha $$\frac{a_{\overline n+1}}{a_n}<m$$In particolare: $$\begin{split}n=\overline n &\ \ \ \ \ \ \ \ \ \ \frac{a_{\overline n+1}}{a_\overline n}<m\Leftrightarrow a_{\overline n+1}<m\cdot a_\overline n
\\ n=\overline n+1 &\ \ \ \ \ \ \ \ \ \ \frac{a_{\overline n+2}}{a_{\overline n+1}}<m\Leftrightarrow a_{\overline n+2}<m\cdot a_{\overline n+1}<m^2a_\overline n\\ n=\overline n+2 &\ \ \ \ \ \ \ \ \ \ \frac{a_{\overline n+3}}{a_{\overline n+2}}<m\Leftrightarrow a_{\overline n+3}<m\cdot a_{\overline n+2}<m^3a_\overline n\end{split}$$ $$n=\overline n+k-1 \Rightarrow a_\overline n+k<m^k\cdot a_\overline n \ \ \ \  \ \forall k>0$$
Chiamo $n=\overline{n}+k$ : $$a_n<m^{n-\overline{n}}\cdot a_\overline{n}=m^n\cdot\frac{a_\overline{n}}{m^\overline{n}}$$Riassumendo: $$0<a_n<\underbrace{m^n\cdot\frac{a_\overline{n}}{m^\overline{n}}}_{0 \text{ (0<m<1)}} \ \ \ \ \forall n\ge\overline{n}$$Per il teorema dei carabinieri: $$\begin{array}.a_n\longrightarrow0\\ \small{n\to+\infty}\end{array}$$

## Successione Trascurabile
Siano $(a_n)_{n\in \mathbb{N}}, (b_n)_{n\in \mathbb{N}}$ **successioni reali**, diciamo che $a_n$ è **trascurabile** rispetto a $b_n$ se: $$\lim_{n\to+\infty}\frac{a_n}{b_n}=0$$in tal caso scriviamo $a_n=o(b_n)$ per $n\to+\infty$
