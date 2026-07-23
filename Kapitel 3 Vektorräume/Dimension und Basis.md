---
tags: [kapitel-3, thema, definition, satz, beispiel]
quelle: Skript S. 47–51
aliases: [Dimension, Basis, kanonische Basis, Koordinaten, geordnete Basis, Koordinatenvektor]
---
# Dimension und Basis

> Kapitel 3 · Vektorräume. Zurück zum [[Inhaltsverzeichnis]].
> Voriges Thema: [[Linearkombinationen und lineare (Un-)Abhängigkeit]] · Nächstes Thema: [[Austauschsatz von Steinitz und Basisergänzungssatz]]
> Grundlage: [[Vektorraum]], [[Linearkombinationen und lineare (Un-)Abhängigkeit]]

Über die maximale Anzahl linear unabhängiger Vektoren eines Vektorraums lässt sich eine Kennzahl für diesen Vektorraum definieren, die **Dimension**. Wie wir in diesem Abschnitt sehen werden, entspricht sie der Anzahl der Vektoren, die benötigt werden, um jeden Vektor des Vektorraums eindeutig als Linearkombination darzustellen.

## Definition 3.15 (Dimension)

Sei $n \in \mathbb{N}$.

**(a)** Falls es $n$ linear unabhängige Vektoren in $V$ gibt, aber je $n + 1$ Vektoren aus $V$ linear abhängig sind, so heißt $n$ die **Dimension von $V$** ($\dim V = n$). Für den Nullraum $V = \{\mathcal{O}\}$ setzen wir $\dim V = 0$.

**(b)** Gibt es in $V$ zu jedem $m \in \mathbb{N}$ (mindestens) $m$ linear unabhängige Vektoren, so heißt $V$ **unendlichdimensional** ($\dim V = \infty$).

Die Zahl $\dim V$ ist also die **Maximalzahl linear unabhängiger Vektoren** in $V$ (falls es eine solche Zahl gibt, andernfalls $\infty$).

## Beispiel 3.16 (Beispiel zu Definition 3.15(b))

Für die Dimension des Funktionenraums $\mathcal{F}(\mathbb{R}, \mathbb{R})$ gilt $\dim \mathcal{F}(\mathbb{R}, \mathbb{R}) = \infty$, denn (siehe Beispiel/Bemerkung 3.14) für jedes $m \in \mathbb{N}_0$ sind $1, x, x^2, \dots, x^m$ linear unabhängig.

## Definition 3.17 (Basis)

Die Vektoren $v_1, \dots, v_n \in V$ (oder auch die Menge $B = \{v_1, \dots, v_n\} \subseteq V$) heißen **Basis von $V$**, falls sich jeder Vektor $w \in V$ **eindeutig** als Linearkombination von $v_1, \dots, v_n$ darstellen lässt, d. h.:

**(1)** Für alle $w \in V$ gilt: es gibt $\lambda_1, \dots, \lambda_n \in K$ mit $w = \sum_{i=1}^n \lambda_i v_i$.

**(2)** Gilt zusätzlich $w = \sum_{i=1}^n \mu_i v_i$ mit $\mu_1, \dots, \mu_n \in K$, so folgt $\mu_1 = \lambda_1, \dots, \mu_n = \lambda_n$.

## Beispiel 3.18

**(a)** Die Vektoren $e_1, \dots, e_n$ bilden eine Basis von $\mathbb{R}^n$ (die sogenannte **kanonische Basis**, mehr dazu in Beispiel 3.22).

**(b)** Die Vektoren $v_1 = \begin{pmatrix} 1 \\ 1 \end{pmatrix},\; v_2 = \begin{pmatrix} 0 \\ 1 \end{pmatrix}$ bilden eine Basis des $\mathbb{R}^2$.

Beispielsweise lässt sich der Vektor $\begin{pmatrix} 5 \\ 7 \end{pmatrix}$ darstellen als $\begin{pmatrix} 5 \\ 7 \end{pmatrix} = 5 \cdot \begin{pmatrix} 1 \\ 1 \end{pmatrix} + 2 \cdot \begin{pmatrix} 0 \\ 1 \end{pmatrix}$.

Allgemein: Sei $w = \begin{pmatrix} w_1 \\ w_2 \end{pmatrix} \in \mathbb{R}^2$ beliebig.

&nbsp;&nbsp;**(1)** $w = \underbrace{w_1}_{=:\lambda_1} \begin{pmatrix} 1 \\ 1 \end{pmatrix} + \underbrace{(w_2 - w_1)}_{=:\lambda_2} \cdot \begin{pmatrix} 0 \\ 1 \end{pmatrix}$, also ist $w$ als LK von $v_1, v_2$ darstellbar (Definition 3.17(1) ist also erfüllt).

&nbsp;&nbsp;**(2)** Sei $w = \mu_1 \begin{pmatrix} 1 \\ 1 \end{pmatrix} + \mu_2 \begin{pmatrix} 0 \\ 1 \end{pmatrix}$, d. h. $w = \begin{pmatrix} w_1 \\ w_2 \end{pmatrix} = \begin{pmatrix} \mu_1 \\ \mu_1 + \mu_2 \end{pmatrix}$, dann folgt $\mu_1 = w_1 = \lambda_1,\; \mu_2 = w_2 - \mu_1 = w_2 - w_1 = \lambda_2$, also ist diese Darstellung eindeutig (Definition 3.17(2) ist also erfüllt).

## Definition/Bemerkung 3.19 (Koordinaten, geordnete Basis)

Sei $B = \{v_1, \dots, v_n\}$ eine Basis von $V$ und sei $w \in V$ gegeben. Weiter seien $\lambda_1, \dots, \lambda_n$ die (eindeutig bestimmten) Skalare mit $w = \lambda_1 v_1 + \cdots + \lambda_n v_n$.

Dann ordnen wir $w$ den Vektor $\begin{pmatrix} \lambda_1 \\ \vdots \\ \lambda_n \end{pmatrix} \in K^n$, den **Koordinatenvektor von $w$** bezüglich der **geordneten Basis** $\widetilde{B} = (v_1, \dots, v_n)$, zu. Die verwendeten Skalare $\lambda_1, \dots, \lambda_n$ heißen dann die **Koordinaten von $w$** bezüglich $\widetilde{B}$.

Im Beispiel 3.18(b) ist $\begin{pmatrix} w_1 \\ w_2 - w_1 \end{pmatrix}$ der Koordinatenvektor von $w$ bezüglich $\widetilde{B} = \left( \begin{pmatrix} 1 \\ 1 \end{pmatrix}, \begin{pmatrix} 0 \\ 1 \end{pmatrix} \right)$.

Hier spielt die Reihenfolge, in der die Basisvektoren aufgelistet werden, eine Rolle, daher der Begriff **geordnete Basis** und die Schreibweise als Tupel (runde Klammern) anstelle der üblichen Schreibweise einer (ungeordneten) Basis als Menge.

Im Falle der kanonischen (geordneten) Basis $\widetilde{B} = (e_1, \dots, e_n)$ des $K$-Vektorraums $K^n$ spricht man von den **kartesischen Koordinaten**.[^descartes] Beispielsweise ist der Koordinatenvektor von $v = \begin{pmatrix} 7 \\ -3 \\ 0 \end{pmatrix} \in \mathbb{R}^3$ bezüglich $\widetilde{B} = (e_1, \dots, e_n)$ gleich $\begin{pmatrix} 7 \\ -3 \\ 0 \end{pmatrix}$, die kartesischen Koordinaten von $v$ sind also $7, -3, 0$.

[^descartes]: benannt nach dem französischen Mathematiker René Descartes

Die Begriffe der Basis und der Dimension eines Vektorraums hängen zusammen. Wie wir in den folgenden Sätzen feststellen werden, entspricht die Anzahl der Vektoren einer Basis genau der Dimension des Vektorraums.

## Satz 3.20 (1. Zusammenhang Dimension/Basis)

Gegeben seien ein Vektorraum $V$ mit $\dim V = n \in \mathbb{N}$ und $n$ linear unabhängige Vektoren[^existenz] $v_1, \dots, v_n \in V$. Dann gilt: Die Menge $\{v_1, \dots, v_n\}$ ist eine Basis von $V$.

[^existenz]: nach der Definition von $\dim V$ existieren solche Vektoren auch tatsächlich

Der Satz besagt also, dass $n$ linear unabhängige Vektoren in einem Vektorraum der Dimension $n$ bereits eine Basis bilden.

> [!note]- Beweis
> Wir zeigen die beiden Eigenschaften einer Basis aus Definition 3.17.
>
> **(1)** Sei $w \in V$ beliebig. Dann sind die $n + 1$ Vektoren $v_1, \dots, v_n, w$ also linear abhängig nach der Definition der Dimension eines Vektorraums (Definition 3.15). Folglich existieren Skalare $\lambda_1, \dots, \lambda_n, \lambda \in K$, nicht alle gleich $0$, mit
> $$\lambda_1 v_1 + \dots + \lambda_n v_n + \lambda w = \mathcal{O}.$$
> Es gilt $\lambda \neq 0$: Andernfalls wäre $\lambda_1 v_1 + \cdots + \lambda_n v_n = \mathcal{O}$, was bedeuten würde (da nicht alle $\lambda_i$ ($1 \leq i \leq n$) gleich $0$ sind), dass $v_1, \dots, v_n$ linear abhängig sind. Damit lässt sich $w$ darstellen als
> $$w = -\lambda_1 \lambda^{-1} v_1 - \cdots - \lambda_n \lambda^{-1} v_n,$$
> also als Linearkombination von $v_1, \dots, v_n$.
>
> **(2)** Sei $w = \sum_{i=1}^n \lambda_i v_i = \sum_{i=1}^n \mu_i v_i$ ($\mu_i, \lambda_i \in K$)
> $$\begin{aligned}
> &\Rightarrow \quad \mathcal{O} = w - w = \sum_{i=1}^n (\lambda_i - \mu_i) v_i \\
> &\overset{v_i\text{ l. u.}}{\Rightarrow} \quad \lambda_i - \mu_i = 0 \text{ für alle } i \\
> &\Rightarrow \quad \lambda_i = \mu_i \text{ für alle } i. \qquad \blacksquare
> \end{aligned}$$

## Satz 3.21

Gegeben seien $m$ Vektoren $v_1, \dots, v_m$ eines Vektorraums. Dann sind je $m + 1$ Linearkombinationen von $v_1, \dots, v_m$ linear abhängig.

Der Satz besagt: Stellt man aus $m$ linear unabhängigen Vektoren weitere $m + 1$ Vektoren (durch Linearkombinationen) her, müssen diese linear abhängig werden; aus $m$ linear unabhängigen Vektoren kann man also nicht mehr als $m$ linear unabhängige Vektoren mittels Linearkombinationen herstellen.

Die Aussage des Satzes wird anschaulicher anhand eines kleinen Beispiels: Wir betrachten zunächst einen einzelnen Vektor $v$ (hier ist also $m = 1$). Die möglichen Linearkombinationen von $v$ sind immer Vielfache von $v$ (die Menge aller $\lambda \cdot v$ mit $\lambda \in K$), und zwei (also $m + 1$) solcher Linearkombinationen sind dann offensichtlich linear abhängig. Diese Überlegung wird im folgenden Beweis als Induktionsanfang benutzt.

> [!note]- Beweis (vollständige Induktion nach $m$)
> **Induktionsanfang ($m = 1$):**
> Sei $v \in V$ gegeben und seien $w_1, w_2$ zwei Linearkombinationen von $v$, also
> $$w_1 = \lambda_1 v, \quad w_2 = \lambda_2 v,$$
> mit $\lambda_1, \lambda_2 \in K$.
>
> *1. Fall:* $\lambda_2 = 0$. Dann ist $w_2 = \mathcal{O}$, und damit sind $w_1, w_2$ linear abhängig (vgl. Bemerkung 3.12(b): ist einer der Vektoren der Nullvektor, so wird die betrachtete Menge von Vektoren linear abhängig).
>
> *2. Fall:* $\lambda_2 \neq 0$. Dann ist $1 \cdot w_1 - \lambda_1 \lambda_2^{-1} w_2 = \lambda_1 v - \lambda_1 v = \mathcal{O}$, und damit sind $w_1, w_2$ ebenfalls linear abhängig (da der Nullvektor auf nicht-triviale Weise als Linearkombination aus diesen beiden Vektoren dargestellt werden kann).
>
> **Induktionsschritt (von $m - 1$ auf $m$):**[^indschritt]
> *Induktionsvoraussetzung:* Folgende Aussage sei wahr für $m \in \mathbb{N}$: Gegeben seien $m - 1$ Vektoren $v_1, \dots, v_{m-1}$ eines $K$-Vektorraums $V$. Dann sind je $m$ Linearkombinationen von $v_1, \dots, v_{m-1}$ linear abhängig.
> *Induktionsbehauptung:* Sind die Vektoren $v_1, \dots, v_m \in V$ gegeben, dann sind je $m + 1$ Linearkombinationen von $v_1, \dots, v_m$ linear abhängig.
> *Beweis der Induktionsbehauptung:* Seien $v_1, \dots, v_m \in V$, und seien $w_1, \dots, w_{m+1}$ Linearkombinationen der Vektoren $v_1, \dots, v_m$. Diese können wir schreiben als
> $$w_i = \underbrace{y_i}_{\text{LK von } v_1, \dots, v_{m-1}} + \lambda_i v_m$$
> mit $\lambda_i \in K$ für $1 \leq i \leq m + 1$. Wir fassen also für jeden Vektor $w_i$ den Teil der Linearkombination als $y_i$ zusammen, der die Vektoren $v_1$ bis $v_{m-1}$ enthält (denn für diesen Teil wollen wir dann die Induktionsvoraussetzung anwenden).
>
> *1. Fall:* $\lambda_1 = \lambda_2 = \cdots = \lambda_{m+1} = 0$, d. h. der hintere Teil der Darstellung der $w_i$ fällt weg, dann sind $w_1, \dots, w_{m-1}$ Linearkombinationen von $v_1, \dots, v_{m-1}$ (der Vektor $v_m$ wird gar nicht gebraucht) und damit nach Induktionsvoraussetzung linear abhängig.
>
> *2. Fall:* Mindestens ein $\lambda_i$ ist ungleich $0$, wir betrachten ohne Beschränkung der Allgemeinheit $\lambda_{m+1} \neq 0$. Setze dann
> $$z_i := w_i - \lambda_i \lambda_{m+1}^{-1} w_{m+1} = y_i - \lambda_i \lambda_{m+1}^{-1} y_{m+1}$$
> für $1 \leq i \leq m$. Die Vektoren $z_1, \dots, z_m$ sind also $m$ Linearkombinationen der $m - 1$ Vektoren $v_1, \dots, v_{m-1}$, also nach Induktionsvoraussetzung linear abhängig. Das heißt, es gibt Skalare $\mu_1, \dots, \mu_m \in K$, nicht alle gleich $0$, mit
> $$\begin{aligned}
> \mathcal{O} = \mu_1 z_1 + \cdots + \mu_m z_m
> = \mu_1 w_1 + \cdots + \mu_m w_m - \left( \mu_1 \lambda_1 \lambda_{m+1}^{-1} + \mu_2 \lambda_2 \lambda_{m+1}^{-1} + \cdots + \mu_m \lambda_m \lambda_{m+1}^{-1} \right) w_{m+1},
> \end{aligned}$$
> also sind $w_1, \dots, w_{m+1}$ linear abhängig. $\qquad \blacksquare$

[^indschritt]: Man kann den Induktionsschritt auch wie gewöhnlich von $m$ auf $m + 1$ durchführen.

## Beispiel 3.22 (Beispiel 3.18(a) genauer)

Im $K$-Vektorraum $V = K^n$ gilt: $e_1, \dots, e_n$ sind linear unabhängig (vgl. Beispiel 3.11(a)), jeder Vektor $v \in V$ ist eine Linearkombination von $e_1, \dots, e_n$ (vgl. Beispiel 3.11(a)), $n + 1$ Vektoren aus $V$ sind also $n + 1$ Linearkombinationen von $e_1, \dots, e_n$ und nach Satz 3.21 linear abhängig. Also ist $\dim V = n$ und nach Satz 3.20 bilden $e_1, \dots, e_n$ eine Basis (die **kanonische Basis**) von $K^n$.

## Satz 3.23 (2. Zusammenhang Dimension/Basis)

Sei $B = \{v_1, \dots, v_n\}$ eine Basis von $V$. Dann sind $v_1, \dots, v_n$ linear unabhängig und $\dim V = n$.

> [!note]- Beweis
> **(1)** Jedes $v \in V$, also auch $\mathcal{O}$, lässt sich eindeutig als Linearkombination von $v_1, \dots, v_n$ schreiben (Definition einer Basis). Die triviale Darstellung $\mathcal{O} = 0 \cdot v_1 + \cdots + 0 \cdot v_n$ ist damit die einzig mögliche, was bedeutet, dass $v_1, \dots, v_n$ linear unabhängig sind.
>
> **(2)** Nach (1) gibt es $n$ linear unabhängige Vektoren in $V$, je $n + 1$ Vektoren sind $n + 1$ Linearkombinationen von $v_1, \dots, v_n$ und nach Satz 3.21 linear abhängig. Damit folgt $\dim V = n$. $\qquad \blacksquare$

## Korollar 3.24 (Anzahl der Vektoren in einer Basis)

Je zwei Basen eines $n$-dimensionalen Vektorraums bestehen aus gleich vielen, nämlich $n$, Vektoren.

> [!tip] Merkregel
> Nach den beiden Sätzen 3.20 und 3.23 gilt also: In einem $n$-dimensionalen Vektorraum bilden $n$ Vektoren **genau dann eine Basis, wenn sie linear unabhängig sind**. Um beispielsweise zu prüfen, ob die Vektoren $\begin{pmatrix} 1 \\ 0 \\ 0 \end{pmatrix}, \begin{pmatrix} 0 \\ 1 \\ 0 \end{pmatrix}, \begin{pmatrix} 1 \\ 1 \\ 1 \end{pmatrix}$ eine Basis des $\mathbb{R}^3$ bilden, reicht es also zu prüfen, ob sie linear unabhängig sind (da wir bereits wissen, dass $\dim \mathbb{R}^3 = 3$ gilt, vgl. Beispiel 3.22).

## Weiter

- [[Austauschsatz von Steinitz und Basisergänzungssatz]] — Basen ineinander umwandeln und ergänzen
- [[Erzeugte Unterräume, Schnitt und Summe von Unterräumen]] — Basis über Erzeugendensysteme (auch für $\dim V = \infty$)
