---
tags: [kapitel-4, definition]
quelle: Skript S. 59–61
aliases: [Matrix, Matrizen, Transponierte, Einheitsmatrix, Nullmatrix, Matrixprodukt]
---
# Matrix

> Kapitel 4 · Matrizen und lineare Gleichungssysteme — atomare Grunddefinition. Zurück zum [[Inhaltsverzeichnis]].
> Grundlage: [[Körper]], [[Vektorraum]]. Verwendet in: [[Matrizen und Operationen mit Matrizen]], [[Zeilen- und Spaltenrang]], [[Matrixinverse]], [[Determinante]], [[Eigenwerte, Eigenvektoren, Eigenräume]].

Diese Datei enthält die zentrale Definition einer **Matrix** samt Notation, Typ, Transponierter und den Grundoperationen. Sie wird von [[Matrizen und Operationen mit Matrizen]] eingebunden und kapitelübergreifend per `[[Matrix]]` verlinkt.

## Definition 4.1 (Matrix)

**(a)** Seien $m, n \in \mathbb{N}$. Eine **$(m \times n)$-Matrix** $A$ über einem [[Körper]] $K$ ist ein rechteckiges Schema

$$A = \begin{pmatrix} a_{11} & a_{12} & \cdots & a_{1n} \\ a_{21} & a_{22} & \cdots & a_{2n} \\ \vdots & \vdots & \ddots & \vdots \\ a_{m1} & a_{m2} & \cdots & a_{mn} \end{pmatrix}$$

mit $m$ **Zeilen** und $n$ **Spalten** und Einträgen $a_{ij}$ ($1 \leq i \leq m,\ 1 \leq j \leq n$) $\in K$, wobei der erste Index $i$ die Zeile angibt und der zweite Index $j$ die Spalte.
Schreibweise: $A = (a_{ij})_{i=1\dots m,\ j=1\dots n}$ oder einfach nur $A = (a_{ij})$.

**(b)** Mit $M_{m,n}$ bezeichnen wir die Menge aller $(m \times n)$-Matrizen über $K$, mit $M_n(K)$ die Menge aller $(n \times n)$-Matrizen über $K$ (die **quadratischen Matrizen**).
Mit dem Subskript $m,n$ (und durch die Schreibweise $m \times n$) wird der **Typ** der Matrix angegeben.

**(c)** Ist $A \in M_{m,n}(K)$, so erhält man die zu $A$ **transponierte Matrix** $A^T \in M_{n,m}(K)$,

$$A^T := \begin{pmatrix} a_{11} & a_{21} & \cdots & a_{m1} \\ a_{12} & a_{22} & \cdots & a_{m2} \\ \vdots & \vdots & \ddots & \vdots \\ a_{1n} & a_{2n} & \cdots & a_{mn} \end{pmatrix},$$

indem man Zeilen und Spalten von $A$ tauscht.

> [!example] Beispiel (Transponieren)
> $$\begin{pmatrix} 1 & 2 & 3 \\ 4 & 5 & 6 \end{pmatrix}^T = \begin{pmatrix} 1 & 4 \\ 2 & 5 \\ 3 & 6 \end{pmatrix}.$$
> Es gilt $\left(A^T\right)^T = A$.

**(d)** Spezielle Matrizen:
- Eine $(1 \times n)$-Matrix wird auch als **Zeilenvektor** mit $n$ Einträgen bezeichnet.
- Eine $(m \times 1)$-Matrix wird als **Spaltenvektor** mit $m$ Einträgen bezeichnet.
- $O = O_{m,n} = \begin{pmatrix} 0 & \cdots & 0 \\ \vdots & \ddots & \vdots \\ 0 & \cdots & 0 \end{pmatrix}$ (alle $a_{ij} = 0$) ist die **Nullmatrix**.
- $E = E_n = \begin{pmatrix} 1 & 0 & \cdots & 0 \\ 0 & 1 & \cdots & 0 \\ \vdots & \vdots & \ddots & \vdots \\ 0 & 0 & \cdots & 1 \end{pmatrix} = \begin{pmatrix} 1 & & 0 \\ & \ddots & \\ 0 & & 1 \end{pmatrix}$ ist die **$(n \times n)$-Einheitsmatrix**.
  Also ist $E_n = (\delta_{ij})$ mit $\delta_{ij} = \begin{cases} 1 & i = j \\ 0 & i \neq j \end{cases}$. (Das Symbol $\delta_{ij}$ wird auch als **Kronecker-Delta** bezeichnet.)

**(e)** Die Menge $M_{m,n}(K)$ lässt sich als [[Vektorraum|$K$-Vektorraum]] auffassen. Wir brauchen dazu eine **Addition** und eine **skalare Multiplikation**: Für $A = (a_{ij}),\ B = (b_{ij}) \in M_{m,n}(K)$ (beide Matrizen sind vom selben Typ!) und $\lambda \in K$ ist

$$A + B := (a_{ij} + b_{ij})_{i=1\dots m,\ j=1\dots n} \quad (\text{Summe von Matrizen}) \quad \text{und}$$
$$\lambda \cdot A := (\lambda \cdot a_{ij})_{i=1\dots m,\ j=1\dots n} \quad (\text{Skalares Vielfaches von } A).$$

Die „Vektoren" dieses Vektorraums sind also $(m \times n)$-Matrizen mit Einträgen aus $K$, der Nullvektor $\mathcal{O}$ ist $O$ (die Nullmatrix), eine Basis wäre z. B.

$$\begin{pmatrix} 1 & 0 & \cdots & 0 \\ 0 & 0 & \cdots & 0 \\ \vdots & \vdots & & \vdots \\ 0 & 0 & \cdots & 0 \end{pmatrix},\ \begin{pmatrix} 0 & 1 & \cdots & 0 \\ 0 & 0 & \cdots & 0 \\ \vdots & \vdots & & \vdots \\ 0 & 0 & \cdots & 0 \end{pmatrix},\ \dots,\ \begin{pmatrix} 0 & 0 & \cdots & 0 \\ 0 & 0 & \cdots & 0 \\ \vdots & \vdots & & \vdots \\ 0 & 0 & \cdots & 1 \end{pmatrix}.$$

Die Dimension dieses Vektorraums ist $\dim(M_{m,n}(K)) = m \cdot n$.

**(f)** Für $A = (a_{ij})_{i=1\dots m,\ j=1\dots n} \in M_{m,n}(K)$ und $B = (b_{jk})_{j=1\dots n,\ k=1\dots l} \in M_{n,l}(K)$ ist das **Matrixprodukt** $A \cdot B$ definiert

$$A \cdot B = (c_{ik})_{i=1\dots m,\ k=1\dots l} \in M_{m,l}(K)$$

mit

$$c_{ik} = a_{i1} b_{1k} + a_{i2} b_{2k} + \cdots + a_{in} b_{nk} \quad (\text{„$i$-te Zeile von $A$ mal $k$-te Spalte von $B$"}) = \sum_{j=1}^{n} a_{ij} b_{jk}.$$

Wir schreiben auch $AB$ statt $A \cdot B$.

> [!warning] Wichtig
> Das Produkt $A \cdot B$ ist nur definiert, wenn die **Anzahl der Spalten von $A$** gleich der **Anzahl der Zeilen von $B$** ist!

**(g)** Die Menge der quadratischen Matrizen $M_n(K)$ bildet mit der Matrixaddition $+$ und der Matrixmultiplikation $\cdot$ einen [[Ring|Ring mit Eins]] (die Eins ist hier die Einheitsmatrix $E_n$).
Eine Matrix $A \in M_n(K)$ heißt **invertierbar**, falls $A^{-1} \in M_n(K)$ existiert mit

$$A A^{-1} = A^{-1} A = E_n.$$

Die Berechnung von $A^{-1}$ wird in [[Matrixinverse]] behandelt.
