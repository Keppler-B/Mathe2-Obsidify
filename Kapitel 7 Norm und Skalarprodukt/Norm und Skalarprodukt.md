---
tags: [kapitel-7, thema, definition, satz, beispiel]
quelle: Skript S. 97–101
aliases: [Kapitel 7, Skalarprodukt und Norm, euklidischer Vektorraum]
---
# Norm und Skalarprodukt

> Kapitel 7 · Norm und Skalarprodukt. Zurück zum [[Inhaltsverzeichnis]].
> Voriges Thema: [[Eigenwerte, Eigenvektoren, Eigenräume]] · Nächstes Thema: [[Lineare Abbildungen (Kapitel 8)|Lineare Abbildungen]]
> Grundlage: [[Vektorraum]] über $\mathbb{R}$, [[Körper]] ($\mathbb{R}$), [[Norm]], [[Skalarprodukt]]

In diesem kurzen Kapitel betrachten wir nur **$\mathbb{R}$-Vektorräume** und befassen uns mit der **Norm** eines Vektors und dem **Abstand** zweier Vektoren.

## Norm eines Vektors

![[Norm#Definition 7.1 (Norm)]]

Mittels dieser Definition lassen sich die folgenden Eigenschaften zeigen.

## Satz 7.2 (Eigenschaften der Norm)

**(a)** $\|v\| \geq 0$ für alle $v \in \mathbb{R}^n$, und $\|v\| = 0 \iff v = \mathcal{O}$

**(b)** $\|\lambda v\| = |\lambda| \cdot \|v\|$ für alle $\lambda \in \mathbb{R},\; v \in \mathbb{R}^n$

**(c)** $\|v + w\| \leq \|v\| + \|w\|$ für alle $v, w \in \mathbb{R}^n$ (**Dreiecksungleichung**), mit Gleichheit genau dann, wenn $v = \lambda w$ für ein $\lambda \in \mathbb{R}$ gilt.

## Skalarprodukt

Mittels der Norm definieren wir — zunächst nur für Vektoren des $\mathbb{R}^3$ — das **Skalarprodukt** zweier Vektoren.

![[Skalarprodukt#Definition 7.3 (Skalarprodukt im $\mathbb{R}^3$)]]

## Satz 7.4 (Eigenschaften des Skalarprodukts)

Seien $u, v, w \in \mathbb{R}^3,\; \lambda \in \mathbb{R}$. Dann gelten die folgenden Eigenschaften für das Skalarprodukt.

**(a)** $(v \mid w) \in \mathbb{R}$ (daher der Name **Skalar**produkt)

**(b)** $(v \mid w) = (w \mid v)$

**(c)** $(\lambda v \mid w) = (v \mid \lambda w) = \lambda (v \mid w)$

**(d)** $(u + v \mid w) = (u \mid w) + (v \mid w)$

**(e)** $(v \mid v) = \|v\|^2$

Eigenschaft (b) wird als **Symmetrie** des Skalarprodukts bezeichnet, die Eigenschaften (c) und (d) zusammen als **Linearität** des Skalarprodukts. Wegen der Symmetrie gelten (c) und (d) auch im zweiten Argument des Skalarprodukts.

> [!note]- Beweis
> **(a)** Folgt aus der Definition.
>
> **(b)** $(v \mid w) = \|v\| \cdot \|w\| \cdot \cos \alpha = \|w\| \cdot \|v\| \cdot \cos(-\alpha) = (w \mid v)$
>
> **(c)**
> - Für $\lambda = 0$ gilt die Gleichung offensichtlich.
> - Für $\lambda > 0$ ist $(\lambda v \mid w) = \|\lambda v\| \cdot \|w\| \cdot \cos \alpha = \lambda \cdot \|v\| \cdot \|w\| \cdot \cos \alpha = \lambda (v \mid w)$.
> - Für $\lambda < 0$ gilt: der Winkel zwischen $\lambda v$ und $w$ ist $\pi - \alpha$, also ist
>   $$(\lambda v \mid w) = \|\lambda v\| \cdot \|w\| \cos(\pi - \alpha) = -\lambda \cdot \|v\| \cdot \|w\| \cdot (-\cos \alpha) = \lambda (v \mid w).$$
>
> **(d)** Für die Flächen der entsprechenden Projektionsrechtecke gilt Gleichheit.
>
> **(e)** In diesem Fall ist $\alpha = 0$ und damit $\cos \alpha = 1$, also gilt $(v \mid v) = \|v\| \cdot \|v\| \cdot 1 = \|v\|^2$. $\qquad \blacksquare$

## Zur Berechnung

Für die kanonischen Basisvektoren $e_1, e_2, e_3 \in \mathbb{R}^3$ gilt:

- $(e_i \mid e_i) = 1$ für alle $i \in \{1, 2, 3\}$, da der von zwei identischen Vektoren eingeschlossene Winkel gleich $0$ ist.
- $(e_i \mid e_j) = 0$ für $i \neq j$, da in diesem Fall $\alpha = 90^\circ$ und $\cos \alpha = 0$ gilt.

Für zwei beliebige Vektoren $v = \begin{pmatrix} v_1 \\ v_2 \\ v_3 \end{pmatrix}$ und $w = \begin{pmatrix} w_1 \\ w_2 \\ w_3 \end{pmatrix} \in \mathbb{R}^3$ lässt sich das Skalarprodukt damit berechnen als

$$
\begin{aligned}
(v \mid w) &= (v_1 e_1 + v_2 e_2 + v_3 e_3 \mid w_1 e_1 + w_2 e_2 + w_3 e_3) \\
&\overset{7.4\,(c),(d)}{=} v_1 w_1 \underbrace{(e_1 \mid e_1)}_{1} + v_1 w_2 \underbrace{(e_1 \mid e_2)}_{0} + v_1 w_3 \underbrace{(e_1 \mid e_3)}_{0} + \cdots + v_3 w_3 (e_3 \mid e_3) \\
&= v_1 w_1 + v_2 w_2 + v_3 w_3.
\end{aligned}
$$

Mit dieser Überlegung lässt sich das Skalarprodukt für Vektoren aus dem $\mathbb{R}^n$ definieren und auch für andere reelle Vektorräume verallgemeinern.

## Definition 7.5 (Skalarprodukt, euklidischer Vektorraum, Norm, Abstand)

**(a)** Für $v = \begin{pmatrix} v_1 \\ \vdots \\ v_n \end{pmatrix},\; w = \begin{pmatrix} w_1 \\ \vdots \\ w_n \end{pmatrix} \in \mathbb{R}^n$ heißt

$$(v \mid w) := \sum_{j=1}^{n} v_j w_j = v^T w$$

das **(Standard-)Skalarprodukt** von $v$ mit $w$.

**(b)** Sei $V$ ein beliebiger [[Vektorraum|$\mathbb{R}$-Vektorraum]]. Eine Abbildung

$$(\,\cdot \mid \cdot\,) : V \times V \to \mathbb{R}, \qquad (v, w) \mapsto (v \mid w)$$

heißt **Skalarprodukt** auf $V$, falls sie die Eigenschaften aus [[#Satz 7.4 (Eigenschaften des Skalarprodukts)|7.4]] erfüllt. Der Vektorraum $V$ heißt dann **Euklidischer Vektorraum**.

**(c)** Für $v, w \in V$ und einen euklidischen Vektorraum $V$ heißt

$$\|v\| := +\sqrt{(v \mid v)}$$

(also die positive Wurzel aus dem Skalarprodukt von $v$ mit sich selbst) die **(euklidische) Norm** von $v$ und

$$d(v, w) = \|v - w\|$$

der **(euklidische) Abstand** von $v$ und $w$.

## Beispiel 7.6

**(a)** $v = \begin{pmatrix} -1 \\ 2 \\ 1 \end{pmatrix},\; w = \begin{pmatrix} 2 \\ 2 \\ 4 \end{pmatrix} \in \mathbb{R}^3$

- $(v \mid w) = v^T w = -1 \cdot 2 + 2 \cdot 2 + 1 \cdot 4 = 6$
- $\|v\| = +\sqrt{(v \mid v)} = +\sqrt{(-1)^2 + 2^2 + 1^2} = \sqrt{6}$
- $d(v, w) = \|v - w\| = \left\| \begin{pmatrix} -1 - 2 \\ 2 - 2 \\ 1 - 4 \end{pmatrix} \right\| = \sqrt{(-3)^2 + 0 + (-3)^2} = \sqrt{18}$
- Winkel zwischen $v$ und $w$:
  $$
  \begin{aligned}
  (v \mid w) &= \|v\| \cdot \|w\| \cdot \cos \alpha \\
  \iff \cos \alpha &= \frac{(v \mid w)}{\|v\| \cdot \|w\|} \\
  \iff \cos \alpha &= \frac{6}{\sqrt{6} \cdot \sqrt{24}} = \frac{1}{2} \;\Rightarrow\; \alpha = \frac{\pi}{3}
  \end{aligned}
  $$

**(b)** Für

$$V = C[a, b] = \{f : [a, b] \to \mathbb{R},\; f \text{ stetig}\},$$

den Vektorraum der stetigen Funktionen, die auf dem Intervall $[a, b]$ definiert sind, lassen sich Skalarprodukt und Norm wie folgt definieren:

$$(f \mid g) := \int_a^b f(t)\, g(t)\, dt$$

ist Skalarprodukt,

$$\|f\| = \sqrt{\int_a^b f^2(t)\, dt}$$

ist Norm auf $V$.

> [!info] Ausblick
> In *Mathematik 3* werden wir das Skalarprodukt für das wichtige Konzept der **Orthogonalität** nutzen.
