---
tags: [kapitel-1, definition, kernbegriff]
quelle: Skript S. 3–5
---
# Gruppe

> Namensgebende Struktur von Kapitel 1. Baut auf [[Verknüpfung und Abgeschlossenheit]] auf und wird von vielen Themen verwendet.
> Zurück: [[Verknüpfungen, Gruppen, erste Beispiele]] · [[Inhaltsverzeichnis]]

## Definition 1.3 (Gruppe)

**(a)** Eine **Gruppe** ist ein Paar $(G, \ast)$ bestehend aus einer nichtleeren Menge $G$ und einer Verknüpfung $\ast : G \times G \to G$ (beachte, dass $\ast$ nach $G$ abbildet, die Menge $G$ also bezüglich $\ast$ [[Verknüpfung und Abgeschlossenheit|abgeschlossen]] ist!), das folgende Eigenschaften (die sogenannten **Gruppenaxiome**) erfüllt:

1. Es gilt $(a \ast b) \ast c = a \ast (b \ast c)$ für alle $a, b, c \in G$ &nbsp;(**Assoziativgesetz**).
2. Es existiert ein Element $e \in G$ mit $a \ast e = e \ast a = a$ für alle $a \in G$ &nbsp;(**Neutrales Element**).
3. Für alle $a \in G$ existiert $a^{-1} \in G$ mit $a \ast a^{-1} = a^{-1} \ast a = e$ &nbsp;(**Inverses Element** oder **Inverse**; das Element $a$ heißt dann **invertierbar**).

**(b)** Gilt zusätzlich

4. $a \ast b = b \ast a$ für alle $a, b \in G$ &nbsp;(**Kommutativgesetz**),

so heißt $G$ **kommutative** oder **abelsche** Gruppe.

**(c)** Ist $G$ eine endliche Menge, so bezeichnet man die Anzahl der Elemente von $G$ als **Ordnung** von $G$, in Zeichen: $|G|$.

**(d)** Das Paar $(G, \ast)$ heißt **Halbgruppe**, falls das Axiom (1) erfüllt ist.

> [!tip] Merkhilfe
> Gruppe $=$ abgeschlossene Verknüpfung $+$ **A**ssoziativität $+$ **N**eutrales $+$ **I**nverse. Zusätzlich kommutativ $\Rightarrow$ *abelsch*. Nur Assoziativität $\Rightarrow$ *Halbgruppe*.

## Beispiel 1.4

**(a)** $(G = \{1\}, \cdot)$ ist eine abelsche Gruppe:
- Offensichtlich ist $G$ abgeschlossen bezüglich der Multiplikation, denn $1 \cdot 1 = 1 \in G$.
- Assoziativgesetz und Kommutativgesetz gelten bekanntlich für die Multiplikation reeller Zahlen.
- Das neutrale Element ist $e = 1$ (es gilt $e \cdot 1 = 1 \cdot 1 = 1 \cdot e = 1$).
- Die Inverse von $1$ (das einzige Element in $G$) ist die Zahl $1$ selbst: $1^{-1} = 1$, denn $1 \cdot 1^{-1} = 1 \cdot 1 = 1^{-1} \cdot 1 = e$.

**(b)** $(\mathbb{Z}, +)$ ist eine abelsche Gruppe:
- $\mathbb{Z}$ ist abgeschlossen bezüglich der Addition.
- Assoziativgesetz und Kommutativgesetz gelten bekanntlich für die Addition ganzer Zahlen.
- Das neutrale Element ist $e = 0$, denn $a + 0 = 0 + a$ für alle $a \in \mathbb{Z}$.
- Die Inverse zu $a \in \mathbb{Z}$ ist $-a \in \mathbb{Z}$.

**(c)** Ebenso sind $(\mathbb{Q}, +)$ und $(\mathbb{R}, +)$ abelsche Gruppen.

**(d)** $(\mathbb{Z}, \cdot)$ ist hingegen **keine** Gruppe: Die Zahl $e = 1$ ist zwar neutrales Element ($1 \cdot a = a \cdot 1 = a$ für alle $a \in \mathbb{Z}$), aber es gibt im Allgemeinen keine Inversen (außer zu den Zahlen $1$ und $-1$). Es handelt sich bei diesem Paar aber um eine kommutative **Halbgruppe** (die zusätzlich das Gruppenaxiom (2) erfüllt).

**(e)** $G = 2\mathbb{Z} := \{2k \mid k \in \mathbb{Z}\}$, die Menge der geraden Zahlen, ist zusammen mit der üblichen Addition $+$ eine abelsche Gruppe, zusammen mit der üblichen Multiplikation $\cdot$ eine kommutative Halbgruppe.

**(f)** $H = 2\mathbb{Z} + 1 := \{2k + 1 \mid k \in \mathbb{Z}\}$, die Menge der ungeraden Zahlen, bildet mit der Addition **keine** Gruppe ($H$ ist nicht abgeschlossen bezüglich $+$, die Summe zweier ungerader Zahlen ergibt eine gerade Zahl). Mit der Multiplikation als Verknüpfung ist $H$ eine kommutative Halbgruppe.

*Weitere Beispiele für (endliche) Gruppen folgen: [[Die symmetrische Gruppe Sn]] und [[Restklassen modulo m als Gruppe]].*

## Verwendet in

- [[Eigenschaften und Rechenregeln]] — Sätze über Gruppen
- [[Die symmetrische Gruppe Sn]], [[Restklassen modulo m als Gruppe]], [[Untergruppen]]
- [[Ring]], [[Körper]], [[Vektorraum]] (jeweils als additive Gruppe)
