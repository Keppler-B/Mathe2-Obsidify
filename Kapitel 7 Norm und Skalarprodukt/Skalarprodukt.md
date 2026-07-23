---
tags: [kapitel-7, definition]
quelle: Skript S. 98
aliases: [Standard-Skalarprodukt, inneres Produkt]
---
# Skalarprodukt

> Atomare Definition aus Kapitel 7 · [[Norm und Skalarprodukt]]. Zurück zum [[Inhaltsverzeichnis]].
> Grundlage: [[Norm]], [[Vektorraum]] über $\mathbb{R}$.

## Definition 7.3 (Skalarprodukt im $\mathbb{R}^3$)

Seien $v, w \in \mathbb{R}^3$ Vektoren, der von ihnen eingeschlossene Winkel sei mit $\alpha$ bezeichnet. Dann heißt

$$(v \mid w) := \|v\| \cdot \|w\| \cdot \cos \alpha$$

das **Skalarprodukt** von $v$ mit $w$.

> [!info] Anschauung (Projektionsrechteck)
> Anschaulich entspricht $(v \mid w)$ dem Flächeninhalt des von den Vektoren $v$ und $w$ erzeugten **Projektionsrechtecks**: Man projiziert $w$ auf die Richtung von $v$; die Projektionslänge beträgt $\|w\| \cdot \cos \alpha$. Das Rechteck mit dieser Breite und der Höhe $\|v\|$ hat den Flächeninhalt $\|v\| \cdot \|w\| \cdot \cos \alpha = (v \mid w)$.

> [!tip] Standard-Skalarprodukt (koordinatenweise)
> In kartesischen Koordinaten lässt sich das Skalarprodukt komponentenweise berechnen (siehe [[Norm und Skalarprodukt]], „Zur Berechnung" sowie Definition 7.5):
> $$(v \mid w) = v_1 w_1 + v_2 w_2 + v_3 w_3 = v^T w.$$

## Verwendet in

- [[Norm und Skalarprodukt]] — Eigenschaften (Satz 7.4), Verallgemeinerung auf $\mathbb{R}^n$ und euklidische Vektorräume (Definition 7.5), Beispiele
