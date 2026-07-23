---
tags: [kapitel-5, thema, definition, satz, beispiel]
quelle: Skript S. 81–85
---
# Definition und Eigenschaften

> Kapitel 5 · Determinanten — erstes Thema. Zurück zum [[Inhaltsverzeichnis]].
> Nächstes Thema: [[Invertierbarkeit und Determinante]]
> Grundlage: [[Determinante]], [[Matrix]], [[Matrizen und Operationen mit Matrizen]]

## Worum geht es?

Die **Determinante** einer quadratischen [[Matrix]] ist ein Skalar, das Auskunft über die [[Matrixinverse|Invertierbarkeit]] der Matrix gibt. In diesem Kapitel lernen wir verschiedene Möglichkeiten kennen, die Determinante einer quadratischen Matrix zu berechnen, lernen ihre Eigenschaften kennen und erhalten eine weitere Charakterisierung invertierbarer Matrizen (siehe [[Invertierbarkeit und Determinante]]).

## Definition

Die grundlegenden Definitionen liegen (kapitelübergreifend genutzt) unter [[Determinante]]:

![[Determinante#Definition 5.1 (Untermatrix)]]

![[Determinante#Definition 5.2 (Determinante, rekursive Definition)]]

## Beispiel/Bemerkung 5.3

**(a)**
$$\det\begin{pmatrix} a_{11} & a_{12} \\ a_{21} & a_{22} \end{pmatrix} = a_{11} \cdot a_{22} - a_{12} \cdot a_{21}$$

**(b)**
$$\det\begin{pmatrix} a_{11} & a_{12} & a_{13} \\ a_{21} & a_{22} & a_{23} \\ a_{31} & a_{32} & a_{33} \end{pmatrix}$$
$$= a_{11} \cdot (a_{22} a_{33} - a_{23} a_{32}) - a_{12} \cdot (a_{21} a_{33} - a_{23} a_{31}) + a_{13} \cdot (a_{21} a_{32} - a_{22} a_{31})$$

Diese Formel für $(3 \times 3)$-Matrizen lässt sich mit folgendem Verfahren (bekannt als **Regel von Sarrus**) leicht merken: Die ersten beiden Spalten der Matrix werden rechts noch einmal an die Matrix angehängt. Anschließend bildet man Produkte aus jeweils drei Einträgen (dargestellt durch schräge Linien), die folgendem Schema entsprechend addiert bzw. subtrahiert werden:

$$
\begin{array}{ccc|cc}
\color{green}{+} & \color{green}{+} & \color{green}{+} & & \\
a_{11} & a_{12} & a_{13} & a_{11} & a_{12} \\
a_{21} & a_{22} & a_{23} & a_{21} & a_{22} \\
a_{31} & a_{32} & a_{33} & a_{31} & a_{32} \\
\color{red}{-} & \color{red}{-} & \color{red}{-} & &
\end{array}
$$

Man addiert die drei Produkte entlang der Diagonalen von links oben nach rechts unten ($+$) und subtrahiert die drei Produkte entlang der Diagonalen von links unten nach rechts oben ($-$):
$$\det(A) = a_{11}a_{22}a_{33} + a_{12}a_{23}a_{31} + a_{13}a_{21}a_{32} - a_{31}a_{22}a_{13} - a_{32}a_{23}a_{11} - a_{33}a_{21}a_{12}.$$

> [!warning] Achtung
> Die Regel von Sarrus gilt **nur für $(3 \times 3)$-Matrizen**. Sie lässt sich nicht auf größere Matrizen übertragen.

**(c)** Für eine $(n \times n)$-Matrix erhält man zur Berechnung der Determinante bis zu $n!$ Summanden. Es gibt noch weitere Formeln zur Berechnung der Determinante, z. B. die **Leibniz-Formel**, die Permutationen verwendet.

**(d)** Ist $A$ eine **untere** oder **obere Dreiecksmatrix**, also
$$A = \begin{pmatrix} a_{11} & 0 & \cdots & 0 \\ a_{21} & a_{22} & \cdots & 0 \\ \vdots & \vdots & \ddots & 0 \\ a_{n1} & a_{n2} & \cdots & a_{nn} \end{pmatrix} \quad \text{bzw.} \quad A = \begin{pmatrix} a_{11} & a_{12} & \cdots & a_{1n} \\ 0 & a_{22} & \cdots & a_{2n} \\ \vdots & \vdots & \ddots & \vdots \\ 0 & 0 & \cdots & a_{nn} \end{pmatrix},$$
so lässt sich $\det(A)$ einfach berechnen als
$$\det(A) = a_{11} \cdot a_{22} \cdot \ldots \cdot a_{nn},$$
also als das **Produkt der Diagonalelemente**.

> [!note]- Begründung
> Für $n = 1$ ist das klar nach der Definition der Determinante: Falls $A = (a)$, so ist $\det(A) = a$.
>
> Für $n > 1$ gilt nach Definition (Entwicklung nach der 1. Zeile, alle Einträge $a_{12}, \dots, a_{1n}$ sind $0$):
> $$\det\begin{pmatrix} a_{11} & 0 & \cdots & 0 \\ a_{21} & a_{22} & \cdots & 0 \\ \vdots & \vdots & \ddots & 0 \\ a_{n1} & a_{n2} & \cdots & a_{nn} \end{pmatrix} = a_{11} \cdot \det\begin{pmatrix} a_{22} & \cdots & 0 \\ \vdots & \ddots & 0 \\ a_{n2} & \cdots & a_{nn} \end{pmatrix},$$
> mittels Induktion folgt die Behauptung. $\qquad \blacksquare$

**(e)** Mit der Überlegung aus Teil (d) gilt also
$$\det(E_n) = 1.$$

## Satz 5.4 (Entwicklungssatz von Laplace)

Definition 5.2 lässt sich verallgemeinern zu folgender Formel. (Die in Definition 5.2 verwendete Formel für $n > 1$ entspricht dabei der Entwicklung nach der 1. Zeile.)

Sei $A \in M_n(K)$.

**(a) Entwicklung nach der $i$-ten Zeile:** Für $i \in \{1, \dots, n\}$ gilt
$$\det(A) = \sum_{j=1}^{n} (-1)^{i+j}\, a_{ij}\, \det(A_{ij}).$$

**(b) Entwicklung nach der $j$-ten Spalte:** Für $j \in \{1, \dots, n\}$ gilt
$$\det(A) = \sum_{i=1}^{n} (-1)^{i+j}\, a_{ij}\, \det(A_{ij}).$$

> [!tip] Vorzeichen-Schachbrett
> Die Vorzeichen $(-1)^{i+j}$ folgen einem Schachbrettmuster $\begin{pmatrix} + & - & + & \cdots \\ - & + & - & \cdots \\ + & - & + & \cdots \\ \vdots & & & \ddots \end{pmatrix}$.

## Beispiel 5.5

$$A = \begin{pmatrix} 2 & 1 & 1 \\ -1 & 0 & 3 \\ 2 & 0 & 4 \end{pmatrix}$$

Mit Definition 5.2 (entspricht Entwicklung nach der 1. Zeile):
$$\det(A) = 2 \cdot \det\begin{pmatrix} 0 & 3 \\ 0 & 4 \end{pmatrix} - 1 \cdot \det\begin{pmatrix} -1 & 3 \\ 2 & 4 \end{pmatrix} + 1 \cdot \det\begin{pmatrix} -1 & 0 \\ 2 & 0 \end{pmatrix}$$
$$= 2 \cdot 0 - 1 \cdot (-10) + 1 \cdot 0 = 10$$

oder: Entwicklung nach der 3. Zeile:
$$\det(A) = 2 \cdot \det\begin{pmatrix} 1 & 1 \\ 0 & 3 \end{pmatrix} - 0 \cdot \det\begin{pmatrix} 2 & 1 \\ -1 & 3 \end{pmatrix} + 4 \cdot \det\begin{pmatrix} 2 & 1 \\ -1 & 0 \end{pmatrix}$$
$$= 2 \cdot 3 + 4 \cdot 1 = 10$$

oder (besser): Entwicklung nach der 2. Spalte:
$$\det(A) = -1 \cdot \det\begin{pmatrix} -1 & 3 \\ 2 & 4 \end{pmatrix} + 0 \cdot \det\begin{pmatrix} 2 & 1 \\ 2 & 4 \end{pmatrix} - 0 \cdot \det\begin{pmatrix} 2 & 1 \\ -1 & 3 \end{pmatrix}$$
$$= -1 \cdot (-10) = 10$$

Es ist also **geschickt, nach einer Zeile oder Spalte zu entwickeln, in der viele Nullen stehen**. Falls es nur wenige Nullen gibt, kann man zuerst den Gauß-Algorithmus ([[Matrizen und Operationen mit Matrizen|4.12]]) anwenden. Allerdings kann sich die Determinante dabei evtl. ändern, wie wir in Satz 5.7 sehen werden.

## Bemerkung 5.6

Aus Satz 5.4 folgt
$$\det(A) = \det(A^T).$$

## Satz 5.7 (Eigenschaften der Determinante)

Seien $A, B \in M_n(K)$ und $s_1, \dots, s_n$ die Spalten von $A$. Weiter sei $s_i' \in K^n$ ein Vektor und $\lambda \in K$. Folgende Eigenschaften gelten für die Determinante.

**(D1)** $\det(s_1, \dots, s_i + s_i', \dots, s_n) = \det(s_1, \dots, s_i, \dots, s_n) + \det(s_1, \dots, s_i', \dots, s_n)$

**(D2)** Beim **Vertauschen zweier Spalten** von $A$ ändert sich das **Vorzeichen** von $\det(A)$.

**(D3)** $\det(s_1, \dots, \lambda s_i, \dots, s_n) = \lambda \cdot \det(s_1, \dots, s_i, \dots, s_n)$

**(D4)** $\det(\lambda \cdot A) = \det(\lambda s_1, \dots, \lambda s_n) = \lambda^n \cdot \det(A)$

**(D5)** Ist eine Spalte von $A$ gleich $\mathcal{O}$ (Nullvektor), so ist $\det(A) = 0$.

**(D6)** Besitzt $A$ zwei **identische Spalten**, so ist $\det(A) = 0$.

**(D7)** $\det(s_1, \dots, \underbrace{s_i + \lambda s_j}_{i}, \dots, s_n) = \det(A) \qquad (i \neq j)$

**(D8)** $\det(A \cdot B) = \det(A) \cdot \det(B)$

Analog lassen sich die Eigenschaften mit **Zeilen** statt Spalten definieren.

> [!note]- Beweis
> - Die Eigenschaften **(D1)–(D3)** lassen sich mittels Einsetzen der Definition 5.2 bzw. Satz 5.4 nachprüfen.
> - **(D4)** folgt durch wiederholte Anwendung von (D3).
> - **(D5)** folgt aus (D3) für $\lambda = 0$.
> - **(D6)** lässt sich mittels vollständiger Induktion und Definition 5.2 bzw. Satz 5.4 zeigen. Für den Induktionsanfang betrachtet man $(2 \times 2)$-Matrizen mit zwei identischen Spalten und berechnet die Determinante, die null ist. Im Induktionsschritt entwickelt man derart nach einer Spalte, dass die kleineren Matrizen in der Determinantenberechnung jeweils wieder die identischen Spalten enthalten.
> - **(D7)** folgt mit (D1), (D3), (D6).
> - **(D8)** beweisen wir hier nicht. Diese Eigenschaft lässt sich mittels sogenannter *Elementarmatrizen* zeigen. Das sind Matrizen, die den elementaren Zeilen- und Spaltenumformungen entsprechen (Multiplikation einer Matrix mit einer Elementarmatrix entspricht der zugehörigen Zeilen- bzw. Spaltenumformung der Matrix). $\qquad \blacksquare$

## Beispiel/Bemerkung 5.8

Eine Strategie zur Berechnung der Determinante ist es also, mit dem Gauß-Algorithmus viele Nulleinträge zu erzeugen und dann nach einer passenden Zeile oder Spalte zu entwickeln, oder die Matrix auf **Dreiecksform** zu bringen und dann einfach die Diagonaleinträge zu multiplizieren. Dabei sollte man beachten, dass sich die Determinante ändert, wenn beim Ausführen des Algorithmus

- zwei Zeilen oder zwei Spalten **vertauscht** werden **(D2)**, oder
- eine Zeile bzw. Spalte mit einem Skalar **multipliziert** wird **(D3)**.

Bei der **Addition einer Zeile bzw. Spalte zum Vielfachen einer anderen** Zeile bzw. Spalte ändert sich die Determinante dagegen **nicht (D7)**.

Zum Beispiel:
$$\det\begin{pmatrix} 0 & 1 & 2 \\ -2 & 0 & 3 \\ 0 & -2 & 3 \end{pmatrix} \overset{I \leftrightarrow II}{=} -\det\begin{pmatrix} -2 & 0 & 3 \\ 0 & 1 & 2 \\ 0 & -2 & 3 \end{pmatrix} \overset{III:\, 2\,II + III}{=} -\det\begin{pmatrix} -2 & 0 & 3 \\ 0 & 1 & 2 \\ 0 & 0 & 7 \end{pmatrix} = -(-2) \cdot 1 \cdot 7 = 14.$$
