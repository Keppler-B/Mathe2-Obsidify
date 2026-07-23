---
tags: [kapitel-8, definition, kernbegriff]
quelle: Skript S. 103
---
# Lineare Abbildung

> Namensgebender Kernbegriff von Kapitel 8. Baut auf [[Vektorraum]] auf und wird im gesamten Kapitel verwendet.
> Zurück: [[Lineare Abbildungen (Kapitel 8)]] · [[Inhaltsverzeichnis]]

## Definition 8.1 (Lineare Abbildung, Vektorraum-Homomorphismus)

Sei $K$ ein [[Körper]], $V$ und $W$ seien [[Vektorraum|$K$-Vektorräume]].

**(a)** $\varphi : V \to W$ heißt **lineare Abbildung** (**Vektorraum-Homomorphismus**), falls gilt:

1. $\varphi(v_1 + v_2) = \varphi(v_1) + \varphi(v_2)$ für alle $v_1, v_2 \in V$ &nbsp;(**Additivität**),
2. $\varphi(\lambda v) = \lambda \cdot \varphi(v)$ für alle $v \in V,\ \lambda \in K$ &nbsp;(**Homogenität**).

**(b)** Ist die lineare Abbildung $\varphi : V \to W$ [[Abbildungen (injektiv, surjektiv, bijektiv)|bijektiv]], so heißt $\varphi$ **Isomorphismus**. Die Vektorräume $V$ und $W$ heißen dann **isomorph**, geschrieben $V \cong W$.

> [!tip] Merkhilfe
> Eine lineare Abbildung ist **strukturerhaltend**: Sie ist mit der Addition und der Skalarmultiplikation verträglich. Kurz zusammengefasst gilt $\varphi(\lambda v_1 + \mu v_2) = \lambda\,\varphi(v_1) + \mu\,\varphi(v_2)$.
