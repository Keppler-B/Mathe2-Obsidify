---
tags: [grundlagen, definition]
quelle: Skript S. 3
---
# Verknüpfung und Abgeschlossenheit

> Grundbaustein aller algebraischen Strukturen dieses Skripts ([[Gruppe]], [[Ring]], [[Körper]], [[Vektorraum]]).
> Zurück: [[Übersicht|Grundlagen]] · [[Verknüpfungen, Gruppen, erste Beispiele]]

## Definition 1.1 (Verknüpfung, Abgeschlossenheit)

**(a)** Seien $X, Y$ nichtleere Mengen. Eine **Verknüpfung** (oder *abstrakte Multiplikation*) $\ast$ auf $X$ ist eine Abbildung

$$\ast : X \times X \to Y, \qquad (a,b) \mapsto a \ast b.$$

Der Ausdruck $a \ast b$ (oft auch einfach nur $ab$) heißt **Produkt** von $a$ und $b$, muss aber nichts mit der üblichen Multiplikation von Zahlen zu tun haben. Bei endlichen Mengen wird die Abbildungsvorschrift oft mittels einer **Multiplikationstafel** (oder **Verknüpfungstafel**) angegeben, siehe Beispiel 1.2.

**(b)** Eine Menge $X \neq \emptyset$ heißt **abgeschlossen** bezüglich einer Verknüpfung $\ast$, falls

$$a \ast b \in X \quad \text{für alle } a, b \in X.$$

## Beispiel 1.2

**(a)** Sei auf $X = \{a, b\}$ eine Verknüpfung $\ast$ definiert mittels

$$\ast : X \times X \to X, \qquad (a,b) \mapsto a \ast b,$$

wobei $a \ast a = b,\; a \ast b = b,\; b \ast a = a,\; b \ast b = a$ gelte. Die Zuordnungsvorschrift der Abbildung $\ast$ kann auch mittels dieser Multiplikationstafel angegeben werden:

| $\ast$ | $a$ | $b$ |
|:------:|:---:|:---:|
| **$a$** | $b$ | $b$ |
| **$b$** | $a$ | $a$ |

Die Menge $X$ ist abgeschlossen bezüglich $\ast$.

Für diese Verknüpfung gilt beispielsweise $(a \ast a) \ast a = b \ast a = a$ und $a \ast (a \ast a) = a \ast b = b$; das vom Rechnen mit reellen Zahlen bekannte **Assoziativgesetz** und das **Kommutativgesetz** (siehe auch [[Gruppe|Definition 1.3]]) sind hier also nicht erfüllt.

**(b)**

- Die Menge $X = \{0, 1\}$ ist abgeschlossen bezüglich der üblichen Multiplikation $\cdot$ auf $\mathbb{Z}$, d. h. es handelt sich bei $\cdot$ um eine Abbildung $\cdot : X \times X \to X$:
  Es gilt $0 \cdot 0 = 0 \in X,\; 0 \cdot 1 = 1 \cdot 0 = 0 \in X,\; 1 \cdot 1 = 1 \in X$.
  Allerdings ist $X$ **nicht** abgeschlossen bezüglich der üblichen Addition $+$ auf $\mathbb{Z}$, d. h. wir haben es hier nur mit einer Abbildung $+ : X \times X \to \mathbb{Z}$ zu tun:
  $0 + 1 = 1 \in X$, aber $1 + 1 = 2 \notin X$.
- Die Menge $X = \{1, 2\}$ ist weder bezüglich der Multiplikation noch bezüglich der Addition abgeschlossen.

## Verwendet in

- [[Gruppe]] — eine Gruppe ist eine Menge mit *einer* abgeschlossenen Verknüpfung
- [[Ring]] und [[Körper]] — Mengen mit *zwei* Verknüpfungen
- [[Vektorraum]] — Vektoraddition und Skalarmultiplikation
