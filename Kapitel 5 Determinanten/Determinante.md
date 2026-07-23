---
tags: [kapitel-5, definition]
quelle: Skript S. 81
aliases: [Determinante, det, Untermatrix]
---
# Determinante

> Kapitel 5 · Determinanten — atomare Kern-Definition. Zurück zum [[Inhaltsverzeichnis]].
> Grundlage: [[Matrix]], [[Matrizen und Operationen mit Matrizen]]
> Verwendet in: [[Definition und Eigenschaften]], [[Invertierbarkeit und Determinante]], [[Eigenwerte, Eigenvektoren, Eigenräume]] (charakteristisches Polynom $\det(A - \lambda I)$)

Die **Determinante** einer quadratischen [[Matrix]] ist ein Skalar (also je nach [[Körper]] oftmals eine Zahl), das sich aus den Einträgen der Matrix berechnen lässt und Auskunft über die [[Matrixinverse|Invertierbarkeit]] der Matrix (und auch über Eigenschaften der linearen Abbildung, die durch diese Matrix beschrieben wird) gibt. Ursprünglich wurde die Determinante im Zusammenhang mit linearen Gleichungssystemen definiert: sie gibt an („determiniert"), ob das LGS eine eindeutige Lösung besitzt.

## Definition 5.1 (Untermatrix)

Sei $A \in M_n(K)$ und $i, j \in \{1, \dots, n\}$. Dann ist die **Untermatrix** $A_{ij} \in M_{n-1}(K)$ die Matrix, die man aus $A$ durch **Streichen der $i$-ten Zeile und der $j$-ten Spalte** erhält.

Beispielsweise sehen für $A = \begin{pmatrix} 1 & 2 & 3 \\ 4 & 5 & 6 \\ 7 & 8 & 9 \end{pmatrix}$ zwei der möglichen Untermatrizen wie folgt aus:

$$A_{11} = \begin{pmatrix} 5 & 6 \\ 8 & 9 \end{pmatrix}, \qquad A_{32} = \begin{pmatrix} 1 & 3 \\ 4 & 6 \end{pmatrix}.$$

## Definition 5.2 (Determinante, rekursive Definition)

Sei $A \in M_n(K)$. Wir definieren $\det(A) \in K$ **rekursiv** wie folgt:

- Für $n = 1$, also $A = (a)$ mit $a \in K$, ist
  $$\det(A) := a.$$
- Für $n > 1$ ist
  $$\det(A) := \sum_{j=1}^{n} (-1)^{1+j}\, a_{1j} \cdot \det(A_{1j})$$
  $$= a_{11} \cdot \det(A_{11}) - a_{12} \cdot \det(A_{12}) + a_{13} \cdot \det(A_{13}) - \dots \pm a_{1n} \cdot \det(A_{1n}).$$

Das Skalar $\det(A)$ heißt **Determinante von $A$**.

> [!info] Schreibweise
> Neben $\det(A)$ ist auch die Schreibweise mit senkrechten Strichen üblich, z. B. $\det\begin{pmatrix} a & b \\ c & d \end{pmatrix} = \begin{vmatrix} a & b \\ c & d \end{vmatrix}$.
