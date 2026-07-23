---
tags: [kapitel-4, thema, satz, beispiel]
quelle: Skript S. 78–79
aliases: [Inverse, Matrixinverse, Gauß-Jordan-Algorithmus, invertierbar]
---
# Matrixinverse

> Kapitel 4 · Matrizen und lineare Gleichungssysteme — sechstes Thema. Zurück zum [[Inhaltsverzeichnis]].
> Voriges Thema: [[Gaußsches Eliminationsverfahren zur Bestimmung der Lösung eines LGS]] · Nächstes Thema: [[Definition und Eigenschaften]]
> Grundlage: [[Matrix]], [[Gaußsches Eliminationsverfahren zur Bestimmung der Lösung eines LGS]], [[Zeilen- und Spaltenrang]].

Eine weitere Anwendung des Gauß-Algorithmus ist die Berechnung der **multiplikativ Inversen** einer Matrix. Wir hatten früher schon überlegt, dass nur quadratische Matrizen eine Inverse besitzen können (aber auch für diese Matrizen muss nicht unbedingt eine Inverse existieren). Falls eine quadratische Matrix eine Inverse besitzt, lässt sich diese mit dem folgenden Verfahren berechnen.

## Bemerkung 4.25 (Gauß-Jordan-Algorithmus)

Gegeben sei das LGS

$$Ax = b$$

mit der quadratischen Matrix $A \in M_n(K)$ mit $\operatorname{rg}(A) = n$ und dem Vektor $b \in K^n$.
Nach [[Gaußsches Eliminationsverfahren zur Bestimmung der Lösung eines LGS#Korollar 4.21 (Zusammenhang von Lösungsraum und Rang)|4.21(b)]] besitzt dieses LGS genau einen Vektor $x \in K^n$ als Lösung, dieser kann mittels des Gaußschen Eliminationsverfahrens (4.12 bzw. 4.20) gefunden werden.

Statt nur auf Zeilenstufenform kann man $(A, b)$ durch elementare Zeilenumformungen auch auf die Form $(E_n, b')$ bringen. Dann ist $b'$ genau der gesuchte Lösungsvektor $x$.

**Beispiel:** Wir betrachten das LGS $\begin{cases} 2x_1 + x_2 = 10 \\ x_1 + 3x_2 = 15 \end{cases}$ über $\mathbb{R}$.

$$(A, b) = \left( \begin{array}{cc|c} 2 & 1 & 10 \\ 1 & 3 & 15 \end{array} \right) \xrightarrow{\mathrm{II}:\ \mathrm{I} - 2 \cdot \mathrm{II}} \left( \begin{array}{cc|c} 2 & 1 & 10 \\ 0 & -5 & -20 \end{array} \right) \xrightarrow{\mathrm{II}:\ \mathrm{II} \cdot (-\frac{1}{5})} \left( \begin{array}{cc|c} 2 & 1 & 10 \\ 0 & 1 & 4 \end{array} \right)$$
$$\xrightarrow{\mathrm{I}:\ \mathrm{I} - \mathrm{II}} \left( \begin{array}{cc|c} 2 & 0 & 6 \\ 0 & 1 & 4 \end{array} \right) \xrightarrow{\mathrm{I}:\ \mathrm{I} \cdot \frac{1}{2}} \left( \begin{array}{cc|c} 1 & 0 & 3 \\ 0 & 1 & 4 \end{array} \right)$$

Damit ist also $\begin{pmatrix} x_1 \\ x_2 \end{pmatrix} = \begin{pmatrix} 3 \\ 4 \end{pmatrix}$ die gesuchte Lösung.

Dieses Verfahren wird **Gauß-Jordan-Algorithmus** genannt.

## Berechnung der Inversen $A^{-1}$

Ähnlich lässt sich die Inverse $A^{-1} \in M_n(K)$ einer Matrix $A \in M_n(K)$ berechnen, falls $A$ tatsächlich invertierbar ist:

Gegeben sei die Gleichung

$$A \cdot X = E_n$$

mit $A, E_n \in M_n(K)$. Gesucht ist die Matrix $X \in M_n(K)$ (also die Inverse $A^{-1}$ von $A$).

Wir bringen die erweiterte Koeffizientenmatrix $(A, E_n)$ mittels elementarer Zeilenumformungen auf die Form $(E_n, E_n')$. Dann ist $E_n'$ genau die gesuchte Lösungsmatrix $X$, also die Inverse $A^{-1}$.

**Beispiel:** $A = \begin{pmatrix} 2 & 1 \\ 1 & 3 \end{pmatrix}$ über $\mathbb{R}$, gesucht ist $A^{-1}$ mit $A \cdot A^{-1} = \begin{pmatrix} 1 & 0 \\ 0 & 1 \end{pmatrix}$.

$$\left( \begin{array}{cc|cc} 2 & 1 & 1 & 0 \\ 1 & 3 & 0 & 1 \end{array} \right) \xrightarrow{\mathrm{II}:\ \mathrm{II} \cdot 2} \left( \begin{array}{cc|cc} 2 & 1 & 1 & 0 \\ 2 & 6 & 0 & 2 \end{array} \right) \xrightarrow{\mathrm{II}:\ \mathrm{I} - \mathrm{II}} \left( \begin{array}{cc|cc} 2 & 1 & 1 & 0 \\ 0 & -5 & 1 & -2 \end{array} \right)$$
$$\xrightarrow{\mathrm{II}:\ \mathrm{II} \cdot (-\frac{1}{5})} \left( \begin{array}{cc|cc} 2 & 1 & 1 & 0 \\ 0 & 1 & -\frac{1}{5} & \frac{2}{5} \end{array} \right) \xrightarrow{\mathrm{I}:\ \mathrm{I} - \mathrm{II}} \left( \begin{array}{cc|cc} 2 & 0 & \frac{6}{5} & -\frac{2}{5} \\ 0 & 1 & -\frac{1}{5} & \frac{2}{5} \end{array} \right) \xrightarrow{\mathrm{I}:\ \mathrm{I} \cdot \frac{1}{2}} \left( \begin{array}{cc|cc} 1 & 0 & \frac{3}{5} & -\frac{1}{5} \\ 0 & 1 & -\frac{1}{5} & \frac{2}{5} \end{array} \right)$$

Die gesuchte Matrix ist also

$$A^{-1} = \begin{pmatrix} \frac{3}{5} & -\frac{1}{5} \\ -\frac{1}{5} & \frac{2}{5} \end{pmatrix},$$

und es gilt $A A^{-1} = A^{-1} A = E_2$.

Dieses Vorgehen beweist im Wesentlichen folgenden Satz.

## Satz 4.26 (Charakterisierung invertierbarer Matrizen)

Sei $A \in M_n(K)$ eine quadratische Matrix. Dann gilt

$$A \text{ ist invertierbar} \iff \operatorname{rg}(A) = n.$$

> [!note]- Beweis
> **„$\Rightarrow$"** Sei $A$ invertierbar. Dann gilt
> $$\begin{aligned} n = \operatorname{rg}(E_n) \quad &\text{(da $E_n$ schon in Zeilenstufenform mit $n$ Stufen ist)} \\ = \operatorname{rg}(A \cdot A^{-1}) \quad & \\ \overset{4.19}{\leq} \operatorname{rg}(A) \quad & \\ \leq n. \quad & \end{aligned}$$
> Daraus folgt, dass $\operatorname{rg}(A) = n$ gelten muss.
> **„$\Leftarrow$"** Folgt aus 4.20, 4.21 und 4.25. $\qquad \blacksquare$

Im folgenden Kapitel über [[Definition und Eigenschaften|Determinanten]] werden wir ein weiteres Kriterium für die Invertierbarkeit einer Matrix kennenlernen (siehe [[Invertierbarkeit und Determinante]]).
