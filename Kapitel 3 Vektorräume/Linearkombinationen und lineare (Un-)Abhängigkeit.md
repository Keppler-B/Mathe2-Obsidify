---
tags: [kapitel-3, thema, definition, beispiel]
quelle: Skript S. 44–46
aliases: [Linearkombination, lineare Unabhängigkeit, lineare Abhängigkeit, LK]
---
# Linearkombinationen und lineare (Un-)Abhängigkeit

> Kapitel 3 · Vektorräume. Zurück zum [[Inhaltsverzeichnis]].
> Voriges Thema: [[Untervektorräume]] · Nächstes Thema: [[Dimension und Basis]]
> Grundlage: [[Vektorraum]]

Wir werden nun die Vektoren eines Vektorraums genauer untersuchen. Dabei interessiert uns, ob oder wie sich Vektoren aus anderen Vektoren „zusammenbauen" lassen. Aus dieser Überlegung entsteht das Konzept der linearen Abhängigkeit von Vektoren, das später zum Begriff einer [[Dimension und Basis|Basis und der Dimension]] eines Vektorraums führt.

Im Folgenden sei immer $V$ mit $K, +, \cdot$ ein [[Vektorraum]].

## Definition 3.9 (Linearkombination, lineare Unabhängigkeit)

**(a)** Seien $v_1, \dots, v_m \in V$. Ein Vektor $v \in V$ heißt **Linearkombination (LK)** von $v_1, \dots, v_m$, wenn es Skalare $\lambda_1, \dots, \lambda_m \in K$ gibt mit
$$v = \lambda_1 v_1 + \cdots + \lambda_m v_m \quad \left( = \sum_{i=1}^m \lambda_i v_i \right).$$

**(b)** Die Vektoren $v_1, \dots, v_m \in V$ heißen **linear abhängig (l. a.)**, wenn es $\lambda_1, \dots, \lambda_m \in K$ gibt, **nicht alle gleich $0$**, so dass
$$\lambda_1 v_1 + \cdots + \lambda_m v_m = \mathcal{O}$$
gilt. Gibt es solche Skalare nicht, heißen $v_1, \dots, v_m$ **linear unabhängig (l. u.)**.

**(c)** Analog nennt man die Menge $\{v_1, \dots, v_m\}$ linear abhängig bzw. linear unabhängig. Die leere Menge $\emptyset$ definieren wir als linear unabhängig.

## Bemerkung 3.10

Die Vektoren $v_1, \dots, v_m \in V$ sind also **linear unabhängig**, wenn aus $\sum_{i=1}^m \lambda_i v_i = \mathcal{O}$ folgt, dass $\lambda_1 = \cdots = \lambda_m = 0$ (d. h., $\mathcal{O}$ lässt sich nur auf triviale Weise $0 \cdot v_1 + \cdots + 0 \cdot v_m$ als Linearkombination darstellen).

Die Vektoren $v_1, \dots, v_m$ sind **linear abhängig**, falls sich $\mathcal{O}$ als nicht-triviale Linearkombination (d. h., mindestens eines der verwendeten Skalare ist ungleich $0$) darstellen lässt.

## Beispiel 3.11

**Zu Definition 3.9(a):**

**(a)** Im $K$-Vektorraum $V = K^n$ ist jeder Vektor $v \in V$ Linearkombination von $e_1, \dots, e_n$, den **kanonischen Einheitsvektoren**, wobei
$$e_i = \begin{pmatrix} 0 \\ \vdots \\ 0 \\ 1 \\ 0 \\ \vdots \\ 0 \end{pmatrix} \leftarrow i\text{-te Stelle.}$$

Zum Beispiel ist
$$\begin{pmatrix} 3 \\ 7 \\ -1 \end{pmatrix} = 3 \cdot \underbrace{\begin{pmatrix} 1 \\ 0 \\ 0 \end{pmatrix}}_{e_1} + 7 \cdot \underbrace{\begin{pmatrix} 0 \\ 1 \\ 0 \end{pmatrix}}_{e_2} - 1 \cdot \underbrace{\begin{pmatrix} 0 \\ 0 \\ 1 \end{pmatrix}}_{e_3} \quad \text{in } \mathbb{R}^3.$$

Die Vektoren $e_1, \dots, e_n$ sind **linear unabhängig**:
$$\begin{aligned}
\lambda_1 e_1 + \cdots + \lambda_n e_n = \mathcal{O}
&\iff \lambda_1 \begin{pmatrix} 1 \\ 0 \\ \vdots \\ 0 \end{pmatrix} + \cdots + \lambda_n \begin{pmatrix} 0 \\ \vdots \\ 0 \\ 1 \end{pmatrix} = \mathcal{O} \\
&\iff \begin{pmatrix} \lambda_1 \\ \vdots \\ \lambda_n \end{pmatrix} = \begin{pmatrix} 0 \\ \vdots \\ 0 \end{pmatrix} \\
&\iff \lambda_i = 0 \text{ für alle } i \in \{1, \dots, n\}.
\end{aligned}$$

**Zu Definition 3.9(b):**

**(b)** Im $\mathbb{R}$-Vektorraum $V = \mathbb{R}^2$ sind die Vektoren $v_1 = \begin{pmatrix} 1 \\ 1 \end{pmatrix},\; v_2 = \begin{pmatrix} 1 \\ 2 \end{pmatrix}$ linear unabhängig:

Seien $\lambda_1, \lambda_2 \in \mathbb{R}$ mit $\lambda_1 v_1 + \lambda_2 v_2 = \begin{pmatrix} 0 \\ 0 \end{pmatrix}$, d. h. $\begin{pmatrix} \lambda_1 + \lambda_2 \\ \lambda_1 + 2\lambda_2 \end{pmatrix} = \begin{pmatrix} 0 \\ 0 \end{pmatrix}$, wir erhalten also die Gleichungen $\lambda_1 + \lambda_2 = 0$ (I) und $\lambda_1 + 2\lambda_2 = 0$ (II).

Aus (I) folgt $\lambda_1 = -\lambda_2$, eingesetzt in (II) ergibt sich $-\lambda_2 + 2\lambda_2 = 0$, was zu $\lambda_2 = 0$ führt und (eingesetzt in (I)) zu $\lambda_1 = 0$.

**(c)** Die Vektoren $\begin{pmatrix} 0 \\ 1 \\ 3 \end{pmatrix}, \begin{pmatrix} 0 \\ 2 \\ 1 \end{pmatrix}$ sind linear abhängig in $\mathbb{Z}_5^3$, da $1 \cdot \begin{pmatrix} 0 \\ 1 \\ 3 \end{pmatrix} + 2 \cdot \begin{pmatrix} 0 \\ 2 \\ 1 \end{pmatrix} = \begin{pmatrix} 0 \\ 0 \\ 0 \end{pmatrix}$.

> [!info]- Warum ergibt das $\mathcal{O}$ (Rechnung mod 5)?
> Entweder man sieht die benötigten Skalare $\lambda_1, \lambda_2$ direkt, oder erkennt, dass $2 \cdot \begin{pmatrix} 0 \\ 1 \\ 3 \end{pmatrix} = \begin{pmatrix} 0 \\ 2 \\ 6 \end{pmatrix} = \begin{pmatrix} 0 \\ 2 \\ 1 \end{pmatrix}$ gilt (in $\mathbb{Z}_5$ ist $6 = 1$), oder man berechnet $\lambda_1, \lambda_2$ wie in Teil (b) aus der Gleichung $\lambda_1 \begin{pmatrix} 0 \\ 1 \\ 3 \end{pmatrix} + \lambda_2 \begin{pmatrix} 0 \\ 2 \\ 1 \end{pmatrix} = \begin{pmatrix} 0 \\ 0 \\ 0 \end{pmatrix}$.
> Probe für $\lambda_1 = 1, \lambda_2 = 2$: zweite Zeile $1 \cdot 1 + 2 \cdot 2 = 5 = 0$, dritte Zeile $1 \cdot 3 + 2 \cdot 1 = 5 = 0$. $\checkmark$

## Bemerkung 3.12

**(a)** Der Nullvektor $\mathcal{O}$ ist linear abhängig: wähle ein beliebiges $0 \neq \lambda \in K$, dann ist $\lambda \cdot \mathcal{O} = \mathcal{O}$, es gibt also eine nicht-triviale Linearkombination des Nullvektors.

**(b)** Ist von den Vektoren $v_1, \dots, v_m \in V$ ein Vektor der Nullvektor, so sind $v_1, \dots, v_m$ linear abhängig. (Sei beispielsweise $v_1 = \mathcal{O}$, dann ist $1 \cdot \mathcal{O} + 0 \cdot v_2 + \cdots + 0 \cdot v_m = \mathcal{O}$, der Nullvektor also als nicht-triviale Linearkombination darstellbar.)

**(c)** Ein einzelner Vektor $0 \neq v \in V$ ist immer linear unabhängig:

> [!note]- Beweis von (c)
> Angenommen, es gibt ein $\lambda \neq 0 \in K$ mit $\lambda \cdot v = \mathcal{O}$. $\quad (\star)$
> Dann ist
> $$\begin{aligned}
> v &\overset{\text{Def. }3.1(2.4)}{=} 1 \cdot v \\
> &\overset{K\text{ Körper}}{=} \left( \lambda^{-1} \cdot \lambda \right) v \\
> &\overset{\text{Def. }3.1(2.1)}{=} \lambda^{-1} (\lambda \cdot v) \\
> &\overset{(\star)}{=} \lambda^{-1} \cdot \mathcal{O} \\
> &\overset{\text{Satz }3.4(b)}{=} \mathcal{O}.
> \end{aligned}$$
> Das ist ein Widerspruch zu $v \neq \mathcal{O}$. $\qquad \blacksquare$

## Beispiel 3.13 (Lineare Abhängigkeit im Funktionenraum $V = \mathcal{F}(\mathbb{R}, \mathbb{R})$)

**(a)** Die Funktionen $f, g : \mathbb{R} \to \mathbb{R}$ mit $f(x) = x,\; g(x) = x^2$ sind linear unabhängig:

Seien $\lambda_1, \lambda_2 \in \mathbb{R}$ mit $\lambda_1 f + \lambda_2 g = \mathcal{O}$. Das bedeutet, dass $\lambda_1 x + \lambda_2 x^2 = 0$ für alle $x \in \mathbb{R}$ gilt, also beispielsweise für $x = 1$, d. h. $\lambda_1 + \lambda_2 = 0$, und für $x = -1$, d. h. $-\lambda_1 + \lambda_2 = 0$. Aus diesen beiden Gleichungen erhält man $\lambda_1 = \lambda_2 = 0$.

**(b)** Die Funktionen $f(x) = \cos^2 x,\; g(x) = \sin^2 x,\; h(x) = 3$ sind linear abhängig, denn (beachte, dass $\cos^2 x + \sin^2 x = 1$)
$$1 \cdot f(x) + 1 \cdot g(x) - \frac{1}{3} \cdot h(x) = \mathcal{O} \quad \text{(Nullfunktion).}$$

## Bemerkung 3.14

Unendlich viele Vektoren aus $V$ heißen **linear unabhängig**, wenn je endlich viele (verschiedene) von ihnen linear unabhängig sind.

Beispielsweise sind in $\mathcal{F}(\mathbb{R}, \mathbb{R})$ die **Monome** $1, x, x^2, \dots$ linear unabhängig:

Sei $x^{k_1}, x^{k_2}, \dots, x^{k_r}$ eine endliche Auswahl dieser Vektoren ($k_i \in \mathbb{N}_0$, alle verschieden) mit $\sum_{j=1}^r \lambda_j x^{k_j} = \mathcal{O}$ (d. h. $\sum_{j=1}^r \lambda_j x^{k_j} = 0$ für alle $x \in \mathbb{R}$). Dann folgt (erzeuge wie in Beispiel 3.13(a) Gleichungen) $\lambda_1 = \cdots = \lambda_r = 0$, da ein reelles Polynom $p(x)$ nur endlich viele Nullstellen besitzt, es sei denn $p(x) \equiv 0$.

## Weiter

- [[Dimension und Basis]] — die maximale Anzahl linear unabhängiger Vektoren als Kennzahl
- [[Erzeugte Unterräume, Schnitt und Summe von Unterräumen]] — Linearkombinationen erzeugen Unterräume
