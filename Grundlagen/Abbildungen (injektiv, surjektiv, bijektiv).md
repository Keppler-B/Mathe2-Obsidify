---
tags: [grundlagen, wiederholung, definition]
quelle: Wiederholung aus Mathematik 1
---
# Abbildungen (injektiv, surjektiv, bijektiv)

> Wiederholung aus *Mathematik 1*. Wird im Skript vorausgesetzt und u. a. benötigt in [[Die symmetrische Gruppe Sn]] (Permutationen) und [[Lineare Abbildungen (Kapitel 8)|Lineare Abbildungen]].
> Zurück: [[Übersicht|Grundlagen]]

> [!info] Hinweis
> Diese Begriffe werden im Skript nicht neu definiert, sondern aus *Mathematik 1* vorausgesetzt. Diese Notiz fasst sie zur schnellen Referenz zusammen.

## Abbildung

Eine **Abbildung** (Funktion) $f : X \to Y$ ordnet jedem Element $x \in X$ genau ein Element $f(x) \in Y$ zu. $X$ heißt **Definitionsbereich**, $Y$ **Zielbereich**.

## Eigenschaften

Sei $f : X \to Y$ eine Abbildung.

- **injektiv** (linkseindeutig): verschiedene Elemente haben verschiedene Bilder,
  $$f(x_1) = f(x_2) \implies x_1 = x_2 \qquad (\text{für alle } x_1, x_2 \in X).$$
- **surjektiv** (rechtstotal): jedes $y \in Y$ wird getroffen,
  $$\forall\, y \in Y\; \exists\, x \in X:\; f(x) = y.$$
- **bijektiv**: injektiv **und** surjektiv. Dann existiert die **Umkehrabbildung** $f^{-1} : Y \to X$ mit $f^{-1} \circ f = \mathrm{id}_X$ und $f \circ f^{-1} = \mathrm{id}_Y$.

## Komposition

Für $f : X \to Y$ und $g : Y \to Z$ ist die **Komposition** $g \circ f : X \to Z$ definiert durch $(g \circ f)(x) = g(f(x))$.

> [!note] Wichtige Fakten (im Skript verwendet)
> - Die Komposition **bijektiver** Abbildungen ist wieder bijektiv (genutzt bei $S_n$).
> - Für endliche Mengen gleicher Größe gilt: $f$ injektiv $\iff$ $f$ surjektiv $\iff$ $f$ bijektiv.
