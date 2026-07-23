---
tags: [kapitel-4, thema, definition, satz]
quelle: Skript S. 69–71
aliases: [Rang, Zeilenrang, Spaltenrang, rg]
---
# Zeilen- und Spaltenrang

> Kapitel 4 · Matrizen und lineare Gleichungssysteme — viertes Thema. Zurück zum [[Inhaltsverzeichnis]].
> Voriges Thema: [[Elementare Zeilenumformungen und Transformation in Zeilenstufenform]] · Nächstes Thema: [[Gaußsches Eliminationsverfahren zur Bestimmung der Lösung eines LGS]]
> Grundlage: [[Matrix]], [[Dimension und Basis]], [[Linearkombinationen und lineare (Un-)Abhängigkeit]].

## Definition 4.14 (Zeilenrang)

Der **Zeilenrang** einer Matrix $A$ ist die Maximalzahl linear unabhängiger Zeilen von $A$.
Das bedeutet: Sind $z_1, \dots, z_m$ die Zeilen von $A$, dann ist der Zeilenrang gleich der Dimension des von den Zeilen aufgespannten Unterraums, also $\dim \langle z_1, \dots, z_m \rangle$.
Der **Spaltenrang** ist analog definiert.

Offensichtlich gilt $\operatorname{Zeilenrang}(A) = \operatorname{Spaltenrang}(A^T)$.

## Satz 4.15 (Invarianz unter Zeilenumformungen)

Elementare Zeilenumformungen ändern den **Zeilenrang** und den **Spaltenrang** einer Matrix nicht.

> [!note]- Beweis
> - **Zeilenrang:** Seien $z_1, \dots, z_m$ die Zeilenvektoren der betrachteten Matrix. Für den von diesen Vektoren erzeugten Unterraum gilt (nach der Definition des erzeugten Unterraums $\langle M \rangle$ als Menge aller Linearkombinationen von Vektoren aus $M$):
>   1. $\langle z_1, \dots, z_m \rangle = \langle z_1, z_2 + \lambda z_1, z_3, \dots, z_m \rangle$ für $\lambda \in K$,
>   2. $\langle z_1, \dots, z_m \rangle = \langle \lambda z_1, z_2, \dots, z_m \rangle$, falls $\lambda \neq 0$,
>   3. $\langle z_1, \dots, z_m \rangle = \langle z_2, z_1, \dots, z_m \rangle$,
>
>   und damit bleibt die Dimension dieser Unterräume durch elementare Zeilenumformungen erhalten.
> - **Spaltenrang:** Wir zeigen exemplarisch, dass die Zeilenumformung (2) den Spaltenrang nicht ändert:
>   Sei o. B. d. A. $n = 2$, dann hat die Matrix die Form $A = \begin{pmatrix} a_{11} & a_{12} \\ \vdots & \vdots \\ a_{m1} & a_{m2} \end{pmatrix}$. Multipliziert man die erste Zeile mit $\lambda \neq 0$, so sind die beiden Spalten $\begin{pmatrix} \lambda a_{11} \\ \vdots \\ a_{m1} \end{pmatrix}$ und $\begin{pmatrix} \lambda a_{12} \\ \vdots \\ a_{m2} \end{pmatrix}$ linear unabhängig genau dann, wenn $\begin{pmatrix} a_{11} \\ \vdots \\ a_{m1} \end{pmatrix}$ und $\begin{pmatrix} a_{12} \\ \vdots \\ a_{m2} \end{pmatrix}$ linear unabhängig sind.
>   Analog lässt sich für die elementaren Zeilenumformungen (1) und (3) argumentieren. $\qquad \blacksquare$

## Bemerkung 4.16 (Rang aus der Zeilenstufenform ablesen)

Bei einer Matrix in **Zeilenstufenform** ist der Zeilenrang direkt ablesbar als die **Anzahl der Zeilen** $\neq \mathcal{O}^T$. Beispielsweise hat die Matrix in [[Elementare Zeilenumformungen und Transformation in Zeilenstufenform#Beispiel 4.13|Beispiel 4.13]] Zeilenrang $3$.

Der Algorithmus zur Transformation in Zeilenstufenform (4.12) liefert also wegen Satz 4.15 (und dem folgenden Satz über den Zusammenhang zwischen Zeilen- und Spaltenrang) ein einfaches Verfahren zur **Rangbestimmung**.

## Satz 4.17 (Zeilenrang = Spaltenrang)

Für jede Matrix $A \in M_{m,n}(K)$ gilt: $\operatorname{Zeilenrang}(A) = \operatorname{Spaltenrang}(A)$.

> [!note]- Beweis
> Bringe $A$ mit 4.12 auf Zeilenstufenform. Sei $r$ die Anzahl der Stufen. Dann sind die **Stufenspalten** $s_{j_1}, \dots, s_{j_r}$ (die Spalten, die eine führende Eins enthalten) linear unabhängig.
> (Sei $\lambda_1 s_{j_1} + \cdots + \lambda_r s_{j_r} = \mathcal{O}$. Da der Eintrag $a_{j_r}$ — die führende Eins der Spalte, die zur $r$-ten Stufe gehört — ungleich null ist, muss $\lambda_r = 0$ gelten. Analog gilt dann $\lambda_{r-1} = 0$ (benutze $\lambda_r = 0$ und $a_{j_{r-1}} \neq 0$), usw., bis wir schließlich erhalten, dass auch $\lambda_1$ und damit alle Koeffizienten der Linearkombination gleich null sein müssen.)
> Also gilt:
> $$\begin{aligned} \operatorname{Spaltenrang}(A) &\geq r && \text{(da wir $r$ lin. unabh. Vektoren gefunden haben, evtl. gibt es noch mehr)} \\ &= \operatorname{Zeilenrang}(A) && \text{(Anzahl der Stufen ist $r$)} \\ &= \operatorname{Spaltenrang}(A^T) \\ &\geq \operatorname{Zeilenrang}(A^T) \\ &= \operatorname{Spaltenrang}(A). \end{aligned}$$
> Es gilt also überall Gleichheit, woraus die Behauptung folgt. $\qquad \blacksquare$

Motiviert durch diesen Satz spricht man normalerweise nur vom **Rang** einer Matrix.

## Definition 4.18 (Rang einer Matrix)

Der Wert $\operatorname{Zeilenrang}(A) = \operatorname{Spaltenrang}(A)$ heißt **Rang von $A$**, wir schreiben dafür $\operatorname{rg}(A)$.

Folgende Eigenschaften des Rangs brauchen wir später im Zusammenhang mit der [[Matrixinverse|Inversen]] einer quadratischen Matrix.

## Satz 4.19 (Rang eines Matrixprodukts)

Für $A \in M_{m,n}(K)$, $B \in M_{n,p}(K)$ gilt:

$$\operatorname{rg}(AB) \leq \operatorname{rg}(A) \quad \text{und} \quad \operatorname{rg}(AB) \leq \operatorname{rg}(B).$$

Der Satz besagt: Durch die Multiplikation mit einer weiteren Matrix kann sich der Rang einer Matrix **nicht vergrößern**.

> [!note]- Beweis
> - Seien $a_1, \dots, a_n$ die Spalten von $A$ und $b_1, \dots, b_p$ die Spalten von $B$, dann gilt für das Matrixprodukt $A \cdot B$ in Spaltenschreibweise
>   $$A \cdot B = (A \cdot b_1, \dots, A \cdot b_p). \qquad (\star)$$
>   Außerdem gilt
>   $$A \cdot b_j = (a_1, \dots, a_n) \cdot \begin{pmatrix} b_{1j} \\ \vdots \\ b_{nj} \end{pmatrix} = b_{1j} \cdot a_1 + \cdots + b_{nj} \cdot a_n \quad \text{für } 1 \leq j \leq p.$$
>   (Diesen Zusammenhang sieht man erst, wenn man die Gleichung einmal konkret nachrechnet.)
>   Also liegt $A \cdot b_j$ für jedes $j \in \{1, \dots, p\}$ im Unterraum $\langle a_1, \dots, a_n \rangle$, der von den Spalten von $A$ erzeugt wird. Mit Gleichung $(\star)$ folgt, dass
>   $$\operatorname{rg}(AB) \leq \dim \langle a_1, \dots, a_n \rangle = \operatorname{rg}(A)$$
>   gelten muss.
> - Die zweite Ungleichung ergibt sich aus der ersten, indem man ausnutzt, dass Zeilen- und Spaltenrang gleich sind, also der Rang einer Matrix gleich dem Rang der transponierten Matrix ist:
>   $$\operatorname{rg}(AB) \overset{4.17}{=} \operatorname{rg}\left((AB)^T\right) = \operatorname{rg}(B^T A^T) \underset{\text{eben gezeigte Ungl.}}{\leq} \operatorname{rg}(B^T) \overset{4.17}{=} \operatorname{rg}(B). \qquad \blacksquare$$
