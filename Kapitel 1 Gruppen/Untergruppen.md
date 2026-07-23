---
tags: [kapitel-1, thema, definition, satz]
quelle: Skript S. 17–19
---
# Untergruppen

> Kapitel 1 · Gruppen — Unterstruktur von Gruppen. Zurück zum [[Inhaltsverzeichnis]].
> Voriges Thema: [[Restklassen modulo m als Gruppe]] · Nächstes Kapitel: [[Ringe]]
> Grundlage: [[Gruppe]]. Analoge Unterstrukturen später: [[Untervektorräume]].

Abschließend lernen wir eine Unterstruktur von Gruppen kennen, die **Untergruppen**.

## Definition/Bemerkung 1.29 (Untergruppe)

Sei $(G, \cdot)$ eine [[Gruppe]], $\emptyset \neq U \subseteq G$ eine nichtleere Teilmenge von $G$. Dann heißt $U$ **Untergruppe** von $G$ (in Zeichen $U \leq G$), falls $U$ bezüglich der Verknüpfung $\cdot$ selbst eine Gruppe ist.

Insbesondere gilt dann:
- Für alle $u, v \in U$ ist $u \cdot v \in U$ (Abgeschlossenheit),
- das neutrale Element $e$ von $G$ ist auch neutrales Element von $U$,
- Inversen in $U$ sind die gleichen wie in $G$.

> [!note]- Beweis (neutrales Element)
> Angenommen, $e$ ist neutrales Element in $G$, aber $U$ besitzt ein anderes neutrales Element $f$. Die Inverse von $f$ in $G$ sei $f^{-1}$, d. h. $f^{-1}f = f f^{-1} = e$. Da $f$ neutrales Element in $U$ ist, gilt $f f = f$. Insgesamt:
> $$f = ef = (f^{-1}f)f = f^{-1}(ff) = f^{-1}f = e,$$
> d. h. $e$ und $f$ sind dieselben Elemente. $\qquad \blacksquare$

## Beispiel 1.30

**(a)** $(\mathbb{Z}, +) \leq (\mathbb{Q}, +) \leq (\mathbb{R}, +)$
**(b)** $(\{-1, 1\}, \cdot) \leq (\mathbb{Q} \setminus \{0\}, \cdot) \leq (\mathbb{R} \setminus \{0\}, \cdot)$
**(c)** $(\{e\}, \cdot)$ ist Untergruppe jeder beliebigen Gruppe mit Verknüpfung $\cdot$ und neutralem Element $e$.
**(d)** Für $\pi = \begin{pmatrix} 1 & 2 & 3 \\ 2 & 1 & 3 \end{pmatrix} \in S_3$ gilt $\pi = \pi^{-1}$, $\pi \circ \pi = \varepsilon$. Damit ist $\{\varepsilon, \pi\} \leq S_3$.

## Satz 1.31 (Untergruppenkriterium)

Eine nicht-leere Teilmenge $U \subseteq G$ einer Gruppe $(G, \cdot)$ ist zusammen mit der Verknüpfung $\cdot$ **genau dann** eine Untergruppe von $G$, wenn

$$u \cdot v^{-1} \in U \quad \text{für alle } u, v \in U$$

gilt.

> [!tip] Praxis
> Man muss zusätzlich zeigen, dass $U \neq \emptyset$ ist (oft einfach: das neutrale Element ist enthalten). Assoziativität (und Kommutativität, falls $G$ abelsch) werden an Teilmengen **vererbt**, müssen also nicht geprüft werden. Abgeschlossenheit sowie Existenz des Neutralen und aller Inversen sind durch die Forderung $u \cdot v^{-1} \in U$ abgedeckt.

> [!note]- Beweis
> **„$\Rightarrow$"** Falls $U \subseteq G$ eine Untergruppe ist, gilt Abgeschlossenheit und die Existenz aller Inversen in $U$; damit ist $u \cdot v^{-1} \in U$ für alle $u, v \in U$ erfüllt.
>
> **„$\Leftarrow$"** Sei $U \neq \emptyset$ und es gelte $u \cdot v^{-1} \in U$ für alle $u, v \in U$.
> - Assoziativität in $U$ folgt aus der Assoziativität in $G$.
> - Das neutrale Element $e \in G$ liegt in $U$: da $U \neq \emptyset$, gibt es ein $u \in U$, und nach Voraussetzung ist $e = u \cdot u^{-1} \in U$.
> - Wegen $v^{-1} = e \cdot v^{-1}$ ist mit $v$ auch $v^{-1} \in U$; jedes Element besitzt also eine Inverse in $U$.
> - Sind $u, v \in U$, so ist auch $v^{-1} \in U$ und damit $u \cdot v = u \cdot (v^{-1})^{-1} \in U$, also ist $U$ abgeschlossen. $\qquad \blacksquare$
