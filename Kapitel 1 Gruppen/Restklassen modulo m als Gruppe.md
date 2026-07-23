---
tags: [kapitel-1, thema, definition, satz]
quelle: Skript S. 10–16
aliases: [Restklassen, Zm, modulo]
---
# Restklassen modulo $m$ als Gruppe

> Kapitel 1 · Gruppen — zweites Beispiel endlicher Gruppen (aus der Zahlentheorie). Zurück zum [[Inhaltsverzeichnis]].
> Voriges Thema: [[Die symmetrische Gruppe Sn]] · Nächstes Thema: [[Untergruppen]]
> Grundlage: [[Gruppe]], [[Verknüpfung und Abgeschlossenheit]]. Wird verwendet in [[Ringe]] und [[Körper]].

Ein weiteres Beispiel endlicher Gruppen kommt aus der elementaren Zahlentheorie: die **Restklassen modulo** einer natürlichen Zahl $m$.

## Vorbemerkung 1.16 (Division mit Rest)

Aus der Schule ist die Division mit Rest bekannt, z. B. $25 : 7 = 3$ Rest $4$, was bedeutet, dass sich die Zahl $25$ als $25 = 3 \cdot 7 + 4$ darstellen lässt, wobei $0 \leq r < 7$ für den Rest $r$ (hier $r = 4$) gilt.

Allgemein kann man zeigen (etwa mit vollständiger Induktion): Zu gegebenem $n \in \mathbb{Z}$ und $m \in \mathbb{N}$ gibt es **eindeutig bestimmte** Zahlen $q \in \mathbb{Z}$ (**Quotient**) und $r \in \{0, 1, \dots, m-1\}$ (**Rest**) mit

$$n = q \cdot m + r.$$

## Definition 1.17 (Kongruenz modulo $m$)

Seien $n, q \in \mathbb{Z}$, $m \in \mathbb{N}$, $r \in \{0, 1, \dots, m-1\}$ wie in Vorbemerkung 1.16.

**(a)** Die Zahl $r$ heißt **Rest von $n$ modulo $m$**, kurz $n \bmod m$. Die Zahl $m$ heißt auch **Modul**.
**(b)** Im Falle $r = 0$ sagen wir auch: $n$ ist **durch $m$ teilbar** (oder *$m$ teilt $n$*), und schreiben $m \mid n$.
**(c)** Gilt für $n_1, n_2 \in \mathbb{Z}$
$$n_1 \bmod m = n_2 \bmod m$$
(d. h. bei Division durch $m$ lassen $n_1, n_2$ denselben Rest), so sagen wir *$n_1$ ist **kongruent** $n_2$ modulo $m$* und schreiben $n_1 \equiv n_2 \bmod m$ oder auch $n_1 \equiv n_2 \pmod{m}$.

## Beispiel 1.18

- $7 \bmod 3 = 1$, denn $7 = 2 \cdot 3 + 1$
- $37 \bmod 7 = 2$
- $42 \bmod 7 = 0$, d. h. $7 \mid 42$
- $-6 \bmod 5 = 4$, denn $-6 = (-2) \cdot 5 + 4$ (beachte, dass der Rest hier ein Element der Menge $\{0,1,2,3,4\}$ sein muss)
- $7 \equiv 1 \bmod 3$
- $37 \equiv 2 \bmod 7$
- $-13 \equiv 1 \bmod 7$

## Bemerkung 1.19

**(a)** $n_1 \equiv n_2 \bmod m$
$$\iff \exists\, q_1, q_2 \in \mathbb{Z},\, r \in \{0, \dots, m-1\} \text{ mit } n_1 = q_1 m + r,\; n_2 = q_2 m + r$$
$$\iff n_1 - n_2 = (q_1 - q_2) \cdot m, \text{ d. h. } m \text{ teilt } (n_1 - n_2).$$
Also: $n_1 \equiv n_2 \bmod m \iff (n_1 - n_2)$ ist durch $m$ teilbar. (Für $m = 2$: $n_1 \equiv n_2 \bmod 2$ genau dann, wenn $n_1, n_2$ beide gerade oder beide ungerade sind.)

**(b)** Ist ein Modul $m \in \mathbb{N}$ fest vorgegeben, so ist auf $\mathbb{Z}$ durch
$$n_1 \sim n_2 :\iff n_1 \equiv n_2 \bmod m$$
eine **[[Äquivalenzrelation]]** definiert. Die Zahlen $0, \dots, m-1$ bilden dafür ein **vollständiges Repräsentantensystem**.

## Definition 1.20 ($(\mathbb{Z}_m, \oplus, \odot)$)

Gegeben sei ein fester Modul $m \in \mathbb{N}$. Auf den Resten

$$\mathbb{Z}_m := \{0, 1, \dots, m-1\}$$

definieren wir Verknüpfungen $\oplus$ und $\odot$ wie folgt:

$$r_1 \oplus r_2 := (r_1 + r_2) \bmod m, \qquad r_1 \odot r_2 := (r_1 \cdot r_2) \bmod m$$

für $r_1, r_2 \in \mathbb{Z}_m$. Ist der Kontext klar, benutzt man auch $+$ und $\cdot$.

## Beispiel 1.21

**(a)** $\mathbb{Z}_5 = \{0,1,2,3,4\}$:
$$2 \oplus 0 = 2,\; 2 \oplus 1 = 3,\; 2 \oplus 2 = 4,\; 2 \oplus 3 = 0,\; 2 \oplus 4 = 1,$$
$$2 \odot 0 = 0,\; 2 \odot 1 = 2,\; 2 \odot 2 = 4,\; 2 \odot 3 = 1,\; 2 \odot 4 = 3.$$

Da es hier zwei verschiedene Verknüpfungen gibt, bezeichnen wir das **additiv Inverse** zu $x \in \mathbb{Z}_m$ mit $-x$, das **multiplikativ Inverse** wie bisher mit $x^{-1}$. Bezüglich $\oplus$ ist $0$ neutrales Element, und jedes Element in $\mathbb{Z}_5$ besitzt eine Inverse:
$$-0 = 0,\quad -1 = 4\; (1 \oplus 4 = 0),\quad -2 = 3,\quad -3 = 2,\quad -4 = 1.$$

> [!warning] Achtung Schreibweise
> $-1, -2, \dots$ bezeichnen hier **nicht** negative ganze Zahlen, sondern die Inversen: „$-1 = 4$" wird gelesen als „das inverse Element zu $1$ ist $4$". Wären negative ganze Zahlen gemeint, müsste man $\equiv$ verwenden, etwa $-1 \equiv 4 \pmod 5$.

Bezüglich $\odot$ ist $1$ neutrales Element, und jedes Element außer $0$ besitzt ein Inverses:
$$1^{-1} = 1,\quad 2^{-1} = 3\; (2 \odot 3 = 1),\quad 3^{-1} = 2,\quad 4^{-1} = 4\; (4 \odot 4 = 1).$$

**(b)** $\mathbb{Z}_4 = \{0,1,2,3\}$:
Inverse bezüglich $\oplus$: $\;-0 = 0,\, -1 = 3,\, -2 = 2,\, -3 = 1.$
Inverse bezüglich $\odot$: $\;1^{-1} = 1,\, 3^{-1} = 3.$
Das Element $2 \in \mathbb{Z}_4$ besitzt **keine** Inverse in $\mathbb{Z}_4$.

## Bemerkung 1.22 (mod als Zahl vs. Relation)

Beachte den Unterschied zwischen $a \bmod m$ und $a \equiv b \pmod m$:
- $a \bmod m$ ist eine **Zahl** aus $\{0, \dots, m-1\}$, nämlich das Bild von $a$ unter der Abbildung $\mathbb{Z} \to \{0,\dots,m-1\},\; a \mapsto a \bmod m$.
- $\equiv \pmod m$ ist eine **Äquivalenzrelation** auf $\mathbb{Z}$, d. h. eine Teilmenge von $\mathbb{Z} \times \mathbb{Z}$; $a \equiv b \pmod m$ entspricht einem Tupel $(a,b)$ dieser Teilmenge.

## Satz 1.23 (Rechenregeln für mod)

**(a)** Seien $a \equiv a' \bmod m$ und $b \equiv b' \bmod m$ mit $a, a', b, b' \in \mathbb{Z}$, $m \in \mathbb{N}$. Dann gilt
$$a + b \equiv (a' + b') \bmod m, \quad a - b \equiv (a' - b') \bmod m, \quad a \cdot b \equiv (a' \cdot b') \bmod m.$$

**(b)** Für $a, b \in \mathbb{Z}$, $m \in \mathbb{N}$ gilt
$$(a + b) \bmod m = ((a \bmod m) + (b \bmod m)) \bmod m,$$
$$(a - b) \bmod m = ((a \bmod m) - (b \bmod m)) \bmod m,$$
$$(a \cdot b) \bmod m = ((a \bmod m) \cdot (b \bmod m)) \bmod m.$$

> [!note]- Beweis
> **(a)** Nach Voraussetzung und Bemerkung 1.19(a) ist $(a - a')$ teilbar durch $m$ und $(b - b')$ teilbar durch $m$. Damit ist auch $(a - a') + (b - b') = (a + b) - (a' + b')$ teilbar durch $m$, was mittels Bem. 1.19(a) äquivalent ist zu $a + b \equiv (a' + b') \bmod m$. Die anderen Kongruenzen analog.
> **(b)** Aus $a = qm + r$ folgt $(a \bmod m) - a = r - (qm + r) = -qm$, also ist $((a \bmod m) - a)$ teilbar durch $m$, d. h. $a \bmod m \equiv a \pmod m$. Mit Teil (a) folgt die Behauptung. $\qquad \blacksquare$

Satz 1.23 besagt: **Gilt eine Gleichung mit $\cdot, +$ in $\mathbb{Z}$, dann auch in $\mathbb{Z}_m$ mit $\odot, \oplus$.**

> [!warning] Achtung
> Für die **Division** muss das nicht gelten!

## Beispiel 1.24 (Rechnen modulo $m$)

**(a)** Was ist $11 \cdot 12 \cdot 13 \bmod 7$?
- Produkt ausrechnen: $11 \cdot 12 \cdot 13 = 1716 \equiv 1 \bmod 7$.
- Teilweise & mit Satz 1.23: $11 \cdot 12 \cdot 13 \equiv 132 \cdot 13 \equiv (-1) \cdot (-1) \equiv 1 \bmod 7$.
- Jeden Faktor einzeln: $11 \cdot 12 \cdot 13 \equiv 4 \cdot 5 \cdot 6 \equiv 120 \equiv 1 \bmod 7$ oder $\equiv (-3)(-2)(-1) \equiv -6 \equiv 1 \bmod 7$.

**(b)** Welchen Rest lässt $2\,149\,342\,026$ bei Division durch $7$?
$$2149342026 = (2100000 + 4900 + 35 - 1)\ldots \equiv (-1) \equiv \ldots \equiv 1 \bmod 7,$$
also Rest $1$. *(Idee: $2149342026 = 210\,000 + 4900 + 35 - 1$ mit den ersten drei Summanden durch $7$ teilbar; vgl. PDF S. 14.)*

## Definition 1.25 (ggT, teilerfremd)

Seien $a_1, \dots, a_n \in \mathbb{Z}$.
**(a)** Ist mindestens ein $a_i \neq 0$, so ist der **größte gemeinsame Teiler** $\gcd(a_1, \dots, a_n)$ die größte natürliche Zahl, die alle $a_1, \dots, a_n$ teilt.
**(b)** Ist $\gcd(a_1, \dots, a_n) = 1$, so heißen $a_1, \dots, a_n$ **teilerfremd**. (Beispiel: $\gcd(20, 24) = 4$, $\gcd(20, 21) = 1$.)

## Bemerkung 1.26 (Erweiterter Euklidischer Algorithmus, EEA)

Der ggT zweier Zahlen ist mittels des **Erweiterten Euklidischen Algorithmus (EEA)** berechenbar (kommt in *Mathematik 3*). Er liefert zu $a, b \in \mathbb{Z}$ ganze Zahlen $s, t$ mit
$$\gcd(a, b) = s \cdot a + t \cdot b.$$
(Beispiel: $\gcd(20, 24) = 4 = (-1) \cdot 20 + 1 \cdot 24$, also $s = -1$, $t = 1$.)

## Satz 1.27 (Restklassengruppe)

Sei $m \in \mathbb{N}$.
**(a)** $(\mathbb{Z}_m, \oplus)$ ist eine **abelsche Gruppe**.
**(b)** $(\mathbb{Z}_m, \odot)$ ist im Allgemeinen **keine** Gruppe.

> [!note]- Beweis
> **(a)**
> - Abgeschlossenheit gilt nach Definition von $\oplus$: für $a, b \in \{0,\dots,m-1\}$ ist auch $a \oplus b \in \{0,\dots,m-1\}$.
> - Assoziativ- und Kommutativgesetz gelten nach Satz 1.23, da sie in $\mathbb{Z}$ gelten.
> - Neutrales Element ist $0$: $a \oplus 0 = (a + 0) \bmod m = a$.
> - Inverse zu $a \in \mathbb{Z}_m$ ist $\;-a = \begin{cases} 0, & a = 0 \\ m - a, & a \neq 0, \end{cases}$ denn $a \oplus (m - a) = (a + (m-a)) \bmod m = m \bmod m = 0$. (Inverse zu $a$ ist die Zahl, die addiert zu $a$ den Modul $m$ ergibt.)
>
> **(b)** Abgeschlossenheit, Assoziativität, Kommutativität wie in (a); neutrales Element ist $1$. **Aber:** Das Element $0$ besitzt keine Inverse (es gäbe kein $a$ mit $0 \odot a = 1$), also ist $(\mathbb{Z}_m, \odot)$ keine Gruppe.
> Welche Elemente sind bezüglich $\odot$ invertierbar?
> $$x \text{ invertierbar} \iff \exists y \in \mathbb{Z}_m:\, x \odot y = 1 \iff \exists y, q \in \mathbb{Z}:\, xy + (-q)m = 1 \underset{\text{Bem.1.26}}{\iff} \gcd(x, m) = 1.$$
> Also: **Nur die zu $m$ teilerfremden Elemente in $\mathbb{Z}_m$ sind bezüglich $\odot$ invertierbar.** $\qquad \blacksquare$

## Definition/Bemerkung 1.28 ($\mathbb{Z}_m^*$, Eulersche $\varphi$-Funktion)

Die Menge

$$\mathbb{Z}_m^* := \{x \in \mathbb{Z}_m \mid \gcd(x, m) = 1\}$$

ist eine **Gruppe bezüglich $\odot$** (man nimmt nur die invertierbaren, d. h. zu $m$ teilerfremden Elemente auf). Weiter definieren wir die **Eulersche $\varphi$-Funktion**

$$\varphi : \mathbb{N} \to \mathbb{N}, \qquad m \mapsto \varphi(m) := |\mathbb{Z}_m^*|.$$

$\varphi(m)$ ist die Anzahl der zu $m$ teilerfremden Zahlen zwischen $1$ und $m$. Beispiele:

$$\mathbb{Z}_3^* = \{1,2\},\, \varphi(3) = 2; \quad \mathbb{Z}_4^* = \{1,3\},\, \varphi(4) = 2; \quad \mathbb{Z}_8^* = \{1,3,5,7\},\, \varphi(8) = 4;$$
$$\mathbb{Z}_p^* = \{1, 2, \dots, p-1\},\, \varphi(p) = p - 1 \text{ (falls $p$ Primzahl)}.$$
