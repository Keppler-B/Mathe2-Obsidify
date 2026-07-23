---
tags: [kapitel-3, definition, kernbegriff]
quelle: Skript S. 37
---
# Vektorraum

> Namensgebende Struktur von Kapitel 3. Baut auf [[Körper]] (Skalarkörper $K$) und [[Gruppe]] (die additive Gruppe $(V,+)$) auf und wird von allen Themen des Kapitels verwendet.
> Zurück: [[Vektorräume (Kapitel 3)|Vektorräume]] · [[Inhaltsverzeichnis]]

## Definition 3.1 (K-Vektorraum)

Gegeben seien

- eine Menge $V \neq \emptyset$, deren Elemente wir **Vektoren** nennen und mit kleinen lateinischen Buchstaben ($u, v, w, x, y, \dots$) bezeichnen,
- ein [[Körper]] $K$, dessen Elemente wir **Skalare** nennen und mit kleinen griechischen Buchstaben ($\alpha, \beta, \lambda, \mu, \dots$) bezeichnen (das Einselement in $K$ bezeichnen wir mit $1$),
- eine [[Verknüpfung und Abgeschlossenheit|Verknüpfung]] $+ : V \times V \to V$ (die **Vektoraddition**) und
- eine Abbildung $\cdot : K \times V \to V$ (die **skalare Multiplikation**).

Es gilt also $v + w \in V$ für $v, w \in V$ und $\lambda \cdot v \in V$ für $\lambda \in K,\, v \in V$. Für $\lambda \cdot v$ schreibt man auch $\lambda v$.

$V$ mit $K, +, \cdot$ heißt **$K$-Vektorraum** (oder **Vektorraum über $K$**), wenn gilt

**(1)** $(V, +)$ ist eine abelsche [[Gruppe]].
&nbsp;&nbsp;&nbsp;&nbsp;Das neutrale Element nennen wir **Nullvektor**, bezeichnet mit $\mathcal{O}$, das Inverse zu $v \in V$ bezeichnen wir mit $-v$ (also $v + (-v) = \mathcal{O}$ für alle $v \in V$).

**(2)** Für $\cdot$ gilt für alle $\lambda, \mu \in K$, $v, w \in V$:

&nbsp;&nbsp;&nbsp;&nbsp;**(2.1)** $(\lambda \cdot \mu) \cdot v = \lambda \cdot (\mu \cdot v)$ &nbsp;(**Assoziativgesetz**)

&nbsp;&nbsp;&nbsp;&nbsp;**(2.2)** $(\lambda + \mu) \cdot v = (\lambda \cdot v) + (\mu \cdot v)$ &nbsp;(**1. Distributivgesetz**)

&nbsp;&nbsp;&nbsp;&nbsp;**(2.3)** $\lambda \cdot (v + w) = (\lambda \cdot v) + (\lambda \cdot w)$ &nbsp;(**2. Distributivgesetz**)

&nbsp;&nbsp;&nbsp;&nbsp;**(2.4)** $1 \cdot v = v$ &nbsp;(mit dem Einselement $1 \in K$)

Oft ist $K = \mathbb{R}$, man spricht dann von einem **reellen Vektorraum**.

> [!tip] Merkhilfe
> Ein Vektorraum verbindet **zwei** Strukturen: $(V, +)$ ist eine abelsche [[Gruppe]] (die Vektoraddition), und der [[Körper]] $K$ wirkt über die skalare Multiplikation von außen auf $V$ — verträglich mit beiden Verknüpfungen (Assoziativität und die beiden Distributivgesetze) sowie normiert durch $1 \cdot v = v$.

## Verwendet in

- [[Vektorräume (Kapitel 3)]] — Beispiele ($K^n$, Funktionenraum) und Rechenregeln (Satz 3.4)
- [[Untervektorräume]] — Teilmengen, die selbst Vektorraum sind
- [[Linearkombinationen und lineare (Un-)Abhängigkeit]], [[Dimension und Basis]]
- [[Erzeugte Unterräume, Schnitt und Summe von Unterräumen]]
