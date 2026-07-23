---
tags: [kapitel-2, thema, definition, satz, kernbegriff]
quelle: Skript S. 24
aliases: [Koerper, Field]
---
# Körper

> Kapitel 2 · Ringe und Körper — spezielle kommutative Ringe mit Eins. Zurück zum [[Inhaltsverzeichnis]].
> Voriges Thema: [[Ringe]] · Nächstes Thema: [[Polynomringe]]
> Grundlage: [[Ring]], [[Gruppe]]. Wird verwendet in [[Polynomringe]], [[Der Körper der komplexen Zahlen]] und [[Vektorraum]].

Wir beschäftigen uns nun mit einer speziellen Klasse von kommutativen Ringen mit Eins, den sogenannten **Körpern**.

## Definition 2.5 (Körper)

Ein kommutativer [[Ring]] $(K, +, \cdot)$ mit Eins heißt **Körper**, wenn jedes Element $0 \neq x \in K$ eine **Einheit** ist, d. h., wenn $K^* = K \setminus \{0\}$ gilt.

> [!tip] Merkhilfe
> Körper $=$ kommutativer Ring mit Eins, in dem *jedes* Element außer $0$ ein multiplikativ Inverses besitzt. $(K \setminus \{0\}, \cdot)$ ist dann eine abelsche Gruppe.

## Beispiel 2.6

**(a)** $(\mathbb{Q}, +, \cdot)$ und $(\mathbb{R}, +, \cdot)$ sind Körper, $(\mathbb{Z}, +, \cdot)$ ist **kein** Körper.

**(b)** Wie wir in [[Restklassen modulo m als Gruppe|1.28]] gesehen hatten, ist $\mathbb{Z}_m^* = \{x \in \mathbb{Z}_m \mid \gcd(x, m) = 1\}$, die Menge der Einheiten in $\mathbb{Z}_m$, eine Gruppe bezüglich $\odot$. Wir hatten auch gesehen, dass genau dann alle Elemente von $\mathbb{Z}_m$ bis auf die $0$ in $\mathbb{Z}_m^*$ liegen, also bezüglich $\cdot$ invertierbar sind, wenn $m$ eine Primzahl ist. Daraus folgt:
$$(\mathbb{Z}_m, \oplus, \odot) \text{ ist genau dann ein Körper, wenn } m \text{ eine Primzahl ist.}$$

## Satz 2.7 (Rechnen in Körpern, Nullteilerfreiheit)

Eine wichtige Eigenschaft von Körpern ist die **Nullteilerfreiheit**, die im folgenden Satz beschrieben wird.

Sei $(K, +, \cdot)$ ein Körper, $a, b \in K$. Dann gilt
$$a \cdot b = 0 \iff a = 0 \text{ oder } b = 0.$$

Wir kennen diese Eigenschaft vom Rechnen mit reellen Zahlen (auch bekannt als **Satz vom Nullprodukt**, der zum Lösen von Gleichungen benutzt wird, z. B. bei $x \cdot (x - 1) = 0$): wenn das Produkt zweier reeller Zahlen $0$ ergibt, muss mindestens einer der Faktoren $0$ sein.

Diese Eigenschaft ist in manchen der bisher betrachteten Strukturen **nicht** erfüllt, z. B. in $(\mathbb{Z}_6, \oplus, \odot)$: Hier gilt $2 \odot 3 = 0$, aber weder $2 = 0$ noch $3 = 0$ in $\mathbb{Z}_6$. (Die Elemente $2, 3 \in \mathbb{Z}_6$ werden als **Nullteiler** bezeichnet.[^nullteiler] $(\mathbb{Z}_6, \oplus, \odot)$ ist also nicht nullteilerfrei.)

[^nullteiler]: Allgemein: Ein **Nullteiler** in einem Ring $(R, +, \cdot)$ ist ein Element $0 \neq a \in R$, für das ein Element $0 \neq b \in R$ existiert mit $a \cdot b = 0$.

> [!note]- Beweis
> **„$\Leftarrow$"** Nach den Rechenregeln in Ringen ([[Ringe|Satz 2.3(a)]]) ist das Produkt eines Ringelements mit $0$ wieder $0$.
>
> **„$\Rightarrow$"** Sei $a \cdot b = 0$. Wir zeigen: Falls $a \neq 0$ ist, muss $b = 0$ sein. Angenommen, $a \neq 0$. Da $K$ ein Körper ist, bedeutet das, dass $a$ eine Inverse $a^{-1}$ besitzt. Damit ist
> $$b = 1 \cdot b = (a^{-1} \cdot a) \cdot b = a^{-1} \cdot (\underbrace{a \cdot b}_{=0}) \overset{2.3(a)}{=} 0. \qquad \blacksquare$$

## Weiter

- [[Polynomringe]] — der Polynomring $K[x]$ über einem Körper $K$
- [[Der Körper der komplexen Zahlen]] — $\mathbb{C}$ als weiteres Beispiel eines Körpers
- [[Vektorraum]] — Vektorräume werden über einem Körper $K$ definiert
