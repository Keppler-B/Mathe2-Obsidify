---
tags: [kapitel-8, thema, definition, satz, beispiel]
quelle: Skript S. 105–106
---
# Rang und Kern linearer Abbildungen

> Kapitel 8 · Lineare Abbildungen — zweites Thema. Zurück zum [[Inhaltsverzeichnis]].
> Voriges Thema: [[Lineare Abbildungen (Kapitel 8)|Lineare Abbildungen]] · Nächstes Thema: [[Lineare Abbildungen auf endlichdimensionalen Vektorräumen]]
> Grundlage: [[Lineare Abbildung]], [[Untervektorräume]], [[Dimension und Basis]], [[Abbildungen (injektiv, surjektiv, bijektiv)]]

## Satz 8.5 (Eigenschaften des Bilds einer linearen Abbildung)

Sei $\varphi : V \to W$ eine [[Lineare Abbildung|lineare Abbildung]].

**(a)** Sei $U \subseteq V$ ein [[Untervektorräume|Unterraum]] von $V$, dann ist $\underbrace{\varphi(U)}_{\text{Bild von } U} \subseteq W$ ein Unterraum von $W$.

**(b)** Falls $\dim(U) < \infty$, so gilt $\dim(\varphi(U)) \leq \dim(U)$.

> [!note]- Beweis
> **(a)** Wir benutzen das [[Untervektorräume|Unterraumkriterium]]:
> - $\varphi(U)$ ist nicht leer, denn $\mathcal{O} = \varphi(\mathcal{O}) \in \varphi(U)$.
> - Seien $v, w \in U$ und $\lambda \in K$. Dann sind $\varphi(v), \varphi(w) \in \varphi(U)$ und damit
>   $$\varphi(v) + \varphi(w) \underset{\varphi\ \text{lin. Abb.}}{=} \varphi(\underbrace{v + w}_{\in\, U,\ \text{da } U \text{ Unterraum}}) \in \varphi(U) \quad \text{und}$$
>   $$\lambda \varphi(v) \underset{\varphi\ \text{lin. Abb.}}{=} \varphi(\underbrace{\lambda v}_{\in\, U}) \in \varphi(U).$$
>
> **(b)** Sei $\{u_1, \dots, u_k\}$ eine [[Dimension und Basis|Basis]] von $U$. Dann ist die Menge $\{\varphi(u_1), \dots, \varphi(u_k)\}$ wegen der Linearität von $\varphi$ ein Erzeugendensystem von $\varphi(U)$ und enthält also auch eine Basis von $\varphi(U)$. Damit gilt die Aussage über die Dimensionen. $\qquad \blacksquare$

Der erste Teil des Satzes motiviert die folgende Definition: Da das Bild einer linearen Abbildung ein Unterraum ist, ergibt es Sinn, von der Dimension des Bilds zu sprechen.

## Definition 8.6 (Rang einer linearen Abbildung)

Sei $\varphi : V \to W$ eine lineare Abbildung und $\dim V < \infty$. Dann heißt $\dim(\varphi(V))$ der **Rang von $\varphi$**, bezeichnet mit $\mathrm{rg}(\varphi)$.

Ein weiterer wichtiger Begriff im Zusammenhang mit linearen Abbildungen ist der **Kern**:

## Definition/Satz 8.7 (Kern einer linearen Abbildung)

Sei $\varphi : V \to W$ eine lineare Abbildung.

**(a)** $\ker \varphi := \{v \in V \mid \varphi(v) = \mathcal{O}\}$ (also die Menge aller Vektoren, die von $\varphi$ auf $\mathcal{O}$ abgebildet werden) heißt der **Kern von $\varphi$** und ist ein [[Untervektorräume|Unterraum]] von $V$.

**(b)** $\varphi$ [[Abbildungen (injektiv, surjektiv, bijektiv)|injektiv]] $\iff \ker \varphi = \{\mathcal{O}\}$.

> [!note]- Beweis
> **(a)** Wir prüfen das Unterraumkriterium (Satz 3.7) für $\ker \varphi$ nach:
> - Nach Bem. 8.2 ist $\varphi(\mathcal{O}) = \mathcal{O}$, also ist $\mathcal{O} \in \ker \varphi$.
> - Seien $u, v \in \ker \varphi$, d. h. $\varphi(u) = \varphi(v) = \mathcal{O}$, und $\lambda, \mu \in K$. Dann ist
>   $$\varphi(\lambda u + \mu v) \underset{\varphi\ \text{linear}}{=} \lambda \underbrace{\varphi(u)}_{\mathcal{O}} + \mu \underbrace{\varphi(v)}_{\mathcal{O}} = \mathcal{O},$$
>   also gilt $\lambda u + \mu v \in \ker \varphi$.
>
> Damit ist $\ker(\varphi)$ ein Unterraum von $V$.
>
> **(b)** „$\Rightarrow$" Nach Bem. 8.2 ist $\varphi(\mathcal{O}) = \mathcal{O}$. Wegen der Injektivität von $\varphi$ kann kein weiteres Element auf $\mathcal{O}$ abgebildet werden, $\ker \varphi$ besteht also nur aus dem Nullvektor.
>
> „$\Leftarrow$" Sei $\ker \varphi = \{\mathcal{O}\}$. Wir zeigen: Falls $\varphi(v_1) = \varphi(v_2)$, dann $v_1 = v_2$ (das ist die Definition von injektiv). Angenommen, es gibt $v_1, v_2 \in V$ mit $\varphi(v_1) = \varphi(v_2)$. Dann ist
>   $$\mathcal{O} = \varphi(v_1) - \varphi(v_2) \underset{\varphi\ \text{linear}}{=} \varphi(v_1 - v_2).$$
>   Da laut Voraussetzung nur $\mathcal{O}$ im $\ker \varphi$ liegt, also nur $\mathcal{O}$ von $\varphi$ auf $\mathcal{O}$ abgebildet wird, ist $v_1 - v_2 = \mathcal{O}$, also $v_1 = v_2$. Damit ist $\varphi$ injektiv. $\qquad \blacksquare$

## Beispiel 8.8

Sei
$$\varphi : \mathbb{R}^3 \to \mathbb{R}^3, \quad \begin{pmatrix} x_1 \\ x_2 \\ x_3 \end{pmatrix} \mapsto \begin{pmatrix} x_1 \\ 2x_1 \\ x_1 + x_2 + 2x_3 \end{pmatrix}$$
eine lineare Abbildung. Die zugehörige Matrix ist
$$A = \begin{pmatrix} 1 & 0 & 0 \\ 2 & 0 & 0 \\ 1 & 1 & 2 \end{pmatrix} \in M_{3,3}(\mathbb{R}).$$
Wir betrachten den Unterraum $U = \langle e_2, e_3 \rangle$ ($\dim U = 2$) und berechnen $\varphi(U)$, $\dim \varphi(U)$ und $\ker \varphi$.

- Zunächst berechnen wir $\varphi(e_2)$ und $\varphi(e_3)$:
  $$\varphi(e_2) = \varphi\begin{pmatrix} 0 \\ 1 \\ 0 \end{pmatrix} = \begin{pmatrix} 0 \\ 0 \\ 1 \end{pmatrix}, \qquad \varphi(e_3) = \varphi\begin{pmatrix} 0 \\ 0 \\ 1 \end{pmatrix} = \begin{pmatrix} 0 \\ 0 \\ 2 \end{pmatrix}.$$
  Dann ist
  $$\varphi(U) = \langle \varphi(e_2), \varphi(e_3) \rangle = \left\langle \begin{pmatrix} 0 \\ 0 \\ 1 \end{pmatrix}, \begin{pmatrix} 0 \\ 0 \\ 2 \end{pmatrix} \right\rangle = \left\langle \begin{pmatrix} 0 \\ 0 \\ 1 \end{pmatrix} \right\rangle,$$
  also die $x_3$-Achse.

- $\dim \varphi(U) = 1$, der Unterraum wird durch $\varphi$ also auf einen Unterraum kleinerer Dimension abgebildet.

- $\ker \varphi$: Für welche $\begin{pmatrix} x_1 \\ x_2 \\ x_3 \end{pmatrix} \in \mathbb{R}^3$ gilt $\varphi\begin{pmatrix} x_1 \\ x_2 \\ x_3 \end{pmatrix} = \begin{pmatrix} 0 \\ 0 \\ 0 \end{pmatrix}$? Hierfür lösen wir das LGS
  $$\begin{cases} x_1 & = 0 \\ 2x_1 & = 0 \\ x_1 + x_2 + 2x_3 & = 0. \end{cases}$$
  Das LGS hat die Lösungen $x_1 = 0,\ x_2 = -2x_3$ (die Variable $x_3$ ist freie Variable). Also ist
  $$\ker \varphi = \left\{ \begin{pmatrix} 0 \\ -2\lambda \\ \lambda \end{pmatrix} \;\Big|\; \lambda \in \mathbb{R} \right\} \quad \text{und} \quad \dim(\ker \varphi) = 1.$$
