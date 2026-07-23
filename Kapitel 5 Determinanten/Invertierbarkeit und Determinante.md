---
tags: [kapitel-5, thema, satz, beispiel]
quelle: Skript S. 86–87
---
# Invertierbarkeit und Determinante

> Kapitel 5 · Determinanten — zweites Thema. Zurück zum [[Inhaltsverzeichnis]].
> Voriges Thema: [[Definition und Eigenschaften]]
> Grundlage: [[Determinante]], [[Matrixinverse]], [[Zeilen- und Spaltenrang]]

Wie bereits erwähnt, liefert die [[Determinante]] eine weitere Möglichkeit zur Überprüfung der [[Matrixinverse|Invertierbarkeit]] einer Matrix, wie der folgende Satz zeigt.

## Satz 5.9 (Charakterisierung invertierbarer Matrizen mittels der Determinante)

Sei $A \in M_n(K)$. Dann gilt
$$A \text{ ist invertierbar} \iff \det(A) \neq 0.$$

In diesem Fall gilt
$$\det(A^{-1}) = (\det(A))^{-1} \quad \left( = \frac{1}{\det(A)}, \text{ falls } K = \mathbb{R} \text{ oder } K = \mathbb{Q} \right).$$

> [!note]- Beweis
> **„$\Rightarrow$"** Sei $A$ invertierbar, das heißt, es existiert eine Matrix $A^{-1}$ mit $A \cdot A^{-1} = E_n$. Dann gilt
> $$\underbrace{\det(A \cdot A^{-1})}_{= \det(A) \cdot \det(A^{-1}),\ (D8)} = \det(E_n) = 1.$$
> Also ist $\det(A) \neq 0$ und $\det(A^{-1}) = (\det(A))^{-1}$.
>
> **„$\Leftarrow$"** Wir beweisen die Rückrichtung durch **Kontraposition**. Sei dazu $A$ nicht invertierbar. Wir zeigen, dass dann $\det(A) = 0$ gelten muss.
>
> Wenn $A$ nicht invertierbar ist, gilt $\operatorname{rg}(A) < n$ nach [[Zeilen- und Spaltenrang|Satz 4.26]]. Also sind die Spalten von $A$ linear abhängig, das heißt, es gibt eine Spalte $s_i$, die sich als Linearkombination der übrigen Spalten von $A$ darstellen lässt, also $s_i = \sum_{\substack{k=1 \\ (k \neq i)}}^{n} \lambda_k s_k$.
>
> Damit folgt
> $$\det(A) \underset{(D7)}{=} \det(s_1, \dots, \underbrace{s_i - \sum_{\lambda} \lambda_k s_k}_{i}, \dots, s_n) = \det(s_1, \dots, \mathcal{O}, \dots, s_n) \underset{(D5)}{=} 0. \qquad \blacksquare$$

## Bemerkung 5.10 (Formel für die Inverse einer $(2 \times 2)$-Matrix)

Für $(2 \times 2)$-Matrizen lässt sich die Inverse (falls existent) einfach mittels der Determinante angeben.

Für $A = \begin{pmatrix} a & b \\ c & d \end{pmatrix} \in M_2(K)$ ist
$$A^{-1} = (\det(A))^{-1} \cdot \begin{pmatrix} d & -b \\ -c & a \end{pmatrix}$$
$$\left( = \frac{1}{\det(A)} \cdot \begin{pmatrix} d & -b \\ -c & a \end{pmatrix}, \text{ falls } K = \mathbb{R} \text{ oder } K = \mathbb{Q} \right).$$

> [!note]- Beweis
> Nachrechnen von $A \cdot A^{-1} = A^{-1} \cdot A = E_2$. $\qquad \blacksquare$

> [!tip] Merkhilfe
> Bei einer $(2 \times 2)$-Matrix werden die **Diagonaleinträge vertauscht** ($a \leftrightarrow d$) und die **Nebendiagonaleinträge mit $-1$ multipliziert** ($b, c$), dann durch $\det(A) = ad - bc$ geteilt.
