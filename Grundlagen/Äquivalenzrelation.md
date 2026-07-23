---
tags: [grundlagen, wiederholung, definition]
quelle: Wiederholung aus Mathematik 1
---
# Äquivalenzrelation

> Wiederholung aus *Mathematik 1*. Wird im Skript vorausgesetzt und in [[Restklassen modulo m als Gruppe]] direkt benötigt (Kongruenz modulo $m$).
> Zurück: [[Übersicht|Grundlagen]]

> [!info] Hinweis
> Der Begriff wird im Skript nicht neu definiert (Bemerkung 1.19(b) und 1.22 verweisen darauf). Diese Notiz fasst ihn zusammen.

## Definition

Eine **Relation** $\sim$ auf einer Menge $X$ ist eine Teilmenge von $X \times X$; man schreibt $a \sim b$, falls $(a,b)$ in dieser Teilmenge liegt.

$\sim$ heißt **Äquivalenzrelation**, wenn für alle $a, b, c \in X$ gilt:

1. $a \sim a$ &nbsp;(**Reflexivität**),
2. $a \sim b \Rightarrow b \sim a$ &nbsp;(**Symmetrie**),
3. $a \sim b$ und $b \sim c \Rightarrow a \sim c$ &nbsp;(**Transitivität**).

## Äquivalenzklassen und Repräsentanten

Die **Äquivalenzklasse** von $a$ ist $[a] = \{x \in X \mid x \sim a\}$. Die Klassen zerlegen $X$ **disjunkt** (Partition). Ein **vollständiges Repräsentantensystem** enthält aus jeder Klasse genau ein Element.

## Wichtigstes Beispiel im Skript: Kongruenz modulo $m$

Auf $\mathbb{Z}$ ist durch

$$n_1 \sim n_2 :\iff n_1 \equiv n_2 \bmod m \quad (\iff m \mid (n_1 - n_2))$$

eine Äquivalenzrelation definiert. Die Klassen sind die **Restklassen**; die Zahlen $0, 1, \dots, m-1$ bilden ein vollständiges Repräsentantensystem — genau die Menge $\mathbb{Z}_m$ (siehe [[Restklassen modulo m als Gruppe]]).

> [!tip] Merkhilfe
> „Gleich bis auf etwas Erlaubtes." Kongruenz mod $m$: gleich, wenn sie denselben Rest lassen. Für $m = 2$: $a \sim b \iff a - b$ gerade.

## Verwendet in

- [[Restklassen modulo m als Gruppe]] — Definition von $\mathbb{Z}_m$
