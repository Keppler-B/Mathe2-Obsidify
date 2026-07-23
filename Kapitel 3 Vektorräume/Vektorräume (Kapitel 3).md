---
tags: [kapitel-3, thema, definition, beispiel, satz]
quelle: Skript S. 37–39
aliases: [Vektorräume]
---
# Vektorräume

> Kapitel 3 · Vektorräume — erster Abschnitt. Zurück zum [[Inhaltsverzeichnis]].
> Voriges Thema: [[Der Körper der komplexen Zahlen]] (Kapitel 2) · Nächstes Thema: [[Untervektorräume]]
> Grundlage: [[Körper]], [[Gruppe]], [[Verknüpfung und Abgeschlossenheit]]

Mit diesem Kapitel beginnt der Vorlesungsteil zur *linearen Algebra*. Der Begriff eines Vektors im reellen Vektorraum $\mathbb{R}^n$ ist aus der Schule bekannt. Hier betrachten wir allgemeiner Vektoren als Elemente eines abstrakten Vektorraums über einem beliebigen [[Körper]].

![[Vektorraum#Definition 3.1 (K-Vektorraum)]]

## Beispiel 3.2

Für einen beliebigen Körper $K$ wird
$$V = K^n := \left\{ \begin{pmatrix} v_1 \\ \vdots \\ v_n \end{pmatrix} \;\middle|\; v_1, \dots, v_n \in K \right\},$$
der **Raum der Spaltenvektoren** mit $n$ Einträgen aus $K$, ein Vektorraum mittels der folgenden Verknüpfungen:

Für $\lambda \in K$ und $v = \begin{pmatrix} v_1 \\ \vdots \\ v_n \end{pmatrix},\; w = \begin{pmatrix} w_1 \\ \vdots \\ w_n \end{pmatrix} \in V$ ist
$$\lambda v = \begin{pmatrix} \lambda v_1 \\ \vdots \\ \lambda v_n \end{pmatrix}$$
(was einer Streckung des Vektors $v$ mit dem Faktor $\lambda$ entspricht) und
$$v + w = \begin{pmatrix} v_1 + w_1 \\ \vdots \\ v_n + w_n \end{pmatrix}.$$

Der Nullvektor ist $\mathcal{O} = \begin{pmatrix} 0 \\ \vdots \\ 0 \end{pmatrix}$, der zu $v \in V$ inverse Vektor ist $-v = \begin{pmatrix} -v_1 \\ \vdots \\ -v_n \end{pmatrix}$.

**(a)** Für $K = \mathbb{R}$ ist diese Art von Vektorräumen bereits aus der Schule bekannt. (Dort wurden Vektoren aus dem $\mathbb{R}^2$ oder $\mathbb{R}^3$ betrachtet.)

**(b)** $K = \mathbb{Z}_2,\; V_1 = \mathbb{Z}_2^2 = \left\{ \begin{pmatrix} x_1 \\ x_2 \end{pmatrix} \;\middle|\; x_1, x_2 \in \mathbb{Z}_2 \right\}.$

$V_1$ hat vier Elemente: $\mathcal{O} = \begin{pmatrix} 0 \\ 0 \end{pmatrix}, \begin{pmatrix} 0 \\ 1 \end{pmatrix}, \begin{pmatrix} 1 \\ 0 \end{pmatrix}, \begin{pmatrix} 1 \\ 1 \end{pmatrix}.$

Für die Verknüpfung $+$ gilt beispielsweise $\begin{pmatrix} 0 \\ 1 \end{pmatrix} + \begin{pmatrix} 0 \\ 1 \end{pmatrix} = \begin{pmatrix} 0 \\ 0 \end{pmatrix}$ (d. h. $-\begin{pmatrix} 0 \\ 1 \end{pmatrix} = \begin{pmatrix} 0 \\ 1 \end{pmatrix}$), $\;\begin{pmatrix} 1 \\ 0 \end{pmatrix} + \begin{pmatrix} 0 \\ 1 \end{pmatrix} = \begin{pmatrix} 1 \\ 1 \end{pmatrix},\; \begin{pmatrix} 0 \\ 1 \end{pmatrix} + \begin{pmatrix} 1 \\ 1 \end{pmatrix} = \begin{pmatrix} 1 \\ 0 \end{pmatrix}.$

Für die skalare Multiplikation gilt $0 \cdot v = \mathcal{O},\; 1 \cdot v = v$ für alle $v \in V_1$. (Mehr Skalare gibt es nicht in $\mathbb{Z}_2$.)

**(c)** $K = \mathbb{Z}_5,\; V_2 = \mathbb{Z}_5^3 = \left\{ \begin{pmatrix} x_1 \\ x_2 \\ x_3 \end{pmatrix} \;\middle|\; x_1, x_2, x_3 \in \mathbb{Z}_5 \right\}.$

Beispielsweise sind $v = \begin{pmatrix} 0 \\ 1 \\ 2 \end{pmatrix},\; w = \begin{pmatrix} 3 \\ 2 \\ 4 \end{pmatrix} \in V_2$,
$$-v = \begin{pmatrix} 0 \\ 4 \\ 3 \end{pmatrix},\quad -w = \begin{pmatrix} 2 \\ 3 \\ 1 \end{pmatrix},\quad v + w = \begin{pmatrix} 3 \\ 3 \\ 1 \end{pmatrix},$$
$$1 \cdot w = w,\quad 2 \cdot w = \begin{pmatrix} 1 \\ 4 \\ 3 \end{pmatrix},\quad \text{usw.}$$
$V_2$ enthält $5 \cdot 5 \cdot 5 = 5^3 = 125$ Vektoren.

> [!info]- Nachrechnen der $\mathbb{Z}_5$-Einträge (mod 5)
> Alle Rechnungen modulo $5$: $-1 = 4,\; -2 = 3,\; -4 = 1$, also $-v = (0, -1, -2)^\top = (0, 4, 3)^\top$ und $-w = (-3, -2, -4)^\top = (2, 3, 1)^\top$. Summe: $v + w = (0{+}3,\, 1{+}2,\, 2{+}4)^\top = (3, 3, 6)^\top = (3, 3, 1)^\top$. Weiter $2 \cdot w = (6, 4, 8)^\top = (1, 4, 3)^\top$.

## Beispiel 3.3 (Weitere Beispiele für Vektorräume)

**(a)** Der **triviale Vektorraum** (oder **Nullraum**): $K$ beliebig, $V = \{\mathcal{O}\}$ mit $\mathcal{O} + \mathcal{O} = \mathcal{O},\; \lambda \cdot \mathcal{O} = \mathcal{O}$ für alle $\lambda \in K$.

**(b)** $\mathbb{R}$ kann als $\mathbb{R}$-Vektorraum aufgefasst werden. Die Vektoren sind reelle Zahlen, die Skalare ebenfalls.

**(c)** **Funktionenraum**: Für einen Körper $K$ und eine Menge $M \neq \emptyset$ sei
$$V = \mathcal{F}(M, K) = \{ f \mid f : M \to K \}$$
die Menge der auf $M$ definierten Abbildungen (Funktionen) mit Werten in $K$. Oft ist $K = \mathbb{R}$ und die betrachteten Abbildungen $f : M \to \mathbb{R}$ sind dann reelle Funktionen. Für $f, g \in V$ und $\lambda \in K$ sei
$$f + g : M \to K,\quad (f + g)(x) = f(x) + g(x) \quad \text{für alle } x \in M,$$
$$\lambda \cdot f : M \to K,\quad (\lambda \cdot f)(x) = \lambda \cdot f(x) \quad \text{für alle } x \in M.$$
Damit ist $V$ mit $K, +, \cdot$ ein Vektorraum. Der Nullvektor $\mathcal{O}$ ist die Funktion $f : M \to K,\; f(x) = 0$ für alle $x \in M$ (die **Nullfunktion** $f = \mathcal{O}$).

## Satz 3.4 (Rechnen in Vektorräumen)

Sei $V$ ein $K$-Vektorraum, $v \in V$, $\lambda \in K$. Dann gilt

**(a)** $0 \cdot v = \mathcal{O}$

**(b)** $\lambda \cdot \mathcal{O} = \mathcal{O}$

**(c)** $(-1) \cdot v = -v$ &nbsp;(und damit auch $(-\lambda) \cdot v = -(\lambda v)$)

> [!note]- Beweis
> **(a)** Für $\mathcal{O}$ gilt $\mathcal{O} = v + (-v)$ für alle $v \in V$ (vgl. [[Vektorraum|Definition 3.1(1)]]). Also gilt auch (statt $v$ verwenden wir jetzt den Vektor $0 \cdot v$)
> $$\begin{aligned}
> \mathcal{O} &= 0 \cdot v + (-(0 \cdot v)) \\
> &= (0 + 0) \cdot v + (-(0 \cdot v)) \\
> &\overset{3.1(2.2)}{=} (0 \cdot v + 0 \cdot v) + (-(0 \cdot v)) \\
> &\overset{3.1(1)}{=} 0 \cdot v + (0 \cdot v + (-(0 \cdot v))) \\
> &= 0 \cdot v + \mathcal{O} \\
> &\overset{3.1(1)}{=} 0 \cdot v,
> \end{aligned}$$
> also $\mathcal{O} = 0 \cdot v$.
>
> **(b)** analog zu (a), starte mit $\mathcal{O} = \lambda \cdot \mathcal{O} + (-(\lambda \cdot \mathcal{O}))$, erhalte $\mathcal{O} = \cdots = \lambda \cdot \mathcal{O}$.
> Andere Möglichkeit:
> $$\lambda \cdot \mathcal{O} \overset{\text{Teil (a)}}{=} \lambda \cdot (0 \cdot \mathcal{O}) \overset{3.1(2.1)}{=} \underbrace{(\lambda \cdot 0)}_{=\,0} \cdot \mathcal{O} \overset{\text{Teil (a)}}{=} \mathcal{O}.$$
>
> **(c)**
> $$v + (-1) \cdot v \overset{3.1(2.4)}{=} 1 \cdot v + (-1) \cdot v \overset{3.1(2.2)}{=} (1 + (-1)) \cdot v \overset{K\text{ Körper}}{=} 0 \cdot v \overset{(a)}{=} \mathcal{O},$$
> damit folgt (c). $\qquad \blacksquare$

## Weiter im Kapitel

- [[Untervektorräume]] — Teilmengen, die selbst ein Vektorraum sind
- [[Linearkombinationen und lineare (Un-)Abhängigkeit]]
- [[Dimension und Basis]] · [[Austauschsatz von Steinitz und Basisergänzungssatz]]
- [[Erzeugte Unterräume, Schnitt und Summe von Unterräumen]]
