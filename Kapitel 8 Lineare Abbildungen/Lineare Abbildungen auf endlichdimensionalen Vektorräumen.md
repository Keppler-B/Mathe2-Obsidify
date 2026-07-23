---
tags: [kapitel-8, thema, satz, beispiel, korollar]
quelle: Skript S. 107–110
---
# Lineare Abbildungen auf endlichdimensionalen Vektorräumen

> Kapitel 8 · Lineare Abbildungen — drittes Thema (letztes Thema des Skripts). Zurück zum [[Inhaltsverzeichnis]].
> Voriges Thema: [[Rang und Kern linearer Abbildungen]]
> Grundlage: [[Lineare Abbildung]], [[Dimension und Basis]], [[Matrix]], [[Abbildungen (injektiv, surjektiv, bijektiv)]]

Der folgende Satz ist eine wichtige Grundlage für den Zusammenhang zwischen linearen Abbildungen und Matrizen, auf den wir im nächsten Kapitel (in *Mathematik 3*) eingehen werden.

## Satz 8.9

Gegeben seien die $K$-[[Vektorraum|Vektorräume]] $V$ und $W$, wobei $\dim V = n$. Seien zudem $\{v_1, \dots, v_n\}$ eine [[Dimension und Basis|Basis]] von $V$ und $w_1, \dots, w_n$ (nicht notwendigerweise verschiedene) Vektoren aus $W$. Dann existiert **genau eine** [[Lineare Abbildung|lineare Abbildung]]
$$\varphi : V \to W \quad \text{mit} \quad \varphi(v_i) = w_i \quad \text{für alle } i \in \{1, \dots, n\},$$
und zwar
$$\varphi : V \to W, \quad v = \sum_{i=1}^{n} \lambda_i v_i \mapsto \sum_{i=1}^{n} \lambda_i \underbrace{w_i}_{\varphi(v_i)}.$$

Das heißt: Weiß man, wie die Basisvektoren abgebildet werden, so kennt man die lineare Abbildung vollständig.

> [!note]- Beweis
> Für obiges $\varphi$ gilt:
>
> - $\varphi$ ist linear.
> - $\varphi(v_i) = w_i$, da $\varphi(v_1) = \varphi(1 v_1 + 0 v_2 + \dots + 0 v_n) = 1 w_1 + 0 w_2 + \dots + 0 w_n = w_1$, usw.
> - $\varphi$ ist eindeutig: Angenommen, es gibt eine lineare Abbildung $\psi : V \to W$ mit $\psi(v_i) = w_i$ für alle $i$. Dann ist
>   $$\psi\Big(\sum_{i=1}^{n} \lambda_i v_i\Big) \underset{\psi\ \text{linear}}{=} \sum_{i=1}^{n} \lambda_i \psi(v_i) = \sum_{i=1}^{n} \lambda_i w_i \underset{\varphi\ \text{linear}}{=} \varphi\Big(\sum_{i=1}^{n} \lambda_i v_i\Big).$$
>   Also gilt $\psi(v) = \varphi(v)$ für jedes $v \in V$, die beiden Abbildungen sind also gleich und damit ist $\varphi$ eindeutig. $\qquad \blacksquare$

## Beispiel 8.10 (Drehmatrix)

Sei $V = \mathbb{R}^2$ und $\varphi_\alpha : \mathbb{R}^2 \to \mathbb{R}^2$ eine Drehung um den Ursprung um den Winkel $\alpha \in [0, 2\pi)$ gegen den Uhrzeigersinn. Die Abbildung $\varphi_\alpha$ ist linear. Wie sieht die Darstellung mit einer Matrix $A$ aus?

Nach dem vorherigen Satz reicht es zu wissen, wie die Basisvektoren durch $\varphi_\alpha$ abgebildet werden:
$$e_1 = \begin{pmatrix} 1 \\ 0 \end{pmatrix} \overset{\varphi_\alpha}{\longmapsto} \begin{pmatrix} \cos \alpha \\ \sin \alpha \end{pmatrix}, \qquad e_2 = \begin{pmatrix} 0 \\ 1 \end{pmatrix} \overset{\varphi_\alpha}{\longmapsto} \begin{pmatrix} -\sin \alpha \\ \cos \alpha \end{pmatrix}.$$

Für einen beliebigen Vektor $x = \begin{pmatrix} x_1 \\ x_2 \end{pmatrix}$ gilt $x = \begin{pmatrix} x_1 \\ x_2 \end{pmatrix} = x_1 \cdot \begin{pmatrix} 1 \\ 0 \end{pmatrix} + x_2 \cdot \begin{pmatrix} 0 \\ 1 \end{pmatrix}$. Wegen der Linearität von $\varphi_\alpha$ gilt
$$\begin{aligned}
\varphi_\alpha(x) &= x_1 \cdot \varphi_\alpha\begin{pmatrix} 1 \\ 0 \end{pmatrix} + x_2 \cdot \varphi_\alpha\begin{pmatrix} 0 \\ 1 \end{pmatrix} \\
&= x_1 \cdot \begin{pmatrix} \cos \alpha \\ \sin \alpha \end{pmatrix} + x_2 \cdot \begin{pmatrix} -\sin \alpha \\ \cos \alpha \end{pmatrix} \\
&= \begin{pmatrix} x_1 \cdot \cos \alpha - x_2 \cdot \sin \alpha \\ x_1 \cdot \sin \alpha + x_2 \cdot \cos \alpha \end{pmatrix} \\
&= A \cdot x \quad \text{mit} \quad A = \begin{pmatrix} \cos \alpha & -\sin \alpha \\ \sin \alpha & \cos \alpha \end{pmatrix}.
\end{aligned}$$

Beispielsweise erhält man für $\alpha = 0$ die Einheitsmatrix, $A = E_2 = \begin{pmatrix} 1 & 0 \\ 0 & 1 \end{pmatrix}$, und für $\alpha = 90^\circ$ die Matrix $A = \begin{pmatrix} 0 & -1 \\ 1 & 0 \end{pmatrix}$.

## Satz 8.11 (Dimensionssatz für lineare Abbildungen)

Seien $V$ und $W$ Vektorräume über einem [[Körper]] $K$ mit $\dim V = n$, und sei $\varphi : V \to W$ eine lineare Abbildung. Dann gilt
$$\dim V = \dim(\ker \varphi) + \mathrm{rg}(\varphi) \quad \big(= \dim(\ker \varphi) + \dim(\varphi(V))\big).$$

> [!note]- Beweis
> Sei $\{u_1, \dots, u_k\}$ eine Basis von $\ker \varphi$. Mithilfe des Basisergänzungssatzes ergänzen wir sie zu einer Basis $\{u_1, \dots, u_n\}$ von $V$ und setzen $U := \langle u_{k+1}, \dots, u_n \rangle_K$.
>
> Da $\ker \varphi \cap U = \{\mathcal{O}\}$ und $V = \ker \varphi + U$, ist $\dim(V) = \dim(\ker \varphi) + \dim(U)$.
>
> Wir zeigen: $\dim U \overset{(1)}{=} \dim \varphi(U) \overset{(2)}{=} \underbrace{\dim \varphi(V)}_{=\, \mathrm{rg}\,\varphi}$:
>
> **(1)** $\ker \varphi \cap U = \{\mathcal{O}\} \Rightarrow \ker(\varphi|_U) = \{\mathcal{O}\} \underset{8.7(b)}{\Rightarrow} \varphi|_U$ injektiv $\Rightarrow \dim U = \dim \varphi(U)$.
>
> **(2)** $\dim \varphi(U) = \dim \varphi(V)$, da
>   $$\varphi(V) = \varphi(U + \ker \varphi) \underset{\varphi\ \text{linear}}{=} \varphi(U) + \underbrace{\varphi(\ker \varphi)}_{=\, \mathcal{O}} = \varphi(U). \qquad \blacksquare$$

## Korollar 8.12 (Äquivalenzsatz für lineare Abbildungen auf endlichen Vektorräumen gleicher Dimension)

Seien $V$ und $W$ zwei $K$-Vektorräume mit $\dim V = \dim W = n$ und $\varphi : V \to W$ eine lineare Abbildung. Dann sind äquivalent:

**(a)** $\varphi$ ist [[Abbildungen (injektiv, surjektiv, bijektiv)|surjektiv]],
**(b)** $\varphi$ ist injektiv,
**(c)** $\varphi$ ist bijektiv.

> [!note]- Beweis
> Aus der Dimensionsformel 8.11 folgt $n = \dim(\ker \varphi) + \mathrm{rg}(\varphi)$. $\quad (\star)$ Damit folgt
> $$\varphi \text{ surjektiv} \iff \mathrm{rg}\,\varphi = n \underset{(\star)}{\iff} \dim(\ker \varphi) = 0 \underset{8.7(b)}{\iff} \varphi \text{ injektiv}. \qquad \blacksquare$$
