---
tags: [kapitel-2, thema, definition, satz, beispiel]
quelle: Skript S. 25–29
aliases: [Polynomring, K[x]]
---
# Polynomringe

> Kapitel 2 · Ringe und Körper — ein weiteres Beispiel für Ringe, deren Elemente **Polynome** sind. Zurück zum [[Inhaltsverzeichnis]].
> Voriges Thema: [[Körper]] · Nächstes Thema: [[Der Körper der komplexen Zahlen]]
> Grundlage: [[Ring]], [[Körper]].

Wir lernen nun ein weiteres Beispiel für Ringe und Körper kennen. Ihre Elemente sind nicht wie bei den bisherigen Beispielen Zahlen, sondern **Polynome**, die wir hier als formalen Ausdruck auffassen.

## Definition 2.8 (Polynome über $K$)

Sei $K$ ein [[Körper]] mit $0$ und $1$.

**(a)** Ein **Polynom über $K$** (in einer Veränderlichen $x$) ist ein Ausdruck
$$f = \underbrace{a_0 x^0}_{= a_0} + \underbrace{a_1 x^1}_{= a_1 x} + \cdots + a_n x^n,$$
wobei $n \in \mathbb{N}_0$ und $a_i \in K$ für $i \in \{0, \dots, n\}$, die **Koeffizienten** von $f$. Wir schreiben auch $f(x)$ statt $f$ und $a_i \cdot x^i$ statt $a_i x^i$.
Ist $a_i = 0$, so kann $a_i x^i$ ($= 0 x^i$) bei der Beschreibung des Polynoms weggelassen werden. Statt $a_0 x^0$ schreibt man auch $a_0$, statt $a_1 x^1$ schreibt man auch $a_1 x$.
Sind alle $a_i = 0$, so nennt man $f$ das **Nullpolynom** und schreibt $f = 0$.

**(b)** Mit $K[x]$ bezeichnen wir die **Menge aller Polynome** über $K$.

**(c)** Zwei Polynome $f, g \in K[x]$ sind **gleich** (in Zeichen: $f = g$), wenn gilt
- $f = 0$ und $g = 0$ oder
- für $f = a_0 + a_1 x + \cdots + a_n x^n$, $g = b_0 + b_1 x + \cdots + b_m x^m$ mit $a_n \neq 0$, $b_m \neq 0$ gilt $n = m$ und $a_i = b_i$ für alle $i \in \{0, \dots, n\}$.

## Beispiel 2.9

**(a)** $f(x) = 3x^2 + \tfrac{2}{3} x - 1 \in \mathbb{Q}[x]$

**(b)** $g(x) = x^7 + x^2 + 1 \in \mathbb{Z}_2[x]$. Die Koeffizienten dieses Polynoms sind entweder $1$ ($a_0, a_2, a_7$) oder $0$ (alle anderen $a_i$).

## Definition/Satz 2.10 (Polynomring)

Wir wollen in $K[x]$ wie mit ganzen Zahlen (also wie in einem Ring) rechnen können. Dazu brauchen wir eine Addition und eine Multiplikation für Polynome.

Sei $K$ ein Körper, dann wird $K[x]$ durch die folgenden Verknüpfungen zu einem **kommutativen Ring mit Eins**:
Für $f = \sum_{i=0}^{n} a_i x^i$, $g = \sum_{j=0}^{m} b_j x^j$ ist
$$f + g := \sum_{i=0}^{\max(m,n)} (a_i + b_i) x^i$$
und
$$f \cdot g := \sum_{i=0}^{n+m} c_i x^i$$
mit $c_i = \sum_{j=0}^{i} a_j b_{i-j} = a_0 b_i + a_1 b_{i-1} + \cdots + a_i b_0$ (**Faltungsprodukt**).

Die $c_i$ ergeben sich so:
$$f \cdot g = (a_0 + a_1 x + \cdots + a_n x^n)(b_0 + b_1 x + \cdots + b_m x^m)$$
$$= \underbrace{a_0 b_0}_{c_0} + \underbrace{(a_0 b_1 + a_1 b_0)}_{c_1} x + \ldots \underbrace{(\ldots)}_{c_{n+m}} x^{n+m}.$$

Das **Einselement** ist $f = 1$ ($a_0 = 1$, $a_i = 0$ für alle $i \geq 1$), das **Nullelement** ist $f = 0$. Der so definierte Ring $K[x]$ heißt der **Polynomring** in einer Variablen über $K$.

> [!note]- Beweis
> Ringeigenschaften nachrechnen. $\qquad \blacksquare$

## Bemerkung 2.11

**(a)** Die Ausdrücke $a_0, a_1 x, a_2 x^2, \dots, a_n x^n$ heißen **Monome**, $a_n x^n$ heißt **Leitterm** von $f = a_0 + \cdots + a_n x^n$ (mit $a_n \neq 0$).

**(b)** Die Pluszeichen in der Beschreibung der Polynome entsprechen der in 2.10 definierten Ringaddition der Monome.

## Beispiel 2.12

**(a)** In $\mathbb{Q}[x]$ und $\mathbb{R}[x]$ funktioniert alles, wie wir es aus der Schule kennen, z. B. $f = 2x^2 + 5x + 1$, $g = 3x^3 - 2x \in \mathbb{Q}[x]$:
$$f + g = 3x^3 + 2x^2 + 3x + 1 \in \mathbb{Q}[x]$$
$$f \cdot g = (2x^2 + 5x + 1) \cdot (3x^3 - 2x) = 6x^5 - 4x^3 + 15x^4 - 10x^2 + 3x^3 - 2x$$
$$= 6x^5 + 15x^4 - x^3 - 10x^2 - 2x \in \mathbb{Q}[x]$$

**(b)** $f = 2x^3 + 1$, $g = x + 2 \in \mathbb{Z}_3[x]$:
$$f + g = 2x^3 + x + (\underbrace{2 + 1}_{\equiv 0 \bmod 3}) = 2x^3 + x \in \mathbb{Z}_3[x]$$
$$f \cdot g = (2x^3 + 1)(x + 2) = 2x^4 + (\underbrace{2 \cdot 2}_{\equiv 1 \bmod 3}) x^3 + x + 2 = 2x^4 + x^3 + x + 2 \in \mathbb{Z}_3[x]$$

**(c)** $f = x^2 + 1$, $g = x + 1 \in \mathbb{Z}_2[x]$:
$$f + f = 0 \in \mathbb{Z}_2[x], \qquad g \cdot g = (x + 1)(x + 1) = x^2 + x + x + 1 = x^2 + 1 \in \mathbb{Z}_2[x]$$

## Definition 2.13 (Grad eines Polynoms)

Sei $0 \neq f \in K[x]$ ein Polynom, $f = a_0 + a_1 x + \cdots + a_n x^n$ mit $a_n \neq 0$. Dann heißt $n$ der **Grad** von $f$, Schreibweise: $\operatorname{grad}(f) = n$.
Wir legen fest: $\operatorname{grad}(0) = -\infty$, und $\operatorname{grad}(g) = 0$, falls $g$ ein konstantes Polynom ungleich dem Nullpolynom ist (d. h. ein Polynom mit $a_0 \neq 0$, $a_i = 0$ für alle $i \geq 1$).

## Satz 2.14 (Gradformel)

Sei $K$ ein Körper, $f, g \in K[x]$ Polynome. Dann gilt
$$\operatorname{grad}(f \cdot g) = \operatorname{grad}(f) + \operatorname{grad}(g).$$
Dabei gilt die Konvention $-\infty + (-\infty) = -\infty + n = -\infty$ für alle $n \in \mathbb{N}_0$.

> [!note]- Beweis
> - Die Formel ist nach der Konvention wahr für $f = 0$ oder $g = 0$.
> - Für alle anderen Fälle nehmen wir an, dass $f$ den Leitterm $a_n x^n$ besitzt und $g$ den Leitterm $b_m x^m$ (und damit $a_n \neq 0$, $b_m \neq 0$). Dann ist $\operatorname{grad}(f) = n$, $\operatorname{grad}(g) = m$, und $(a_n \cdot b_m) x^{n+m}$ ist Leitterm von $f \cdot g$. Nach [[Körper|Satz 2.7]] (Nullteilerfreiheit von $K$) kann $a_n \cdot b_m$ nicht Null sein, woraus $\operatorname{grad}(f \cdot g) = n + m$ folgt. $\qquad \blacksquare$

## Korollar 2.15

Aus der Gradformel lässt sich direkt folgern, welche Elemente in $K[x]$ bezüglich der Multiplikation invertierbar (also Einheiten) sind.

Sei $K$ ein Körper, dann ist
$$K[x]^* = \{f \in K[x] \mid \operatorname{grad}(f) = 0\},$$
d. h., nur die **konstanten Polynome ungleich $0$** sind invertierbar bezüglich der Multiplikation in $K[x]$.

> [!note]- Beweis
> Die multiplikative Inverse zu $f \in K[x]$ sei $f^{-1}$, es gilt also $1 = f \cdot f^{-1}$. Damit folgt
> $$0 = \operatorname{grad}(1) = \operatorname{grad}(f \cdot f^{-1}) \overset{\text{Satz 2.14}}{=} \operatorname{grad}(f) + \operatorname{grad}(f^{-1}).$$
> Dies ist nur möglich für $\operatorname{grad}(f) = \operatorname{grad}(f^{-1}) = 0$, d. h., wenn $f$ (und $f^{-1}$) ein konstantes Polynom ist.
>
> Umgekehrt gilt, dass ein konstantes Polynom ungleich dem Nullpolynom eine Einheit ist: Sei $f = a_0 \neq 0$. Da $a_0 \neq 0$ in $K$ invertierbar ist, gilt $f^{-1} = a_0^{-1}$ und damit $f \cdot f^{-1} = f^{-1} \cdot f = 1$. $\qquad \blacksquare$

## Definition 2.16 (Teilbarkeit im Polynomring)

Mit Polynomen lässt sich (wegen der Ringstruktur) wie mit ganzen Zahlen rechnen. Wir können verschiedene von $\mathbb{Z}$ bekannte Konzepte auf Polynome übertragen, etwa **Teilbarkeit** und **Division mit Rest** (und wie wir in *Mathematik 3* sehen werden, gibt es auch „Primpolynome" (sogenannte *irreduzible Polynome*) analog zu den Primzahlen).

Sei $K$ ein Körper und $f, g \in K[x]$. Wir sagen, **$f$ teilt $g$**, in Zeichen $f \mid g$, falls ein Polynom $q \in K[x]$ existiert, so dass $g = q \cdot f$ gilt. (Nach der Gradformel (Satz 2.14) ist dann $\operatorname{grad}(f) \leq \operatorname{grad}(g)$, falls $g \neq 0$.)

## Bemerkung 2.17 (Division mit Rest im Polynomring)

Wie in $\mathbb{Z}$ gibt es für Polynome die Division mit Rest.

Sei $0 \neq f \in K[x]$ und $g \in K[x]$. Dann existieren **eindeutig bestimmte** Polynome $q, r \in K[x]$ mit
$$g = q \cdot f + r, \quad \text{und} \quad \operatorname{grad}(r) < \operatorname{grad}(f).$$
Wie in $\mathbb{Z}$ wird das Polynom $q$ als **Quotient** bezeichnet und $r$ als **Rest** oder $g \bmod f$.

## Beispiel 2.18

**(a)** $g = x^4 + 2x^3 - x + 2$, $f = 3x^2 - 1 \in \mathbb{R}[x]$:
$$
\begin{array}{l}
(x^4 + 2x^3 + 0x^2 - 1x + 2) : (3x^2 - 1) = \tfrac{1}{3}x^2 + \tfrac{2}{3}x + \tfrac{1}{9} \quad \text{Rest } \left(-\tfrac{1}{3}x + \tfrac{19}{9}\right) \\[2pt]
\underline{-(x^4 + 0x^3 - \tfrac{1}{3}x^2)} \\[2pt]
\qquad\quad 2x^3 + \tfrac{1}{3}x^2 - 1x + 2 \\[2pt]
\qquad\quad \underline{-(2x^3 + 0x^2 - \tfrac{2}{3}x)} \\[2pt]
\qquad\qquad\qquad \tfrac{1}{3}x^2 - \tfrac{1}{3}x + 2 \\[2pt]
\qquad\qquad\qquad \underline{-(\tfrac{1}{3}x^2 + 0x - \tfrac{1}{9})} \\[2pt]
\qquad\qquad\qquad\qquad\quad -\tfrac{1}{3}x + \tfrac{19}{9}
\end{array}
$$
Hier ist also $q = \tfrac{1}{3}x^2 + \tfrac{2}{3}x + \tfrac{1}{9}$ und $r = -\tfrac{1}{3}x + \tfrac{19}{9}$ (beachte außerdem $\operatorname{grad}(r) < \operatorname{grad}(f)$).

**(b)** $g = x^4 + x^2 + 1$, $f = x^2 + x \in \mathbb{Z}_2[x]$:
$$
\begin{array}{l}
(x^4 + 0x^3 + x^2 + 0x + 1) : (x^2 + x) = x^2 + x \quad \text{Rest } 1 \\[2pt]
\underline{-(x^4 + x^3)} \\[2pt]
\qquad\quad x^3 + x^2 + 0x + 1 \\[2pt]
\qquad\quad \underline{-(x^3 + x^2)} \\[2pt]
\qquad\qquad\qquad\qquad\quad 1
\end{array}
$$
Hier ist $q = x^2 + x$ und $r = 1$.

## Korollar 2.19 (Linearfaktoren und Nullstellen)

Als Folgerung aus der Division mit Rest erhalten wir folgendes Korollar.

Sei $K$ ein Körper, $b \in K$. Das Polynom $f \in K[x]$ ist genau dann durch $(x - b)$ teilbar (d. h., bei der Polynomdivision von $f$ durch $(x - b)$ ist $r = 0$), wenn $f(b) = 0$ ist (d. h., $b$ ist **Nullstelle** von $f$).[^auswertung]

[^auswertung]: Mit $f(b)$ ist die **Auswertung** des Polynoms an der Stelle $b$ gemeint: Man kann für jedes $b \in K$ eine Abbildung $\varphi_b : K[x] \to K$ definieren, die ein Polynom $f(x) = \sum_{i=0}^{n} a_i x^i \in K[x]$ abbildet auf $f(b) := \sum_{i=0}^{n} a_i b^i$, also die Auswertung des Polynoms an der Stelle $b \in K$ berechnet. Man setzt also (wie man es für Polynome aus der Schule gewohnt ist) für die Variable $x$ das Element $b$ ein und berechnet dann den so entstehenden Ausdruck in $K$. Die Abbildung $\varphi_b$ wird als **Auswertungshomomorphismus** bezeichnet, siehe *Mathematik 3*.

> [!note]- Beweis
> **„$\Leftarrow$"** Sei $f$ durch $(x - b)$ teilbar, d. h., $f = q \cdot (x - b)$. Dann gilt
> $$f(b) = q(b) \cdot \underbrace{(b - b)}_{0} = 0,$$
> da in Ringen $y \cdot 0 = 0$ für alle Elemente $y$ des Rings gilt.
>
> **„$\Rightarrow$"** Sei $f(b) = 0$. Zu zeigen ist $(x - b) \mid f$, d. h., $r = 0$. Die Division mit Rest liefert $f = q \cdot (x - b) + r$ mit $\operatorname{grad}(r(x)) < \underbrace{\operatorname{grad}((x - b))}_{= 1}$. Daraus folgt, dass $r$ ein konstantes Polynom (dann wäre $\operatorname{grad}(r) = 0$) oder das Nullpolynom (dann wäre $\operatorname{grad}(r) = -\infty$) sein muss, also ein Element von $K$ ist. Wegen $0 = f(b) = q(b) \cdot \underbrace{(b - b)}_{0} + r = r$ folgt, dass $r = 0$ gilt. $\qquad \blacksquare$

## Beispiel 2.20

Bestimme die Nullstellen von $f(x) = x^3 - 6x^2 + 11x - 6 \in \mathbb{R}[x]$.

Wir können eine Nullstelle **erraten** (falls sie ganzzahlig ist, muss sie Teiler des konstanten Terms $-6$ sein, also $\pm 1, \pm 2, \pm 3, \pm 6$). Beispielsweise ist $x = 1$ Nullstelle, denn (durch Einsetzen in $f$ prüfen) $f(1) = 1 - 6 + 11 - 6 = 0$. Nach Korollar 2.19 muss der Linearfaktor $(x - 1)$ also $f$ teilen.

Polynomdivision ergibt $(x^3 - 6x^2 + 11x - 6) : (x - 1) = x^2 - 5x + 6$. Die Nullstellen dieses Polynoms zweiten Grades sind $x = 2$ und $x = 3$ (Mitternachtsformel).

## Weiter

- [[Der Körper der komplexen Zahlen]] — ein weiterer Körper, in dem jedes Polynom in Linearfaktoren zerfällt (Fundamentalsatz der Algebra)
