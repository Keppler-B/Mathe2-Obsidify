---
tags: [kapitel-4, thema, definition, beispiel]
quelle: Skript S. 59–61
aliases: [Matrizen, Matrixoperationen, Matrixaddition, Matrixmultiplikation]
---
# Matrizen und Operationen mit Matrizen

> Kapitel 4 · Matrizen und lineare Gleichungssysteme — erstes Thema. Zurück zum [[Inhaltsverzeichnis]].
> Voriges Thema: [[Erzeugte Unterräume, Schnitt und Summe von Unterräumen]] · Nächstes Thema: [[Lineare Gleichungssysteme]]
> Grundlage: [[Körper]], [[Vektorraum]], [[Ring]]. Atomare Definition: [[Matrix]].

Matrizen spielen in der Mathematik und der Informatik in vielen Bereichen eine wichtige Rolle. Durch sie lassen sich lineare Zusammenhänge mehrerer Variablen übersichtlich darstellen, beispielsweise im Zusammenhang mit **linearen Abbildungen** oder **linearen Gleichungssystemen**.

Die zentrale Definition (Notation $A \in K^{m \times n}$ bzw. $M_{m,n}(K)$, Transponierte, Nullmatrix, Einheitsmatrix, Matrixprodukt, Ring der quadratischen Matrizen) ist in der atomaren Datei [[Matrix]] gepflegt und hier eingebunden:

![[Matrix#Definition 4.1 (Matrix)]]

## Beispiel 4.2

**(a)** $A = \begin{pmatrix} 1 & 2 & 3 \\ -1 & 0 & 2 \end{pmatrix} \in M_{2,3}(\mathbb{R})$, $\quad B = \begin{pmatrix} 0 & 0 & -3 \\ 1 & 0 & 1 \end{pmatrix} \in M_{2,3}(\mathbb{R})$

- $A + B = \begin{pmatrix} 1 & 2 & 0 \\ 0 & 0 & 3 \end{pmatrix}$
- $3 \cdot B = \begin{pmatrix} 0 & 0 & -9 \\ 3 & 0 & 3 \end{pmatrix}$
- $A \cdot B$ ist **nicht definiert**, da $A$ drei Spalten besitzt, $B$ aber nur zwei Zeilen.
- $B^T = \begin{pmatrix} 0 & 1 \\ 0 & 0 \\ -3 & 1 \end{pmatrix} \in M_{3,2}(\mathbb{R})$
- $A \cdot B^T = \begin{pmatrix} -9 & 4 \\ -6 & 1 \end{pmatrix} \in M_{2,2}(\mathbb{R})$
- $B^T \cdot A = \begin{pmatrix} -1 & 0 & 2 \\ 0 & 0 & 0 \\ -4 & -6 & -7 \end{pmatrix} \in M_{3,3}(\mathbb{R})$

An den letzten beiden Rechnungen kann man sehen, dass das **Matrixprodukt im Allgemeinen nicht kommutativ** ist (auch nicht in $M_n(K)$).

**(b)** $A = \begin{pmatrix} 1 & 2 & 0 \end{pmatrix} \in M_{1,3}(\mathbb{Z}_3)$, $\quad B = \begin{pmatrix} 2 \\ 2 \\ 1 \end{pmatrix} \in M_{3,1}(\mathbb{Z}_3)$

- $A \cdot B = \begin{pmatrix} 0 \end{pmatrix}\ (= O_{1,1}) \in M_{1,1}(\mathbb{Z}_3)$. (Eine Zahl ist also auch eine Matrix.)
  *(Rechnung in $\mathbb{Z}_3$: $1 \cdot 2 + 2 \cdot 2 + 0 \cdot 1 = 6 \equiv 0$.)*
- $B \cdot A = \begin{pmatrix} 2 & 1 & 0 \\ 2 & 1 & 0 \\ 1 & 2 & 0 \end{pmatrix} \in M_{3,3}(\mathbb{Z}_3)$
  *(z. B. Eintrag $(1,2) = 2 \cdot 2 = 4 \equiv 1$ in $\mathbb{Z}_3$.)*

## Bemerkung 4.3 (Rechenregeln für Matrizen)

Seien $A, A_1, A_2 \in M_{m,n}(K)$, $B, B_1, B_2 \in M_{n,p}(K)$, $C \in M_{p,q}(K)$ und $\lambda \in K$. Dann gelten die folgenden Rechenregeln (bekannt aus den Kapiteln zu [[Ring|Ringen]] bzw. [[Vektorraum|Vektorräumen]] oder einfach nachzurechnen):

**(a)** $(A \cdot B) \cdot C = A \cdot (B \cdot C)$
**(b)** $(A_1 + A_2) \cdot B = A_1 B + A_2 B$
**(c)** $A \cdot (B_1 + B_2) = A B_1 + A B_2$
**(d)** $(\lambda A) B = \lambda (AB) = A (\lambda B)$
**(e)** $(AB)^T = B^T A^T$
