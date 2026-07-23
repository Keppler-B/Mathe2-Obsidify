---
tags: [kapitel-2, definition, kernbegriff]
quelle: Skript S. 21–22
---
# Ring

> Namensgebende Struktur von Kapitel 2 — eine Menge mit **zwei** Verknüpfungen. Baut auf [[Gruppe]] und [[Verknüpfung und Abgeschlossenheit]] auf und wird von [[Körper]], [[Polynomringe]], [[Der Körper der komplexen Zahlen]] und [[Vektorraum]] verwendet.
> Zurück: [[Ringe]] · [[Inhaltsverzeichnis]]

## Definition 2.1 (Ring)

Sei $R \neq \emptyset$ eine Menge mit zwei Verknüpfungen $+, \cdot$.

**(a)** Das Tripel $(R, +, \cdot)$ heißt **Ring**, falls gilt

1. $(R, +)$ ist eine [[Gruppe|abelsche Gruppe]].[^kain] Das neutrale Element bezeichnen wir hier mit $0$, das zu $a \in R$ inverse Element mit $-a$. Wir schreiben im Folgenden daher auch manchmal $a - b$ für $a + (-b)$.
2. $(R, \cdot)$ ist eine [[Gruppe|Halbgruppe]].[^halbgruppe] Statt $a \cdot b$ schreibt man auch $ab$ (für $a, b \in R$).
3. Es gelten die **Distributivgesetze**:
$$a \cdot (b + c) = (a \cdot b) + (a \cdot c) \overset{(\ast)}{=} ab + ac$$
$$(a + b) \cdot c = (a \cdot c) + (b \cdot c) \overset{(\ast)}{=} ac + bc$$
für alle $a, b, c \in R$.

> [!info] $(\ast)$ Punkt-vor-Strich
> Wir legen die „Punkt-vor-Strich"-Regel fest: $\cdot$ bindet stärker als $+$. Damit können wir beim Ausdruck $(a \cdot b) + (a \cdot c)$ die Klammern weglassen und auch einfach $a \cdot b + a \cdot c$ (oder $ab + ac$) schreiben, analog für $(a \cdot c) + (b \cdot c) = ac + bc$.
> Ist die multiplikative Verknüpfung kommutativ, so muss für das Distributivgesetz nur eine der beiden Gleichungen nachgewiesen werden, die Gültigkeit der anderen folgt dann.

**(b)** $(R, +, \cdot)$ heißt **kommutativ**, falls $\cdot$ ebenfalls kommutativ ist, also $a \cdot b = b \cdot a$ für alle $a, b \in R$ gilt.

**(c)** $(R, +, \cdot)$ heißt **Ring mit Eins**, falls $(R, \cdot)$ eine Halbgruppe ist, in der ein neutrales Element $1 \neq 0$ existiert mit
$$a \cdot 1 = 1 \cdot a = a \quad \text{für alle } a \in R.$$

**(d)** Ist $(R, +, \cdot)$ Ring mit Eins, so heißen die bezüglich $\cdot$ invertierbaren Elemente **Einheiten**. Das zu $a \in R$ bezüglich $\cdot$ inverse Element bezeichnen wir mit $a^{-1}$. Mit $R^*$ bezeichnen wir die **Menge der Einheiten** in $R$. (Die Menge $R^*$ bildet also bezüglich $\cdot$ eine Gruppe, vgl. [[Restklassen modulo m als Gruppe|Bemerkung 1.28]] zu $\mathbb{Z}_m^*$.)

[^kain]: Eselsbrücke: **KAIN** — **K**ommutativgesetz, **A**ssoziativgesetz, **I**nverse, **N**eutrales Element.
[^halbgruppe]: d. h., es gelten Abgeschlossenheit und Assoziativgesetz.

> [!tip] Merkhilfe
> Ring $=$ additive **abelsche Gruppe** $(R,+)$ $+$ multiplikative **Halbgruppe** $(R,\cdot)$ $+$ **Distributivgesetze**. Zusätzlich: $\cdot$ kommutativ $\Rightarrow$ *kommutativer Ring*; neutrales Element $1 \neq 0$ für $\cdot$ vorhanden $\Rightarrow$ *Ring mit Eins*.

## Verwendet in

- [[Ringe]] — Beispiele, Rechenregeln (Satz 2.3), Binomialsatz (Bem. 2.4)
- [[Körper]] — ein Körper ist ein spezieller kommutativer Ring mit Eins
- [[Polynomringe]] — $K[x]$ ist ein Ring
- [[Der Körper der komplexen Zahlen]], [[Vektorraum]]
