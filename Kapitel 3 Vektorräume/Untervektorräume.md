---
tags: [kapitel-3, thema, definition, satz, beispiel]
quelle: Skript S. 40–43
aliases: [Untervektorraum, Unterraum, Unterraumkriterium]
---
# Untervektorräume

> Kapitel 3 · Vektorräume. Zurück zum [[Inhaltsverzeichnis]].
> Voriges Thema: [[Vektorräume (Kapitel 3)|Vektorräume]] · Nächstes Thema: [[Linearkombinationen und lineare (Un-)Abhängigkeit]]
> Grundlage: [[Vektorraum]], [[Verknüpfung und Abgeschlossenheit]]

Wie bei den Gruppen (vgl. [[Untergruppen]]) gibt es auch für Vektorräume eine Unterstruktur, also eine Teilmenge des Grundraums, die die gleichen Eigenschaften erfüllt wie der Grundraum.

## Definition 3.5 (Untervektorraum)

Sei $V$ mit $K, +, \cdot$ ein [[Vektorraum]]. Eine Teilmenge $\emptyset \neq U \subseteq V$ heißt **Untervektorraum** (oder **Unterraum**) von $V$, falls $U$ mit $K, +, \cdot$ selbst ein Vektorraum ist.

> [!info] Bemerkung
> Insbesondere muss dann $\mathcal{O} \in U$ gelten. Dieses Kriterium am besten immer kurz nachrechnen, wenn man prüfen soll, ob es sich bei einer gegebenen Teilmenge tatsächlich um einen Unterraum handelt. Oft kann man damit ohne großen Aufwand direkt ein Gegenbeispiel identifizieren.

## Beispiel 3.6

$U = \left\{ \begin{pmatrix} \lambda \\ 0 \end{pmatrix} \;\middle|\; \lambda \in \mathbb{R} \right\}$ ist Unterraum des Vektorraums $\mathbb{R}^2$, ebenso ist $W = \left\{ \begin{pmatrix} \lambda \\ 0 \end{pmatrix} \;\middle|\; \lambda \in K \right\}$ Unterraum des Vektorraums $K^2$ (für einen beliebigen Körper $K$). Für den Nachweis müssen alle Eigenschaften aus [[Vektorraum|Definition 3.1]] nachgeprüft werden. Deutlich weniger Aufwand ist es, den folgenden Satz zu verwenden.

## Satz 3.7 (Unterraumkriterium)

Sei $V$ ein $K$-Vektorraum. Eine Teilmenge $U \subseteq V$ ist ein Unterraum von $V$ **genau dann, wenn** die folgenden drei Eigenschaften erfüllt sind:

**(1)** $\mathcal{O} \in U$

**(2)** $u \in U,\; \lambda \in K \;\Rightarrow\; \lambda u \in U$

**(3)** $u, v \in U \;\Rightarrow\; u + v \in U$

> [!info] Bemerkung
> Es muss nicht explizit gefordert werden, dass der Nullvektor $\mathcal{O}$ in $U$ liegt. Diese Forderung steckt schon in (2), wenn man $\lambda = 0$ einsetzt, und in (3), wenn man $v = -u$ wählt. Wie oben schon gesagt, ist es aber ein einfach zu prüfendes Kriterium, das einen langen Beweis für ein Gegenbeispiel ersparen kann.
> Die Eigenschaften (2) und (3) können auch zusammengefasst werden zu folgender Forderung:
> $$\text{Für alle } u, v \in U,\; \lambda, \mu \in K \text{ gilt } \lambda u + \mu v \in U.$$

> [!note]- Beweis
> „$\Rightarrow$" &nbsp; $U$ ist laut Definition 3.5 selbst ein Vektorraum, deshalb gelten (1)–(3).
>
> „$\Leftarrow$" &nbsp; Wir zeigen: wenn die Eigenschaften (1)–(3) erfüllt sind, besitzt $U$ alle Eigenschaften eines Vektorraums. Wegen (1) ist $U$ nicht leer und es gilt $\mathcal{O} \in U$. Gibt es zusätzlich zu $\mathcal{O}$ noch ein weiteres Element $u$ in $U$, muss (wegen Eigenschaft (2)) der zu $u$ inverse Vektor $-u$ wegen $-u = (-1) \cdot u$ in $U$ liegen. Also ist $(U, +)$ eine abelsche Gruppe (Assoziativgesetz und Kommutativgesetz gelten in $V$ und damit auch in jeder Teilmenge von $V$).
> Wegen Eigenschaft (3) gilt, dass mit $u, v \in U$ auch $u + v \in U$ gilt, wegen Eigenschaft (2), dass für $\lambda \in K$ auch $\lambda u \in U$ erfüllt ist. Die übrigen in [[Vektorraum|Definition 3.1]] geforderten Eigenschaften sind für $U$ erfüllt, da sie bereits in $V$ gelten und an jede Teilmenge vererbt werden. $\qquad \blacksquare$

## Beispiel 3.8

**(a)** Sei $V$ ein $K$-Vektorraum, $\mathcal{O} \neq u, v \in V$ mit $u \neq v$. Dann ist
$$G = \{ \lambda v \mid \lambda \in K \}$$
ein Unterraum. Für $v = \mathcal{O}$ erhalten wir den Nullraum. Für $V = \mathbb{R}^n$ ist $G$ eine **Gerade durch den Nullpunkt**.

Ebenso ist
$$E = \{ \lambda u + \mu v \mid \lambda, \mu \in K \}$$
ein Unterraum. Für $V = \mathbb{R}^n$ ist $E$ eine **Ebene**, die durch den Nullpunkt geht.

Allerdings ist für $w \neq \mu v$ (für $\mu \in K$) die Menge
$$G' = \{ w + \lambda v \mid \lambda \in K \}$$
**kein** Unterraum von $V$! Der Nullvektor $\mathcal{O}$ liegt nicht in $G'$.

**(b)** Für $V = \mathbb{R}^3$ ist die Menge $U_1 = \left\{ \begin{pmatrix} x_1 \\ x_2 \\ x_3 \end{pmatrix} \in \mathbb{R}^3 \;\middle|\; x_1 + x_2 - x_3 = 0 \right\}$ ein Unterraum. Wir rechnen die Eigenschaften des Unterraumkriteriums 3.7 nach.

&nbsp;&nbsp;**(1)** Für $\mathcal{O} = \begin{pmatrix} 0 \\ 0 \\ 0 \end{pmatrix}$ ist die für $U_1$ geforderte Bedingung $x_1 + x_2 - x_3 = 0$ erfüllt, denn $0 + 0 - 0 = 0$.

&nbsp;&nbsp;**(2)** Sei $\lambda \in \mathbb{R},\; v = \begin{pmatrix} v_1 \\ v_2 \\ v_3 \end{pmatrix} \in U_1$, d. h. $v_1 + v_2 - v_3 = 0$ gilt. Zu prüfen ist, ob $\lambda v \in U_1$ gilt. Es ist $\lambda v = \begin{pmatrix} \lambda v_1 \\ \lambda v_2 \\ \lambda v_3 \end{pmatrix}$, und $\lambda v_1 + \lambda v_2 - \lambda v_3 = \lambda \cdot \underbrace{(v_1 + v_2 - v_3)}_{=\,0} = \lambda \cdot 0 = 0$, also ist $\lambda v \in U_1$.

&nbsp;&nbsp;**(3)** Seien $v = \begin{pmatrix} v_1 \\ v_2 \\ v_3 \end{pmatrix},\; w = \begin{pmatrix} w_1 \\ w_2 \\ w_3 \end{pmatrix} \in U_1$, d. h. $v_1 + v_2 - v_3 = 0,\; w_1 + w_2 - w_3 = 0$ gilt. Zu prüfen ist, ob $v + w \in U_1$ gilt. Es ist $v + w = \begin{pmatrix} v_1 + w_1 \\ v_2 + w_2 \\ v_3 + w_3 \end{pmatrix}$ und
$$(v_1 + w_1) + (v_2 + w_2) - (v_3 + w_3) = \underbrace{v_1 + v_2 - v_3}_{=\,0} + \underbrace{w_1 + w_2 - w_3}_{=\,0}, \quad \text{also } v + w \in U_1.$$

Die Menge $U_1$ lässt sich schreiben als
$$U_1 = \left\{ \begin{pmatrix} x_1 \\ x_2 \\ x_1 + x_2 \end{pmatrix} \;\middle|\; x_1, x_2 \in \mathbb{R} \right\} = \left\{ x_1 \cdot \begin{pmatrix} 1 \\ 0 \\ 1 \end{pmatrix} + x_2 \cdot \begin{pmatrix} 0 \\ 1 \\ 1 \end{pmatrix} \;\middle|\; x_1, x_2 \in \mathbb{R} \right\},$$
d. h. $U_1$ ist die Ebene durch $\mathcal{O}$ mit Richtungsvektoren $\begin{pmatrix} 1 \\ 0 \\ 1 \end{pmatrix}$ und $\begin{pmatrix} 0 \\ 1 \\ 1 \end{pmatrix}$.

**(c)** $U_2 = \left\{ \begin{pmatrix} x_1 \\ x_2 \\ x_3 \end{pmatrix} \in \mathbb{R}^3 \;\middle|\; x_1 + x_2 - x_3 = 1 \right\}$ ist **kein** Unterraum (wieso? Geometrische Interpretation?).

> [!tip]- Warum ist $U_2$ kein Unterraum?
> Der Nullvektor $\mathcal{O}$ erfüllt die Bedingung nicht: $0 + 0 - 0 = 0 \neq 1$, also $\mathcal{O} \notin U_2$. Geometrisch ist $U_2$ eine Ebene, die **nicht** durch den Ursprung geht (eine zu $U_1$ parallel verschobene Ebene).

**(d)** $U_3 = \left\{ \begin{pmatrix} x_1 \\ x_2 \\ x_3 \end{pmatrix} \in \mathbb{R}^3 \;\middle|\; x_1^2 + x_2^2 + x_3^2 \leq 1 \right\}$ ist **kein** Unterraum:

Es gilt zwar $\mathcal{O} \in U_3$, aber beispielsweise ist $\begin{pmatrix} 1 \\ 0 \\ 0 \end{pmatrix} \in U_3$ (denn $1^2 + 0^2 + 0^2 \leq 1$), aber $2 \cdot \begin{pmatrix} 1 \\ 0 \\ 0 \end{pmatrix} = \begin{pmatrix} 2 \\ 0 \\ 0 \end{pmatrix} \notin U_3$ (denn $2^2 + 0^2 + 0^2 > 1$).

Geometrische Interpretation: Die Menge $U_3$ ist die **Kugel** um $\mathcal{O}$ mit Radius $1$.

**(e)** Für ein Intervall $I \subseteq \mathbb{R}$ ist die Menge $C(I)$ der stetigen Funktionen auf $I$ ein Unterraum des Vektorraums $\mathcal{F}(I, \mathbb{R})$ (die Verknüpfung stetiger Funktionen ist stetig, *Mathematik 1*).

## Verwandte Themen

- [[Vektorräume (Kapitel 3)|Vektorräume]] — Grundraum und Funktionenraum $\mathcal{F}(M, K)$
- [[Erzeugte Unterräume, Schnitt und Summe von Unterräumen]] — wie man aus Vektoren Unterräume gewinnt und wie man sie kombiniert
- [[Dimension und Basis]] — Kennzahlen eines (Unter-)Raums
