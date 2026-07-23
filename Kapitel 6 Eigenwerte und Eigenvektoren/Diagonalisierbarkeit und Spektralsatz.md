---
tags: [kapitel-6, thema, definition, satz, beispiel]
quelle: Skript S. 92–95
aliases: [Diagonalisierbarkeit, Spektralsatz, Diagonalmatrix, Geometrische Vielfachheit, Algebraische Vielfachheit]
---
# Diagonalisierbarkeit und Spektralsatz

> Kapitel 6 · Eigenwerte und Eigenvektoren. Zurück zum [[Inhaltsverzeichnis]].
> Voriges Thema: [[Eigenwerte, Eigenvektoren, Eigenräume]] · Nächstes Thema: [[Norm und Skalarprodukt]] (Kapitel 7)
> Grundlage: [[Eigenwert und Eigenvektor]], [[Matrix]], [[Matrixinverse]], [[Linearkombinationen und lineare (Un-)Abhängigkeit]]

## Definition 6.7 (Diagonalisierbarkeit)

Eine Matrix $A \in M_n(K)$ heißt **diagonalisierbar**, wenn eine invertierbare Matrix $S \in M_n(K)$ existiert, so dass

$$A = SDS^{-1}$$

gilt, wobei

$$D = \begin{pmatrix} \lambda_1 & & 0 \\ & \ddots & \\ 0 & & \lambda_n \end{pmatrix}$$

eine **Diagonalmatrix** ist, deren Einträge $\lambda_i$ auf der Diagonalen die Eigenwerte von $A$ sind. Da $S$ invertierbar ist, lässt sich die Gleichung $A = SDS^{-1}$ umformen, es gilt also auch

$$D = S^{-1}AS.$$

Die Darstellung einer Matrix als Produkt $SDS^{-1}$ ist unter anderem (vgl. Anwendungen 6.5 in [[Eigenwerte, Eigenvektoren, Eigenräume]]) zur Berechnung ihrer Potenzen hilfreich. Lässt sich jede quadratische Matrix derart darstellen, ist also jede quadratische Matrix diagonalisierbar? Der folgende Satz beantwortet diese Frage.

## Satz 6.8 (Spektralsatz)

**(a)** Eine Matrix $A \in M_n(K)$ ist diagonalisierbar genau dann, wenn sie $n$ linear unabhängige Eigenvektoren besitzt.
$$A \in M_n(K) \text{ diagonalisierbar} \iff \exists\ n \text{ l.u. Eigenvektoren von } A.$$

**(b)** Besitzt $A$ genau $n$ verschiedene Eigenwerte, so ist $A$ diagonalisierbar.
$$A \in M_n(K) \text{ diagonalisierbar} \impliedby A \text{ besitzt } n \text{ verschiedene Eigenwerte.}$$

> [!note]- Beweis
> **(a)** Sei $A$ diagonalisierbar, d. h., es existiert eine invertierbare Matrix $S$ mit
> $$S^{-1}AS = \begin{pmatrix} \lambda_1 & & 0 \\ & \ddots & \\ 0 & & \lambda_n \end{pmatrix}.$$
> Multiplikation dieser Gleichung von links mit $S$ ergibt
> $$AS = S \begin{pmatrix} \lambda_1 & & 0 \\ & \ddots & \\ 0 & & \lambda_n \end{pmatrix}.$$
> Für die $i$-te Spalte $s_i$ von $S$ gilt dann
> $$As_i = \lambda_i s_i \quad \text{für alle } i \in \{1, \dots, n\}.$$
> Also ist $s_i$ Eigenvektor zum Eigenwert $\lambda_i$ von $A$. Nach Satz 4.26 gilt, dass die Matrix $S$ genau dann invertierbar ist, wenn ihre Spalten $s_1, \dots, s_n$ linear unabhängig sind. Das ist genau die Aussage des Satzes.
>
> **(b)** Wir zeigen mittels vollständiger Induktion, dass die zugehörigen Eigenvektoren linear unabhängig sind. Die Behauptung folgt dann aus Teil (a).
> Seien $\lambda_1, \dots, \lambda_n$ paarweise verschiedene Eigenwerte von $A$ und $v_1, \dots, v_n$ jeweils dazugehörige Eigenvektoren. Zu zeigen ist, dass $v_1, \dots, v_n$ linear unabhängig sind.
>
> **Induktionsanfang:** Für $n = 1$ gilt die Aussage: Nach Definition eines Eigenvektors ist $v_1$ nicht der Nullvektor, also linear unabhängig.
>
> **Induktionsschritt von $n-1$ auf $n$:** Es seien $v_1, \dots, v_{n-1}$ linear unabhängig (Induktionsvoraussetzung). Wir nehmen an, die Vektoren $v_1, \dots, v_n$ sind linear abhängig (und wollen das zu einem Widerspruch führen). Dann lässt sich $v_n$ als Linearkombination von $v_1, \dots, v_{n-1}$ darstellen, also
> $$v_n = \sum_{i=1}^{n-1} a_i v_i$$
> mit $a_i \in K$, und damit gilt
> $$\lambda_n v_n = \sum_{i=1}^{n-1} \lambda_n a_i v_i.$$
> Andererseits gilt aber, da $v_n$ Eigenvektor zum Eigenwert $\lambda_n$ von $A$ ist,
> $$\lambda_n v_n = A v_n = \sum_{i=1}^{n-1} a_i A v_i = \sum_{i=1}^{n} a_i \lambda_i v_i.$$
> Ein Koeffizientenvergleich liefert (da $v_1, \dots, v_{n-1}$ linear unabhängig sind), dass mindestens ein $a_i$ ungleich $0$ sein muss. Daraus folgt aber, dass dann $\lambda_i = \lambda_n$ gilt, was ein Widerspruch zur Annahme ist, dass die Eigenwerte paarweise verschieden sind. Damit sind also auch $v_1, \dots, v_n$ linear unabhängig. $\qquad \blacksquare$

> [!warning] Achtung — nur hinreichend
> Teil (b) ist nur eine **hinreichende**, keine notwendige Bedingung: Es gibt diagonalisierbare Matrizen, die *nicht* $n$ verschiedene Eigenwerte besitzen (siehe Bemerkung 6.9).

## Bemerkung 6.9 (zu Satz 6.8(b))

Es gibt auch diagonalisierbare Matrizen, die nicht $n$ verschiedene Eigenwerte besitzen. Beispielsweise ist die Einheitsmatrix $E_n$ bereits in Diagonalform:

$$E_n = \begin{pmatrix} 1 & & 0 \\ & \ddots & \\ 0 & & 1 \end{pmatrix} = \underbrace{\begin{pmatrix} 1 & & 0 \\ & \ddots & \\ 0 & & 1 \end{pmatrix}}_{S} \underbrace{\begin{pmatrix} 1 & & 0 \\ & \ddots & \\ 0 & & 1 \end{pmatrix}}_{D} \underbrace{\begin{pmatrix} 1 & & 0 \\ & \ddots & \\ 0 & & 1 \end{pmatrix}}_{S^{-1}}.$$

Das charakteristische Polynom von $E_n$ ist $p_{E_n}(\lambda) = (1-\lambda)^n$; die Nullstelle $\lambda = 1$ tritt $n$-fach auf, $\lambda = 1$ ist also Eigenwert mit algebraischer Vielfachheit $n$ (die Matrix besitzt nicht $n$ verschiedene Eigenwerte, sondern nur einen, der $n$-fach vorkommt). Die Eigenvektoren sind die kanonischen Einheitsvektoren.

## Definition/Bemerkung 6.10 (Geometrische Vielfachheit)

Ist $\lambda \in K$ Eigenwert von $A \in M_n(K)$, so heißt

$$\dim \operatorname{Eig}_A(\lambda) \ (\geq 1)$$

die **geometrische Vielfachheit** von $\lambda$. Sie muss nicht mit der algebraischen Vielfachheit von $\lambda$ übereinstimmen (sie ist immer kleiner gleich der algebraischen Vielfachheit).

Für $A \in M_n(K)$ gilt folgender **Satz**:

> [!info] Diagonalisierbarkeitskriterium
> $A$ ist genau dann diagonalisierbar, wenn für **jeden** Eigenwert von $A$ algebraische und geometrische Vielfachheit übereinstimmen.

Im Beispiel von Bemerkung 6.9 hatten wir gesehen, dass die Einheitsmatrix $E_n$ diagonalisierbar ist. Hier war $\lambda = 1$ Eigenwert mit algebraischer Vielfachheit $n$. Gleichzeitig ist $\dim \operatorname{Eig}_{E_n}(\lambda) = n$ (alle Vektoren des $K^n$ werden von $E_n$ gestreckt mit Faktor $\lambda = 1$), also ist die geometrische Vielfachheit auch $n$.
