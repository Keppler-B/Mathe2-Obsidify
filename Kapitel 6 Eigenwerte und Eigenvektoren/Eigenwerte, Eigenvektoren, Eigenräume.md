---
tags: [kapitel-6, thema, definition, satz, beispiel]
quelle: Skript S. 89–92
aliases: [Eigenwerte, Eigenvektoren, Eigenräume, Charakteristisches Polynom, Eigenwert, Eigenvektor, Eigenraum]
---
# Eigenwerte, Eigenvektoren, Eigenräume

> Kapitel 6 · Eigenwerte und Eigenvektoren. Zurück zum [[Inhaltsverzeichnis]].
> Voriges Thema: [[Definition und Eigenschaften]] (Determinanten, Kapitel 5) · Nächstes Thema: [[Diagonalisierbarkeit und Spektralsatz]]
> Grundlage: [[Matrix]], [[Determinante]], [[Vektorraum]], [[Zeilen- und Spaltenrang]], [[Matrixinverse]]

Im Zusammenhang mit [[Matrizen und Operationen mit Matrizen|Matrizen]] oder [[Lineare Abbildungen (Kapitel 8)|linearen Abbildungen]] spricht man oft von **Eigenvektoren** und **Eigenwerten**. Eigenvektoren einer quadratischen Matrix sind Vektoren, die durch Multiplikation mit der Matrix nur skaliert und nicht anderweitig verändert werden. Der Faktor, mit dem skaliert wird, heißt **Eigenwert** der Matrix. Eigenwerte charakterisieren wichtige Eigenschaften von Matrizen, etwa die eindeutige Lösbarkeit des zugehörigen linearen Gleichungssystems.

## Definition 6.1 (Eigenwert, Eigenvektor, Eigenraum)

![[Eigenwert und Eigenvektor#Definition 6.1 (Eigenwert, Eigenvektor, Eigenraum)]]

> Die Kern-Definition ist als atomare Datei [[Eigenwert und Eigenvektor]] gepflegt und hier eingebunden.

## Satz 6.2 (Berechnung von Eigenwerten)

Sei $A \in M_n(K)$. Dann gilt

$$\lambda \in K \text{ ist Eigenwert von } A \iff \det(A - \lambda \cdot E_n) = 0,$$

und die zu $\lambda$ gehörenden Eigenvektoren sind genau die nicht-trivialen Lösungen des LGS

$$[A - \lambda \cdot E_n]\,x = \mathcal{O},$$

also:

$$\operatorname{Eig}_A(\lambda) = \ker(A - \lambda \cdot E_n).$$

> [!note]- Beweis
> Für Eigenwerte $\lambda$ und Eigenvektoren $x$ von $A$ gilt:
> $$Ax = \lambda x \iff Ax = \lambda E_n x \iff (A - \lambda E_n)x = \mathcal{O}.$$
> Es gilt also:
> $$
> \begin{aligned}
> \lambda \text{ ist Eigenwert von } A
> &\iff (A - \lambda E_n)x = \mathcal{O} \text{ hat noch weitere Lösungen als } x = \mathcal{O} \\
> &\overset{4.21}{\iff} \operatorname{rg}(A - \lambda E_n) < n \\
> &\overset{4.26}{\iff} (A - \lambda E_n) \text{ ist nicht invertierbar} \\
> &\overset{5.9}{\iff} \det(A - \lambda E_n) = 0.
> \end{aligned}
> $$
> Ein Vektor $x$ ist also genau dann Eigenvektor von $A$, wenn $x \neq \mathcal{O}$ und $(A - \lambda E_n)x = \mathcal{O}$. $\qquad \blacksquare$

## Definition 6.3 (Charakteristisches Polynom)

Für $A \in M_n(K)$ heißt

$$p_A(\lambda) := \det(A - \lambda \cdot E_n)$$

das **charakteristische Polynom** von $A$. Seine Nullstellen sind nach Satz 6.2 genau die Eigenwerte von $A$.

## Beispiel 6.4

Sei $A = \begin{pmatrix} 1 & 1 \\ -2 & 4 \end{pmatrix} \in M_2(\mathbb{R})$. Wir bestimmen das charakteristische Polynom, Eigenwerte, Eigenvektoren und Eigenräume von $A$.

$$A - \lambda \cdot E_2 = \begin{pmatrix} 1 & 1 \\ -2 & 4 \end{pmatrix} - \lambda \cdot \begin{pmatrix} 1 & 0 \\ 0 & 1 \end{pmatrix} = \begin{pmatrix} 1-\lambda & 1 \\ -2 & 4-\lambda \end{pmatrix}$$

- **Charakteristisches Polynom:**
$$
\begin{aligned}
p_A(\lambda) = \det\begin{pmatrix} 1-\lambda & 1 \\ -2 & 4-\lambda \end{pmatrix}
&= (1-\lambda)\cdot(4-\lambda) - 1\cdot(-2) \\
&= \lambda^2 - 5\lambda + 6 \\
&= (\lambda - 2)(\lambda - 3)
\end{aligned}
$$

- **Eigenwerte von $A$:**
$$\lambda \text{ ist Eigenwert von } A \overset{6.2}{\iff} p_A(\lambda) = 0 \iff \lambda = 2 \ \lor\ \lambda = 3.$$
Also sind $\lambda_1 = 2$ und $\lambda_2 = 3$ die Eigenwerte von $A$.

- **Eigenvektoren und Eigenräume von $A$:**

$x$ ist Eigenvektor zu $\lambda_1 = 2 \iff x \neq \mathcal{O}$ und $(A - \lambda_1 E_2)x = \mathcal{O}$, also
$$\begin{pmatrix} 1-2 & 1 \\ -2 & 4-2 \end{pmatrix} x = \begin{pmatrix} 0 \\ 0 \end{pmatrix}, \qquad \text{d.h.} \qquad \begin{pmatrix} -1 & 1 \\ -2 & 2 \end{pmatrix} x = \begin{pmatrix} 0 \\ 0 \end{pmatrix}.$$
Eine mögliche Lösung ist z. B. $x = \begin{pmatrix} 1 \\ 1 \end{pmatrix}$. Um alle Lösungen angeben zu können, berechnen wir den Eigenraum zu $\lambda_1$ und erhalten
$$\operatorname{Eig}_A(\lambda_1) = \ker\begin{pmatrix} -1 & 1 \\ -2 & 2 \end{pmatrix} = \left\langle \begin{pmatrix} 1 \\ 1 \end{pmatrix} \right\rangle.$$

$y$ ist Eigenvektor zu $\lambda_2 = 3 \iff y \neq \mathcal{O}$ und
$$\begin{pmatrix} -2 & 1 \\ -2 & 1 \end{pmatrix} y = \begin{pmatrix} 0 \\ 0 \end{pmatrix}.$$
Eine mögliche Lösung ist $y = \begin{pmatrix} 1 \\ 2 \end{pmatrix}$, und es gilt
$$\operatorname{Eig}_A(\lambda_2) = \ker\begin{pmatrix} -2 & 1 \\ -2 & 1 \end{pmatrix} = \left\langle \begin{pmatrix} 1 \\ 2 \end{pmatrix} \right\rangle.$$

## Anwendungen 6.5

**(a) Matrixpotenzen** lassen sich mit Kenntnis der Eigenwerte und Eigenvektoren einfach berechnen. Berechne z. B.

$$A^{2026} = \underbrace{A \cdot A \cdot \ldots \cdot A}_{2026 \text{ mal}} \qquad \text{für } A = \begin{pmatrix} 1 & 1 \\ -2 & 4 \end{pmatrix} \text{ aus Bsp. 6.4.}$$

Wir bilden die Matrix $S$, die zu jedem Eigenwert von $A$ jeweils einen Eigenvektor als Spalte enthält, also

$$S := \begin{pmatrix} 1 & 1 \\ 1 & 2 \end{pmatrix}, \qquad \text{Spalten } x_1,\, x_2.$$

Dann ist

$$S^{-1} \overset{5.10}{=} \begin{pmatrix} 2 & -1 \\ -1 & 1 \end{pmatrix}, \qquad \text{da } \det(S) = 1,$$

und

$$A = S \cdot \underbrace{\begin{pmatrix} 2 & 0 \\ 0 & 3 \end{pmatrix}}_{:=D} \cdot S^{-1}$$

mit der **Diagonalmatrix** $D$, deren Einträge auf der Diagonalen die Eigenwerte $\lambda_1 = 2$ und $\lambda_2 = 3$ von $A$ sind (und zwar in der Reihenfolge, in der die Eigenvektoren für die Spalten von $S$ gewählt wurden). Damit gilt

$$
\begin{aligned}
A^{2026} = (SDS^{-1})^{2026}
&= (SD\,\underbrace{S^{-1})(S}_{=E_2}\,D\,\underbrace{S^{-1})(S}_{=E_2}\,D\,\underbrace{S^{-1}) \cdots (S}_{=E_2}\,D\,S^{-1}) \\
&= S \cdot D^{2026} \cdot S^{-1} \\
&= S \cdot \begin{pmatrix} 2^{2026} & 0 \\ 0 & 3^{2026} \end{pmatrix} \cdot S^{-1}.
\end{aligned}
$$

> [!tip] Idee
> Beim Ausmultiplizieren von $(SDS^{-1})^{2026}$ heben sich benachbarte Faktoren $S^{-1}S = E_2$ gegenseitig weg. Übrig bleiben nur ein äußeres $S$, die Potenz $D^{2026}$ der Diagonalmatrix (die man einträgeweise bildet) und ein äußeres $S^{-1}$. Vgl. [[Diagonalisierbarkeit und Spektralsatz]].

**(b)** Einige weitere Anwendungen, die in der Vorlesung besprochen werden, sind beispielsweise Eigenschwingungen, Googles PageRank-Algorithmus oder die „Eigenfaces".

## Definition/Bemerkung 6.6 (Grad und algebraische Vielfachheit)

Für $A \in M_n(K)$ ist

$$p_A(\lambda) = \det(A - \lambda E_n) = \det\begin{pmatrix} a_{11}-\lambda & a_{12} & \dots & a_{1n} \\ \vdots & \ddots & & \vdots \\ a_{n1} & \dots & \dots & a_{nn}-\lambda \end{pmatrix}$$

ein Polynom vom **Grad $n$** (folgt aus der Definition der [[Determinante]]). Die Nullstellen von $p_A(\lambda)$ sind genau die Eigenwerte von $A$. Ist $K = \mathbb{R}$, so besitzt $A$ also **höchstens $n$** Eigenwerte; für $K = \mathbb{C}$ besitzt $A$ **genau $n$** (nicht notwendigerweise verschiedene) Eigenwerte.

Die Anzahl des Auftretens eines Eigenwerts $\lambda_j$ als Nullstelle in $p_A(\lambda)$ (die Vielfachheit der Nullstelle) nennt man die **algebraische Vielfachheit** von $\lambda_j$.

Beispielsweise ist für

$$A = \begin{pmatrix} 2 & 3 & 0 \\ 0 & 2 & -1 \\ 0 & 0 & 1 \end{pmatrix}$$

das charakteristische Polynom

$$p_A(\lambda) = \det\begin{pmatrix} 2-\lambda & 3 & 0 \\ 0 & 2-\lambda & -1 \\ 0 & 0 & 1-\lambda \end{pmatrix} = (2-\lambda)(2-\lambda)(1-\lambda).$$

Die Nullstelle $\lambda = 2$ tritt also zweifach auf, $\lambda = 2$ ist Eigenwert mit algebraischer Vielfachheit $2$. Die Nullstelle $\lambda = 1$ tritt nur einmal auf, $\lambda = 1$ ist Eigenwert mit algebraischer Vielfachheit $1$ (und wird dann auch als **einfacher Eigenwert** von $A$ bezeichnet).
