---
tags: [kapitel-1, thema, satz]
quelle: Skript S. 5–6
---
# Eigenschaften und Rechenregeln

> Kapitel 1 · Gruppen. Zurück zum [[Inhaltsverzeichnis]].
> Voriges Thema: [[Verknüpfungen, Gruppen, erste Beispiele]] · Nächstes Thema: [[Die symmetrische Gruppe Sn]]
> Grundlage: [[Gruppe]]

Ab sofort benutzen wir als Symbol für die Verknüpfung in einer Gruppe meistens $\cdot$ und schreiben statt $a \cdot b$ oftmals einfach nur $ab$. Es muss sich dabei aber nicht unbedingt um die übliche Multiplikation handeln.

Wir haben bisher gesehen, dass es in einer [[Gruppe]] immer ein neutrales Element und zu jedem Element der Gruppe ein inverses Element geben muss. Kann es mehrere neutrale Elemente geben? Und könnten manche Elemente auch mehrere Inverse besitzen? Der folgende Satz gibt darauf Antwort.

## Satz 1.5 (Eigenschaften von Gruppen)

Sei $(G, \cdot)$ eine Gruppe. Dann gelten die folgenden Eigenschaften.

**(a)** Das neutrale Element von $G$ ist eindeutig.
**(b)** Für jedes $a \in G$ gibt es eine eindeutige Inverse.
**(c)** Für alle $a, b \in G$ gilt $(ab)^{-1} = b^{-1} a^{-1}$.

> [!note]- Beweis
> Für die Teile (a) und (b) muss die **Eindeutigkeit** gezeigt werden. Dazu nimmt man jeweils an, dass es zwei solcher Elemente gibt, und zeigt, dass diese dann gleich sein müssen.
>
> **(a)** Angenommen, $e_1, e_2 \in G$ sind neutrale Elemente. Dann gilt
> $$e_1 = e_1 \cdot e_2 = e_2.$$
> (Benutze für beide Gleichungen [[Gruppe|1.3(2)]]: Bei der ersten Gleichheit übernimmt $e_2$ die Rolle von $e$ aus 1.3(2), bei der zweiten Gleichheit übernimmt $e_1$ die Rolle von $e$.)
>
> **(b)** Angenommen, $a \in G$ besitzt zwei Inverse $x$ und $y$. Dann ist
> $$x \;\overset{1.3(2)}{=}\; x(ay) \;\overset{1.3(1)}{=}\; (xa)y \;\overset{1.3(2)}{=}\; y,$$
> wobei $ay = e$ bzw. $xa = e$ benutzt wurde; also gilt $x = y$.
>
> **(c)** Nach [[Gruppe|Definition 1.3(3)]] gilt $(ab)^{-1}(ab) = e$. Wir prüfen nun, ob diese Gleichung auch gilt, wenn wir für $(ab)^{-1}$ das Element $b^{-1}a^{-1}$ einsetzen, das nach Behauptung gerade die Inverse von $(ab)$ ist. Tatsächlich gilt
> $$b^{-1}a^{-1}(ab) \;\overset{1.3(1)}{=}\; b^{-1}(a^{-1}a)b \;\overset{1.3(2)}{=}\; b^{-1}b \;\overset{1.3(3)}{=}\; e.$$
> Ebenso gilt
> $$(ab)(ab)^{-1} = (ab)(b^{-1}a^{-1}) = a(bb^{-1})a^{-1} = aa^{-1} = e. \qquad \blacksquare$$

Wir wissen, wie Gleichungen der Art $ax = b$ mit $a, b \in \mathbb{R}$ und einer Unbekannten $x \in \mathbb{R}$ gelöst werden. Wie geht man mit Gleichungen um, in denen $a, b, x$ keine reellen Zahlen, sondern ganz allgemein Elemente einer Gruppe sind? Der folgende Satz liefert eine Antwort darauf.

## Satz 1.6 (Gleichungen lösen in Gruppen)

Sei $(G, \cdot)$ eine Gruppe, $a, b \in G$. (Beachte, dass $G$ **nicht** abelsch sein muss!) Dann gilt:

**(a)** Es gibt genau ein $x \in G$ mit $ax = b$ (nämlich $x = a^{-1}b$).
**(b)** Es gibt genau ein $y \in G$ mit $ya = b$ (nämlich $y = ba^{-1}$).
**(c)** Ist $ax = bx$ für ein $x \in G$, dann gilt $a = b$.
&nbsp;&nbsp;&nbsp;&nbsp;Ist $ya = yb$ für ein $y \in G$, dann gilt $a = b$. &nbsp;(**Kürzungsregel**)

> [!note]- Beweis
> **(a)** Um die **Existenz** eines solchen $x$ zu beweisen, zeigen wir, dass $x = a^{-1}b$ tatsächlich die Gleichung löst, mit diesem $x$ also $ax = b$ gilt:
> $$a\underbrace{(a^{-1}b)}_{x} \;\overset{1.3(1)}{=}\; (aa^{-1})b \;\overset{1.3(3)}{=}\; eb \;\overset{1.3(2)}{=}\; b.$$
> Um die **Eindeutigkeit** dieser Lösung zu zeigen, nehmen wir an, dass $ax = b$ gelte $(\ast)$. Dann folgt
> $$x \;\overset{1.3(2)}{=}\; ex \;\overset{1.3(3)}{=}\; (a^{-1}a)x \;\overset{1.3(1)}{=}\; a^{-1}(ax) \;\overset{(\ast)}{=}\; a^{-1}b.$$
>
> **(b)** Der Beweis lässt sich analog zum Beweis von Teil (a) führen.
>
> **(c)** Multiplizieren der Gleichung von rechts mit $x^{-1}$ bzw. (zweite Gleichung) von links mit $y^{-1}$ ergibt das gewünschte Ergebnis $a = b$. $\qquad \blacksquare$

> [!tip] Anwendung
> Satz 1.6 wird direkt genutzt, um in Gruppen Gleichungen aufzulösen — z. B. bei Permutationen in [[Die symmetrische Gruppe Sn]] (Bestimme $x$ mit $\sigma \circ x = \tau$).
