---
tags: [kapitel-8, thema, definition, satz, beispiel]
quelle: Skript S. 103–104
aliases: [Lineare Abbildungen]
---
# Lineare Abbildungen

> Kapitel 8 · Lineare Abbildungen — erstes Thema. Zurück zum [[Inhaltsverzeichnis]].
> Nächstes Thema: [[Rang und Kern linearer Abbildungen]]
> Grundlage: [[Vektorraum]], [[Matrix]], [[Abbildungen (injektiv, surjektiv, bijektiv)]]

In diesem Kapitel befassen wir uns mit **strukturerhaltenden Abbildungen** zwischen [[Vektorraum|Vektorräumen]], den sogenannten **linearen Abbildungen**. Wie wir sehen werden, bilden sie Unterräume wieder auf Unterräume ab.

Lineare Abbildungen sind von besonderer Bedeutung für die Geometrie und damit auch für die grafische Datenverarbeitung und die Robotik.

## Definition 8.1 (Lineare Abbildung, Vektorraum-Homomorphismus)

![[Lineare Abbildung#Definition 8.1 (Lineare Abbildung, Vektorraum-Homomorphismus)]]

## Bemerkung 8.2

Für eine lineare Abbildung $\varphi : V \to W$ gelten folgende Eigenschaften.

**(a)** $\varphi(\mathcal{O}) = \mathcal{O}$, da
$$\varphi(\underbrace{\mathcal{O} + \mathcal{O}}_{=\,\mathcal{O}}) = \varphi(\mathcal{O}) + \varphi(\mathcal{O}).$$

**(b)**
$$\varphi\Big(\underbrace{\sum_{i=1}^{n} \lambda_i v_i}_{\in\, V}\Big) = \underbrace{\sum_{i=1}^{n} \lambda_i \cdot \underbrace{\varphi(v_i)}_{\in\, W}}_{\in\, W} \qquad \text{für } v_i \in V,\ \lambda_i \in K,$$

d. h., [[Linearkombinationen und lineare (Un-)Abhängigkeit|Linearkombinationen]] in $V$ werden durch $\varphi$ in Linearkombinationen in $W$ überführt.

## Beispiel 8.3

**(a)** Die **Nullabbildung** $\varphi : V \to W,\ v \mapsto \mathcal{O}$ ist linear.

**(b)** Die Abbildung $\varphi : V \to V,\ v \mapsto \lambda v$ (für ein festes $\lambda \in K$), die einen Vektor $v$ mit dem Faktor $\lambda$ streckt, ist linear. Für $\lambda = 1$ ist $\varphi = \mathrm{id}_V$.

**(c)** Die Spiegelung an der $x_1, x_2$-Ebene,
$$\varphi : \mathbb{R}^3 \to \mathbb{R}^3, \quad \begin{pmatrix} x_1 \\ x_2 \\ x_3 \end{pmatrix} \mapsto \begin{pmatrix} x_1 \\ x_2 \\ -x_3 \end{pmatrix},$$
ist eine lineare Abbildung.

**(d)** Die Abbildung $\varphi : \mathbb{R} \to \mathbb{R},\ x \mapsto x + 1$ ist **nicht** linear, da zum Beispiel
$$\varphi(1 + 1) = \varphi(2) = 3, \quad \text{aber} \quad \underbrace{\varphi(1)}_{2} + \underbrace{\varphi(1)}_{2} \neq 3.$$

**(e)** Die Abbildung $\varphi : \mathbb{R}^2 \to \mathbb{R}^2,\ \begin{pmatrix} x_1 \\ x_2 \end{pmatrix} \mapsto \begin{pmatrix} x_1^2 \\ x_2 \end{pmatrix}$ ist ebenfalls nicht linear (wieso?).

## Satz 8.4 (Matrizen als lineare Abbildungen)

Sei $A \in M_{m,n}(K)$ eine [[Matrix]]. Dann ist
$$\varphi : K^n \to K^m, \quad x \mapsto A \cdot x$$
eine lineare Abbildung.

> [!note]- Beweis
> Der Beweis folgt aus den Rechenregeln für [[Matrizen und Operationen mit Matrizen|Matrizen]]:
>
> 1. $\varphi(x + y) = A(x + y) = Ax + Ay = \varphi(x) + \varphi(y)$
> 2. $\varphi(\lambda x) = A(\lambda x) = \lambda A x = \lambda \varphi(x) \qquad \blacksquare$

Alle bisherigen Beispiele für lineare Abbildungen in 8.3 waren von dieser Form! (Falls $V = K^n$ und $W = K^m$ gilt.)

- **Beispiel 8.3(a):** $A = \mathcal{O}$, die Nullmatrix.
- **Beispiel 8.3(b):** $A = \begin{pmatrix} \lambda & & 0 \\ & \ddots & \\ 0 & & \lambda \end{pmatrix} = \lambda \cdot E_n$.
- **Beispiel 8.3(c):** $A = \begin{pmatrix} 1 & 0 & 0 \\ 0 & 1 & 0 \\ 0 & 0 & -1 \end{pmatrix} \in M_{3,3}(\mathbb{R})$.

> [!info] Ausblick
> Tatsächlich sind **alle** linearen Abbildungen $K^n \to K^m$ von der Form in Satz 8.4, können also als Multiplikation eines Vektors mit einer Matrix beschrieben werden (siehe dazu auch [[Lineare Abbildungen auf endlichdimensionalen Vektorräumen#Beispiel 8.10 (Drehmatrix)|Beispiel 8.10]]). Wie wir in *Mathematik 3* sehen werden, lässt sich sogar jede lineare Abbildung $V \to W$ (für beliebige endliche Vektorräume $V$ und $W$) mittels einer passenden Matrix darstellen (dazu muss man in $V$ und $W$ jeweils eine [[Dimension und Basis|Basis]] festlegen, bezüglich derer die Wirkung der Abbildung beschrieben werden kann).
