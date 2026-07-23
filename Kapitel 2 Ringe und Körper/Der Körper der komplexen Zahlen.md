---
tags: [kapitel-2, thema, definition, satz, beispiel]
quelle: Skript S. 30–32
aliases: [Komplexe Zahlen, C, ℂ]
---
# Der Körper der komplexen Zahlen

> Kapitel 2 · Ringe und Körper — $\mathbb{C}$ als weiteres Beispiel eines Körpers. Zurück zum [[Inhaltsverzeichnis]].
> Voriges Thema: [[Polynomringe]] · Unterabschnitt: [[Polarkoordinaten]]
> Grundlage: [[Körper]], [[Ring]].

In diesem Abschnitt lernen wir ein weiteres Beispiel für einen Körper kennen.

## Definition/Satz 2.21 (Die komplexen Zahlen)

**(a)** Eine **komplexe Zahl** $z$ ist von der Form
$$z = a + i \cdot b$$
mit $a, b \in \mathbb{R}$ (auch $z = a + ib$ oder $z = a + bi$) und einer „neuen Zahl" $i$ (die **imaginäre Einheit**[^imag]), für die $i^2 = -1$ gilt.
Die Zahl $a$ nennt man **Realteil** von $z$ (Schreibweise $a = \operatorname{Re}(z)$), die Zahl $b$ heißt **Imaginärteil** von $z$ (Schreibweise $b = \operatorname{Im}(z)$).

[^imag]: Achtung, $i$ ist **kein** Element von $\mathbb{R}$.

Die Menge aller komplexen Zahlen bezeichnet man mit $\mathbb{C}$, es gilt also
$$\mathbb{C} = \{a + i \cdot b \mid a, b \in \mathbb{R}\}.$$
Die reellen Zahlen sind eine **Teilmenge** von $\mathbb{C}$: sie entsprechen genau den komplexen Zahlen, deren Imaginärteil Null ist.

**(b)** Für $z = a + ib \in \mathbb{C}$ heißt $|z| := \sqrt{a^2 + b^2}$ **Betrag** von $z$, die Zahl $\overline{z} := a - ib$ die zu $z$ **Konjugierte** (oder die zu $z$ konjugiert komplexe Zahl).

**(c)** Auf der Menge $\mathbb{C}$ werden die Verknüpfungen $+$ und $\cdot$ folgendermaßen definiert:
Für $z = a + ib$, $w = a' + ib' \in \mathbb{C}$ ist
$$z + w := (a + a') + i(b + b'),$$
$$z \cdot w := (aa' - bb') + i(ab' + ba').$$

> [!info] Motivation der Multiplikation
> Die Definition für die Multiplikation zweier komplexer Zahlen ist motiviert durch das Ergebnis, das man erhält, wenn man $(a + ib) \cdot (a' + ib')$ ausmultipliziert, wie man es von reellen Zahlen gewohnt ist, und dabei $i$ als Zahl betrachtet, für die $i^2 = -1$ gilt:
> $$(a + ib) \cdot (a' + ib') = aa' + aib' + iba' + \underbrace{i^2}_{= -1} bb'$$
> $$= (aa' - bb') + i(ab' + ba').$$

**Damit ist $\mathbb{C}$ ein Körper:**
- Assoziativgesetze, Kommutativgesetze, Distributivgesetze lassen sich mit etwas Arbeit nachrechnen.
- **Nullelement** (neutrales Element bezüglich der Addition) ist die Zahl $0 = 0 + i \cdot 0$.
- Das **additiv Inverse** zu $z = a + ib$ ist $-z = -a + i(-b) = -a - ib$.
- **Einselement** (neutrales Element bezüglich der Multiplikation) ist die Zahl $1 = 1 + i \cdot 0$.
- Das **multiplikativ Inverse** zu $z = a + ib$ ist $z^{-1} = \tfrac{1}{z} = \tfrac{1}{a + ib}$. Um zu sehen, dass diese Zahl tatsächlich von der Form $x + iy$ mit $x, y \in \mathbb{R}$ ist, multiplizieren wir sie mit $\tfrac{a - ib}{a - ib}$ und verwenden $i^2 = -1$:
$$z^{-1} = \frac{1}{z} = \frac{1}{a + ib} = \frac{1}{a + ib} \cdot \frac{a - ib}{a - ib} = \frac{a - ib}{a^2 + b^2} = \underbrace{\frac{a}{a^2 + b^2}}_{\in \mathbb{R}} + i \cdot \underbrace{\frac{-b}{a^2 + b^2}}_{\in \mathbb{R}}.$$

## Beispiel 2.22

**(a)** Für $z = 3 + 4i \in \mathbb{C}$ ist $\operatorname{Re}(z) = 3$, $\operatorname{Im}(z) = 4$, $\overline{z} = 3 - 4i$, $|z| = \sqrt{3^2 + 4^2} = 5$, $z \cdot \overline{z} = 25$.

**(b)** Für $w = 1 + i \in \mathbb{C}$ ist $\operatorname{Re}(w) = 1$, $\operatorname{Im}(w) = 1$, $\overline{w} = 1 - i$, $|w| = \sqrt{1^2 + 1^2} = \sqrt{2}$, $w \cdot \overline{w} = 2$.

**(c)** Für $u = 7 \in \mathbb{C}$ ist $\operatorname{Re}(u) = 7$, $\operatorname{Im}(u) = 0$, $\overline{u} = 7$, $|7| = \sqrt{7^2 + 0^2} = 7$, $u \cdot \overline{u} = 49$.

**(d)** Für $v = 5i \in \mathbb{C}$ ist $\operatorname{Re}(v) = 0$, $\operatorname{Im}(v) = 5$, $\overline{v} = -5i$, $|v| = \sqrt{0^2 + 5^2} = 5$, $v \cdot \overline{v} = 25$.

> [!info]
> Eine Bemerkung/Motivation für $\mathbb{C}$ ist auf den Vorlesungsfolien vom 06.05.2026 zu finden.

## Bemerkung 2.23 (Gaußsche Zahlenebene)

Man kann $\mathbb{C}$ in der **Gaußschen Zahlenebene** veranschaulichen. Betrachte dazu $z = x + iy \in \mathbb{C}$ als Punkt $(x \mid y)$ in $\mathbb{R}^2$:

> [!info] Skizze (Gaußsche Zahlenebene)
> Ein zweidimensionales Koordinatensystem mit
> - **waagrechter Achse:** reelle Achse $\mathbb{R}$ (Realteil $\operatorname{Re}(z) = x$),
> - **senkrechter Achse:** imaginäre Achse $i\mathbb{R}$ (Imaginärteil $\operatorname{Im}(z) = y$).
>
> Die komplexe Zahl $z = x + iy$ entspricht dem Punkt $(x \mid y)$. Die Strecke vom Ursprung $(0 \mid 0)$ zum Punkt $z$ hat die Länge $|z|$; nach dem **Satz des Pythagoras** gilt $|z|^2 = x^2 + y^2$, also $|z| = \sqrt{x^2 + y^2}$.
>
> Die konjugierte Zahl $\overline{z} = x - iy$ ist die **Spiegelung** von $z$ an der reellen Achse; das additiv Inverse $-z = -x - iy$ ist die Punktspiegelung am Ursprung.

In $\mathbb{R}$ beschreibt der Betrag einer reellen Zahl deren Abstand zur Zahl $0$. In $\mathbb{C}$ verhält es sich ebenso: $|z|$ ist gleich dem Abstand des Punkts $z = (x \mid y)$ zum Ursprung $(0 \mid 0)$ im zweidimensionalen Koordinatensystem, $|z| = \sqrt{x^2 + y^2}$.

## Bemerkung 2.24 (Weitere Eigenschaften von $\mathbb{C}$)

**(a)** In $\mathbb{C}$ existiert $\sqrt{-1}$, die Gleichung $x^2 + 1 = 0$ ist in den komplexen Zahlen lösbar. Als Polynom in $\mathbb{C}[x]$ zerfällt $x^2 + 1$ in Linearfaktoren: $x^2 + 1 = (x + i)(x - i)$.

**(b)** Man kann jede quadratische Gleichung $ax^2 + bx + c$ (mit $a, b, c \in \mathbb{R}$) in $\mathbb{C}$ lösen. Für die Lösungen $x_1$ und $x_2$ gilt
$$x_{1,2} = \frac{-b \pm \sqrt{b^2 - 4ac}}{2a}.$$
Falls die Diskriminante $b^2 - 4ac < 0$ ist, schreibe $\dfrac{-b \pm i \cdot \sqrt{4ac - b^2}}{2a}$.
Beispielsweise sind die beiden Lösungen der Gleichung $x^2 + x + 2 = 0$ die Zahlen
$$x_{1,2} = \frac{-1 \pm \sqrt{1^2 - 4 \cdot 1 \cdot 2}}{2} = \frac{-1 \pm \sqrt{-7}}{2} = \frac{-1 \pm i \cdot \sqrt{7}}{2}.$$

**(c)** Der **(Gauß-d'Alembertsche) Fundamentalsatz der Algebra** besagt, dass jedes Polynom $f \in \mathbb{C}[x]$ vom Grad $n \geq 1$ genau $n$ Nullstellen in $\mathbb{C}$ besitzt, d. h., in $n$ Linearfaktoren zerfällt.

**(d)** Der Körper der komplexen Zahlen $\mathbb{C}$ hat alle algebraischen und analytischen Eigenschaften wie $\mathbb{R}$ (und teilweise noch mehr als $\mathbb{R}$), bis auf eine: Es gibt auf $\mathbb{C}$ **keine vollständige Ordnung** $\leq$, die mit $+$ und $\cdot$ verträglich ist, d. h., für die gelten würde
$$a \leq b, \; c \leq d \Rightarrow a + c \leq b + d$$
$$a \leq b, \; r \geq 0 \Rightarrow r \cdot a \leq r \cdot b.$$

## Weiter

- [[Polarkoordinaten]] — zweite Darstellungsform komplexer Zahlen (Betrag und Winkel), Eulersche Formel, Einheitswurzeln
