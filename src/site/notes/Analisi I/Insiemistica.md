---
{"dg-publish":true,"permalink":"/analisi-i/insiemistica/"}
---

### Massimo/Minimo di $A \subseteq \mathbb{R}$ 
##### Definizione #def 
Sia $A\subseteq\mathbb{R},A\neq\varnothing$
Diciamo che $M\in\mathbb{R}$ è **massimo** di $A$ se:
- $M\in A$
- $M\ge a \ \ \ \ \ \forall a\in A$
Diciamo che $m\in\mathbb{R} è **minimo** di $A$ se:
- $m\in A$
- $m\le a \ \ \ \ \ \forall a\in A$
##### Osservazione
Sia $A\subseteq\mathbb{R}$: se $A$ ammette $\max$ (o $\min$) allora esso è **unico**.
###### Dimostrazione #dim 
Siamo $M_1$ e $M_2$ massimi di $A$.
Allora, per definizione di massimo, si ha: $M_1\ge M_2$ (poiché $M_1$ è $\max$ e $M_2\in A$) ma anche $M_2\ge M_1$
$\Rightarrow M_1=M_2$
### Maggiorante/Minorante
##### Definizione #def 
Sia $A\subseteq\mathbb{R}$. 
Diciamo che $\mu\in\mathbb{R}$ è un **maggiorante** di $A$ se $\mu\ge a \ \forall a\in A$
Diciamo che $\lambda\in\mathbb{R}$ è un **minorante** di $A$ se $\lambda\le a \ \forall a\in A$
##### Definizione #def 
Se $A$ ammette maggioranti, si dice che è **limitato superiormente**
Se $A$ ammette minoranti, si dice che è **limitato inferiormente**
Se $A$ è limitato sia superiormente che inferiormente allora $A$ si dice **limitato**
#### Teorema #teor 
Sia $A\subseteq{R}$
- L'insieme dei maggioranti ammette minimo
- L'insieme dei minoranti ammette massimo
##### Definizione - Estremi #def 
Chiamiamo **estremo superiore** di $A$ ($\sup A$) il minimo dell'insieme dei maggioranti di $A$.
Chiamiamo **estremo inferiore** di $A$ ($\inf A$) il massimo dell'insieme dei minoranti di $A$.
Se $A$ non è limitato superiormente, poniamo $\sup A=+\infty$
Se $A$ non è limitato inferiormente, poniamo $\inf A=-\infty$