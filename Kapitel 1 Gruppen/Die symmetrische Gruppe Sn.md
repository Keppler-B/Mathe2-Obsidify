---
tags: [kapitel-1, thema, definition, beispiel]
quelle: Skript S. 7–10
aliases: [Symmetrische Gruppe, Permutationen, Sn]
---
# Die symmetrische Gruppe $S_n$

> Kapitel 1 · Gruppen — erstes Beispiel einer endlichen Gruppe. Zurück zum [[Inhaltsverzeichnis]].
> Voriges Thema: [[Eigenschaften und Rechenregeln]] · Nächstes Thema: [[Restklassen modulo m als Gruppe]]
> Grundlage: [[Gruppe]], [[Abbildungen (injektiv, surjektiv, bijektiv)|bijektive Abbildungen]]

Im Folgenden lernen wir Beispiele für **endliche Gruppen** (Gruppen bestehend aus endlich vielen Elementen) kennen. Unser erstes Beispiel ist die **symmetrische Gruppe** $S_n$, deren Elemente sogenannte **Permutationen** (Umordnungen bzw. Anordnungen von endlich vielen Elementen) sind.

## Vorüberlegung 1.7

Sei $X = \{a, b, c\}$. Wir betrachten Anordnungen der Elemente von $X$, beispielsweise $abc$ oder $cba$ oder $bca$. Es gibt insgesamt sechs verschiedene solcher Anordnungen. Jede davon lässt sich als **bijektive Abbildung** $\sigma : X \to X$ auffassen.

## Definition 1.8 (Permutationen, die Menge $S_n$)

**(a)** Eine **Permutation** ist eine bijektive Abbildung einer endlichen Menge auf sich selbst. Im Allgemeinen verwendet man die Menge $\{1, \dots, n\}$ ($n \in \mathbb{N}$) und schreibt die Permutation

$$\sigma : \{1, \dots, n\} \to \{1, \dots, n\}, \qquad i \mapsto \sigma(i)$$

als **Wertetabelle** der Form

$$\sigma = \begin{pmatrix} 1 & 2 & \dots & n \\ \sigma(1) & \sigma(2) & \dots & \sigma(n) \end{pmatrix}.$$

**(b)** Mit $S_n$ bezeichnen wir die Menge aller Permutationen von $\{1, \dots, n\}$.

## Beispiel 1.9

**(a)** $X = \{1, 2, 3, 4\}$ (hier ist also $n = 4$). Zwei Permutationen aus $S_4$ sind etwa
$$\sigma = \begin{pmatrix} 1 & 2 & 3 & 4 \\ 2 & 3 & 1 & 4 \end{pmatrix} \quad \text{und} \quad \tau = \begin{pmatrix} 1 & 2 & 3 & 4 \\ 4 & 3 & 2 & 1 \end{pmatrix}.$$
Das Element $1 \in X$ wird durch $\sigma$ auf $2$ abgebildet, durch $\tau$ auf $4$; das Element $2 \in X$ wird durch $\sigma$ auf $3$ abgebildet, durch $\tau$ ebenfalls auf $3$, usw.

**(b)** Die identische Abbildung auf $\{1, \dots, n\}$ ist die Permutation $\sigma = \begin{pmatrix} 1 & 2 & 3 & 4 \\ 1 & 2 & 3 & 4 \end{pmatrix} \in S_n$ (d. h. $1 \mapsto 1, 2 \mapsto 2, \dots$).

**(c)**
$$S_1 = \left\{ \begin{pmatrix} 1 \\ 1 \end{pmatrix} \right\}$$
$$S_2 = \left\{ \begin{pmatrix} 1 & 2 \\ 1 & 2 \end{pmatrix}, \begin{pmatrix} 1 & 2 \\ 2 & 1 \end{pmatrix} \right\}$$
$$S_3 = \left\{ \begin{pmatrix} 1 & 2 & 3 \\ 1 & 2 & 3 \end{pmatrix}, \begin{pmatrix} 1 & 2 & 3 \\ 1 & 3 & 2 \end{pmatrix}, \begin{pmatrix} 1 & 2 & 3 \\ 2 & 1 & 3 \end{pmatrix}, \begin{pmatrix} 1 & 2 & 3 \\ 2 & 3 & 1 \end{pmatrix}, \begin{pmatrix} 1 & 2 & 3 \\ 3 & 1 & 2 \end{pmatrix}, \begin{pmatrix} 1 & 2 & 3 \\ 3 & 2 & 1 \end{pmatrix} \right\}$$

## Bemerkung 1.10 (Ordnung von $S_n$)

Es gilt

$$|S_n| = n! = n \cdot (n-1) \cdots 2 \cdot 1.$$

(Beweis durch vollständige Induktion.)

## Definition 1.11 (Produkt von Permutationen)

Wir definieren auf $S_n$ eine [[Verknüpfung und Abgeschlossenheit|Verknüpfung]] $\circ$ über die Hintereinanderausführung (**Komposition**): Für $\sigma, \tau \in S_n$ sei

$$(\sigma \circ \tau)(i) := \sigma(\tau(i)) \quad \text{für alle } i \in \{1, \dots, n\}.$$

$\sigma \circ \tau$ liest man „**$\sigma$ nach $\tau$**": Zuerst wird die Permutation $\tau$ ausgeführt, anschließend die Permutation $\sigma$.

## Bemerkung 1.12 (Abgeschlossenheit)

Die Menge $S_n$ ist bezüglich $\circ$ [[Verknüpfung und Abgeschlossenheit|abgeschlossen]]: Die Verknüpfung zweier Permutationen ergibt wieder eine Permutation. Dies liegt daran, dass die Komposition bijektiver Abbildungen wieder bijektiv ist (Satz aus *Mathematik 1*).

## Beispiel 1.13

Wir betrachten $\sigma = \begin{pmatrix} 1 & 2 & 3 \\ 2 & 3 & 1 \end{pmatrix},\; \tau = \begin{pmatrix} 1 & 2 & 3 \\ 2 & 1 & 3 \end{pmatrix} \in S_3$.

Dann ist
$$\sigma \circ \tau = \begin{pmatrix} 1 & 2 & 3 \\ 3 & 2 & 1 \end{pmatrix} \quad \text{und} \quad \tau \circ \sigma = \begin{pmatrix} 1 & 2 & 3 \\ 1 & 3 & 2 \end{pmatrix}.$$

> [!info]- Rechenweg (wie liest man die Komposition?)
> Für den ersten Eintrag in der unteren Zeile von $\sigma \circ \tau$ beginnen wir in der oberen Zeile von $\tau$ (wegen „$\sigma$ nach $\tau$"): Die $1$ wird durch $\tau$ abgebildet auf $2$. Anschließend wechseln wir in die obere Zeile von $\sigma$ an die Stelle von $2$ und sehen, dass diese $2$ durch $\sigma$ abgebildet wird auf $3$. Insgesamt wird $1$ durch $\sigma \circ \tau$ also abgebildet auf $3$, usw.

Hier ist also $\sigma \circ \tau \neq \tau \circ \sigma$, das **Kommutativgesetz gilt für $\circ$ also nicht**!

## Satz 1.14 (Symmetrische Gruppe)

$(S_n, \circ)$ ist für jedes $n \in \mathbb{N}$ eine [[Gruppe]], die sogenannte **symmetrische Gruppe**. Diese ist für $n \geq 3$ **nicht abelsch**.

> [!note]- Beweis
> - **Assoziativität:** Für die Komposition von Abbildungen gilt bekanntlich das Assoziativgesetz:
>   $$((\sigma \circ \tau) \circ \pi)(i) = \sigma(\tau(\pi(i))) = (\sigma \circ (\tau \circ \pi))(i)$$
>   für alle $i \in \{1, \dots, n\}$, $\sigma, \tau, \pi \in S_n$.
> - **Neutrales Element:** die identische Abbildung $\varepsilon = \begin{pmatrix} 1 & 2 & \dots & n \\ 1 & 2 & \dots & n \end{pmatrix}$, d. h. $\varepsilon(i) = i$ für alle $i$, denn
>   $$(\sigma \circ \varepsilon)(i) = \sigma(\underbrace{\varepsilon(i)}_{i}) = \sigma(i) \quad \text{und} \quad (\varepsilon \circ \sigma)(i) = \varepsilon(\sigma(i)) = \sigma(i),$$
>   also $\sigma \circ \varepsilon = \varepsilon \circ \sigma = \sigma$.
> - **Inverses Element** zu $\sigma = \begin{pmatrix} 1 & \dots & n \\ \sigma(1) & \dots & \sigma(n) \end{pmatrix}$ ist
>   $$\sigma^{-1} : \sigma(1) \mapsto 1, \;\dots,\; \sigma(n) \mapsto n,$$
>   denn damit gilt $\sigma \circ \sigma^{-1} = \sigma^{-1} \circ \sigma = \begin{pmatrix} 1 & 2 & \dots & n \\ 1 & 2 & \dots & n \end{pmatrix} = \varepsilon$.
> - **Kommutativgesetz** ist nicht erfüllt, siehe Beispiel 1.13. $\qquad \blacksquare$

## Beispiel 1.15 (Rechnen in $S_4$)

Wir betrachten $\sigma = \begin{pmatrix} 1 & 2 & 3 & 4 \\ 4 & 1 & 2 & 3 \end{pmatrix},\; \tau = \begin{pmatrix} 1 & 2 & 3 & 4 \\ 2 & 4 & 1 & 3 \end{pmatrix} \in S_4$.

Dann ist
$$\sigma \circ \tau = \begin{pmatrix} 1 & 2 & 3 & 4 \\ 1 & 3 & 4 & 2 \end{pmatrix}, \quad \tau \circ \sigma = \begin{pmatrix} 1 & 2 & 3 & 4 \\ 3 & 2 & 4 & 1 \end{pmatrix}, \quad \sigma \circ \sigma = \sigma^2 = \begin{pmatrix} 1 & 2 & 3 & 4 \\ 3 & 4 & 1 & 2 \end{pmatrix},$$
$$\sigma^{-1} = \begin{pmatrix} 1 & 2 & 3 & 4 \\ 2 & 3 & 4 & 1 \end{pmatrix}, \quad \tau^{-1} = \begin{pmatrix} 1 & 2 & 3 & 4 \\ 3 & 1 & 4 & 2 \end{pmatrix}.$$
Es gilt $\sigma \circ \sigma^{-1} = \sigma^{-1} \circ \sigma = \varepsilon$ und $\sigma \circ \varepsilon = \varepsilon \circ \sigma = \sigma$.

**Gleichungen lösen** (mit [[Eigenschaften und Rechenregeln|Satz 1.6]]): Für welche Permutation $x \in S_4$ gilt $\sigma \circ x = \tau$? (Welche Permutation muss man *vor* $\sigma$ ausführen, um insgesamt $\tau$ zu erhalten?) Mit Satz 1.6(a) ($ax = b \Rightarrow x = a^{-1}b$) gilt

$$x = \sigma^{-1} \circ \tau = \begin{pmatrix} 1 & 2 & 3 & 4 \\ 3 & 1 & 2 & 4 \end{pmatrix}.$$

Ebenso lässt sich die Gleichung $x \circ \sigma = \tau$ mittels Satz 1.6(b) auflösen:

$$x = \tau \circ \sigma^{-1} = \begin{pmatrix} 1 & 2 & 3 & 4 \\ 4 & 1 & 3 & 2 \end{pmatrix}.$$
