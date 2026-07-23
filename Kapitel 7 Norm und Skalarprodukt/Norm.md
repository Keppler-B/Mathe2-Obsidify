---
tags: [kapitel-7, definition]
quelle: Skript S. 97
aliases: [Länge eines Vektors, euklidische Norm]
---
# Norm

> Atomare Definition aus Kapitel 7 · [[Norm und Skalarprodukt]]. Zurück zum [[Inhaltsverzeichnis]].
> Grundlage: [[Vektorraum]] über $\mathbb{R}$.

## Definition 7.1 (Norm)

Für $v = \begin{pmatrix} v_1 \\ \vdots \\ v_n \end{pmatrix} \in \mathbb{R}^n$ heißt

$$\|v\| := \left( \sum_{i=1}^{n} v_i^2 \right)^{\frac{1}{2}}$$

die **Norm** oder **Länge** von $v$.

> [!info] Anschauung (Satz des Pythagoras)
> Für $v = \begin{pmatrix} v_1 \\ v_2 \end{pmatrix} \in \mathbb{R}^2$ bilden die Komponenten $v_1$ (in $x$-Richtung) und $v_2$ (in $y$-Richtung) die Katheten eines rechtwinkligen Dreiecks, dessen Hypotenuse der Vektor $v$ vom Ursprung zum Punkt $(v_1, v_2)$ ist. Nach dem **Satz des Pythagoras** entspricht
> $$\|v\| = \sqrt{v_1^2 + v_2^2}$$
> der Länge des Vektors.

## Verwendet in

- [[Norm und Skalarprodukt]] — Eigenschaften der Norm (Satz 7.2), Definition von Skalarprodukt, euklidischer Norm und Abstand
