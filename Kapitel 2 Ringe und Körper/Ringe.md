---
tags: [kapitel-2, thema, satz, beispiel]
quelle: Skript S. 21–23
aliases: [Ring (Thema)]
---
# Ringe

> Kapitel 2 · Ringe und Körper — erste algebraische Struktur mit **zwei** Verknüpfungen (Addition und Multiplikation), die durch das Distributivgesetz in Beziehung stehen. Zurück zum [[Inhaltsverzeichnis]].
> Voriges Kapitel: [[Restklassen modulo m als Gruppe]] · Nächstes Thema: [[Körper]]
> Grundlage: [[Gruppe]], [[Verknüpfung und Abgeschlossenheit]]. Atomare Definition: [[Ring]].

In diesem Kapitel beschäftigen wir uns mit **Ringen** und **Körpern**, algebraischen Strukturen mit *zwei* Verknüpfungen (Addition und Multiplikation), die durch das *Distributivgesetz* in Beziehung stehen.

Die grundlegende Definition liegt in der atomaren Notiz [[Ring]] und ist hier eingebettet:

![[Ring#Definition 2.1 (Ring)]]

## Beispiel 2.2

**(a)** $(\mathbb{Z}, +, \cdot)$ (die Menge der ganzen Zahlen mit bekannter Addition und Multiplikation) ist ein **kommutativer Ring mit Eins**; die Eins ist die Zahl $1$. Die Menge der Einheiten ist $\mathbb{Z}^* = \{1, -1\}$.
Ebenso sind $(\mathbb{Q}, +, \cdot)$ und $(\mathbb{R}, +, \cdot)$ Ringe mit Eins. Die Einheiten sind $\mathbb{Q}^* = \mathbb{Q} \setminus \{0\}$ bzw. $\mathbb{R}^* = \mathbb{R} \setminus \{0\}$.

**(b)** $(2\mathbb{Z}, +, \cdot)$ ist ein **kommutativer Ring ohne Eins** (da die Zahl $1$ nicht gerade und damit kein Element von $2\mathbb{Z}$ ist).

**(c)** $(\{0\}, +, \cdot)$ ist der **triviale Ring**, ein Ring ohne Eins (die Zahl $0$, das einzige Element dieses Rings, ist bezüglich $\cdot$ zwar auch neutral, aber in [[Ring|Definition 2.1(c)]] war $1 \neq 0$ gefordert).

**(d)** Für $m \in \mathbb{N}$, $m \geq 2$ ist $(\mathbb{Z}_m, \oplus, \odot)$ ein **kommutativer Ring mit Eins**.
Die geforderten Eigenschaften haben wir bereits in [[Restklassen modulo m als Gruppe|Kapitel 1]] geprüft, neu sind nur die Distributivgesetze, die aus [[Restklassen modulo m als Gruppe|Satz 1.23]] (Rechenregeln für modulo) folgen.

**(e)** $(\mathbb{R}^n, +, \cdot)$, die Menge aller Vektoren mit $n$ reellen Einträgen, wobei Addition und Multiplikation komponentenweise definiert werden, ist ein kommutativer Ring mit Eins.
Allgemein gilt: Sind $R_1, \dots, R_n$ Ringe mit den Verknüpfungen $+$ und $\cdot$, dann ist auch $R_1 \times \cdots \times R_n$ ein Ring (mit komponentenweise gebildeten Verknüpfungen $+$ und $\cdot$).

## Satz 2.3 (Rechnen in Ringen)

Der folgende Satz liefert Rechenregeln für die Multiplikation mit dem neutralen Element und von additiv Inversen in Ringen.

Sei $(R, +, \cdot)$ ein Ring, $a, b \in R$. Dann gilt

**(a)** $a \cdot 0 = 0 \cdot a = 0$
**(b)** $(-a) \cdot b = a \cdot (-b) = -(a \cdot b)$
**(c)** $(-a) \cdot (-b) = a \cdot b$

> [!note]- Beweis
> **(a)** Es gilt
> $$a \cdot 0 = a \cdot (0 + 0) \overset{2.1(3)}{=} a \cdot 0 + a \cdot 0.$$
> Addition von $-(a \cdot 0)$ (dem Inversen von $a \cdot 0$) auf beiden Seiten ergibt $0 = a \cdot 0$. Analog erhält man $0 \cdot a = 0$.
>
> **(b)** Es gilt
> $$(-a) \cdot b + a \cdot b \overset{2.1(3)}{=} (-a + a) \cdot b = 0 \cdot b \overset{\text{Teil (a)}}{=} 0,$$
> also ist $(-a) \cdot b$ Inverses zu $a \cdot b$ (d. h. $-(a \cdot b)$), also
> $$(-a) \cdot b = -(a \cdot b).$$
> Analog zeigt man $a \cdot (-b) = -(a \cdot b)$.
>
> **(c)**
> $$(-a) \cdot (-b) \overset{\text{Teil (b)}}{=} -(a \cdot (-b)) \overset{\text{Teil (b)}}{=} -(-(a \cdot b)) = a \cdot b.$$
> Die letzte Gleichheit gilt aus folgendem Grund: $-(-(a \cdot b))$ ist Inverse zu $-(a \cdot b)$. Andererseits ist aber bereits $a \cdot b$ Inverse zu $-(a \cdot b)$. Da das inverse Element eindeutig ist ([[Eigenschaften und Rechenregeln|Satz 1.5(b)]] über Eigenschaften von Gruppen), muss also $-(-(a \cdot b)) = a \cdot b$ gelten. $\qquad \blacksquare$

## Bemerkung 2.4

**(a)** In jedem Ring mit Eins sind $1$ und $-1$ (additiv Inverses von $1$) Einheiten, denn $(-1) \cdot (-1) = 1$ nach 2.3(c), d. h., $-1$ ist seine eigene Inverse (**selbstinvers**).
Es kann noch mehr Einheiten geben (siehe $\mathbb{Z}_3, \mathbb{Z}_5, \dots$), es kann auch $1 = -1$ gelten (das ist der Fall in $(\mathbb{Z}_2, \oplus, \odot)$, hier ist $1 \oplus 1 = 0$, $1 \odot 1 = 1$).

**(b)** Das Element $0$ kann nach Satz 2.3(a) **nie Einheit** sein (da $1 \neq 0$ laut [[Ring|Definition 2.1]]).

**(c)** In einem kommutativen Ring $R$ gilt der **Binomialsatz** (vgl. *Mathematik 1*, Beweis mittels vollständiger Induktion und der rekursiven Beschreibung von $\binom{n}{k}$):
$$(a + b)^n = \sum_{k=0}^{n} \binom{n}{k} a^k \cdot b^{n-k}$$
mit $n \in \mathbb{N}$, $a, b \in R$, wobei
$$a^0 b^n = b^n, \qquad a^n b^0 = a^n,$$
$$a^k = \underbrace{a \cdot \ldots \cdot a}_{k \text{ Faktoren}},$$
$$\binom{n}{k} a^k \cdot b^{n-k} = \underbrace{a^k \cdot b^{n-k} + \cdots + a^k \cdot b^{n-k}}_{\binom{n}{k} \text{ Summanden}}.$$

> [!info]
> Wir brauchen diese Beschreibung, da nicht gefordert wurde, dass es in $R$ eine Eins gibt.

Die Binomialkoeffizienten lassen sich einfach mittels des **Pascalschen Dreiecks** berechnen, siehe *Mathematik 1*. Achtung, die dabei entstehenden Zahlen müssen richtig im Ring interpretiert werden, z. B. ist $(a + b)^2 = a^2 + 2ab + b^2$ gleich $a^2 + b^2$ in $\mathbb{Z}_2$, da $2ab = ab + ab = 0$ in $\mathbb{Z}_2$.

## Weiter

- [[Körper]] — spezielle kommutative Ringe mit Eins, in denen jedes Element $\neq 0$ invertierbar ist
- [[Polynomringe]] — der Ring $K[x]$ der Polynome über einem Körper $K$
