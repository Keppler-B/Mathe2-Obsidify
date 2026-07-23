---
tags: [grundlagen, wiederholung, referenz]
quelle: Wiederholung aus Mathematik 1
---
# Mengen und Mengenoperationen

> Notations-Referenz. Diese Symbole werden im gesamten Skript vorausgesetzt und durchgehend verwendet.
> Zurück: [[Übersicht|Grundlagen]]

> [!info] Hinweis
> Diese Notation stammt aus *Mathematik 1* und wird im Skript nicht neu eingeführt. Hier als Schnellreferenz.

## Grundbegriffe

Eine **Menge** ist eine Zusammenfassung wohlunterschiedener Objekte (ihrer **Elemente**).

| Symbol | Bedeutung | Beispiel |
|:---|:---|:---|
| $a \in X$ | $a$ ist Element von $X$ | $2 \in \mathbb{Z}$ |
| $a \notin X$ | $a$ ist kein Element von $X$ | $\tfrac12 \notin \mathbb{Z}$ |
| $\emptyset$ | leere Menge | $\{\}$ |
| $X \subseteq Y$ | $X$ ist Teilmenge von $Y$ | $\mathbb{N} \subseteq \mathbb{Z}$ |
| $\{x \mid E(x)\}$ | Menge aller $x$ mit Eigenschaft $E$ | $\{x \in \mathbb{Z} \mid x > 0\}$ |
| $\lvert X \rvert$ | Anzahl der Elemente (Mächtigkeit) | $\lvert\{a,b,c\}\rvert = 3$ |

## Verknüpfungen von Mengen

| Operation | Definition |
|:---|:---|
| Vereinigung $X \cup Y$ | $\{a \mid a \in X \text{ oder } a \in Y\}$ |
| Schnitt $X \cap Y$ | $\{a \mid a \in X \text{ und } a \in Y\}$ |
| Differenz $X \setminus Y$ | $\{a \mid a \in X \text{ und } a \notin Y\}$ |
| Kartesisches Produkt $X \times Y$ | $\{(a, b) \mid a \in X,\ b \in Y\}$ (Menge der geordneten Paare) |

Das **kartesische Produkt** ist besonders wichtig: Eine [[Verknüpfung und Abgeschlossenheit|Verknüpfung]] $\ast : X \times X \to X$ ist eine Abbildung *auf Paaren*, und $K^n = \underbrace{K \times \dots \times K}_{n}$ ist der Standard-[[Vektorraum]].

## Zahlbereiche (Standard-Mengen)

$$\mathbb{N} \subseteq \mathbb{Z} \subseteq \mathbb{Q} \subseteq \mathbb{R} \subseteq \mathbb{C}$$

natürliche $\subseteq$ ganze $\subseteq$ rationale $\subseteq$ reelle $\subseteq$ komplexe Zahlen. Dazu die Restklassen $\mathbb{Z}_m$ ([[Restklassen modulo m als Gruppe]]).

## Verwendet in

- Praktisch überall — insbesondere [[Verknüpfung und Abgeschlossenheit]], [[Gruppe]], [[Vektorraum]], [[Untervektorräume]], [[Erzeugte Unterräume, Schnitt und Summe von Unterräumen]].
