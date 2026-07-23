---
tags: [kapitel-4, thema, definition, satz]
quelle: Skript S. 62–64
aliases: [LGS, Lineares Gleichungssystem, Lösungsraum, homogen, inhomogen]
---
# Lineare Gleichungssysteme

> Kapitel 4 · Matrizen und lineare Gleichungssysteme — zweites Thema. Zurück zum [[Inhaltsverzeichnis]].
> Voriges Thema: [[Matrizen und Operationen mit Matrizen]] · Nächstes Thema: [[Elementare Zeilenumformungen und Transformation in Zeilenstufenform]]
> Grundlage: [[Matrix]], [[Körper]], [[Vektorraum]], [[Untervektorräume]].

Ein *Gleichungssystem* ist eine Menge von Gleichungen mit einer oder mehreren Unbekannten, die alle gleichzeitig erfüllt sein sollen. Wir betrachten hier **lineare Gleichungssysteme**, was bedeutet, dass die Gleichungen nur Linearkombinationen der Unbekannten enthalten dürfen (die Unbekannten kommen also nur in der ersten Potenz vor) und befassen uns näher mit der Struktur der Lösungen dieser Systeme.

## Definition 4.4 (Lineares Gleichungssystem)

**(a)** Ein **lineares Gleichungssystem (LGS)** über einem [[Körper]] $K$ hat die Form

$$\left. \begin{aligned} a_{11} x_1 + a_{12} x_2 + \cdots + a_{1n} x_n &= b_1 \\ a_{21} x_1 + a_{22} x_2 + \cdots + a_{2n} x_n &= b_2 \\ &\ \,\vdots \\ a_{m1} x_1 + a_{m2} x_2 + \cdots + a_{mn} x_n &= b_m \end{aligned} \right\} \quad (\star),$$

es besteht also aus $m$ Gleichungen, $n$ Unbekannten $x_1, \dots, x_n$, Koeffizienten $a_{ij} \in K$ und Elementen $b_1, \dots, b_m \in K$.
Der Vektor $\begin{pmatrix} x_1 \\ \vdots \\ x_n \end{pmatrix}$ heißt **Lösung** des LGS, wenn die $x_1, \dots, x_n$ sämtliche Gleichungen erfüllen.

**(b)** Ein LGS heißt **homogen**, falls $b_1 = \cdots = b_m = 0$, ansonsten heißt es **inhomogen**.

**(c)** Setzt man $A = \begin{pmatrix} a_{11} & \cdots & a_{1n} \\ \vdots & \ddots & \vdots \\ a_{m1} & \cdots & a_{mn} \end{pmatrix} \in M_{m,n}(K)$, die sogenannte **Koeffizientenmatrix**, und $b = \begin{pmatrix} b_1 \\ \vdots \\ b_m \end{pmatrix} \in K^m$, so lässt sich $(\star)$ in **Matrixform** schreiben als

$$Ax = b.$$

**(d)** Sind $s_1, \dots, s_n$ die Spalten von $A$, so lässt sich $(\star)$ in **Spaltenform** schreiben als

$$x_1 s_1 + \cdots + x_n s_n = b.$$

> [!info] Beachte (Null-Lösung)
> Ein homogenes LGS hat *immer* mindestens eine Lösung, nämlich $\mathcal{O} = \begin{pmatrix} 0 \\ \vdots \\ 0 \end{pmatrix}$, die **Null-Lösung** (triviale Lösung).

## Bemerkung 4.5 (LGS als Abbildung)

Aus Definition 4.4(c) ergibt sich, dass

$$\varphi_A : K^n \to K^m, \qquad x \mapsto Ax$$

für $A \in M_{m,n}(K)$, $x \in K^n$ eine **Abbildung** ist, die Vektoren aus $K^n$ auf Vektoren aus $K^m$ abbildet.[^folien]

> [!info] Lineare Abbildung
> Genauer gesagt, handelt es sich um eine sogenannte **lineare Abbildung** $\varphi : K^n \to K^m$, die durch folgende Eigenschaften charakterisiert ist:
> $$\varphi(v_1 + v_2) = \varphi(v_1) + \varphi(v_2) \quad \text{für alle } v_1, v_2 \in K^n,$$
> $$\varphi(\lambda v) = \lambda \varphi(v) \quad \text{für alle } v \in K^n,\ \lambda \in K.$$
> Wie wir später sehen werden, kann jede Matrix als lineare Abbildung aufgefasst werden, und alle linearen Abbildungen $\varphi : K^n \to K^m$ lassen sich als Multiplikation mit einer passenden Matrix darstellen. (Siehe [[Lineare Abbildungen (Kapitel 8)|Lineare Abbildungen]].)

[^folien]: Überlegungen und Beispiele dazu sind auf den Vorlesungsfolien vom 15.06.2026 und auf Präsenzblatt 9 zu finden.

## Satz 4.6 (Lösungsraum eines LGS)

**(a)** Die Menge der Lösungen des homogenen LGS

$$Ax = \mathcal{O}$$

bildet einen [[Untervektorräume|Unterraum]] von $K^n$.

**(b)** Ist das inhomogene LGS

$$Ax = b$$

lösbar und $x_0$ irgendeine spezielle Lösung, so erhält man alle Lösungen

$$\{x \in K^n \mid Ax = b\}$$

durch

$$\{x_0 + y \mid Ay = \mathcal{O}\}.$$

Ist also $U$ der Lösungsraum des zugehörigen homogenen LGS $Ax = \mathcal{O}$, so ist die Lösungsmenge von $Ax = b$ von der Form $x_0 + U$ (das nennt man einen **affinen Unterraum**, d. h. ein Unterraum verschoben um $x_0$).

> [!note]- Beweis
> **(a)** Wir weisen die Eigenschaften aus dem Unterraum-Kriterium (3.7) nach:
> 1. $\mathcal{O}$ ist eine Lösung (siehe Bemerkung am Ende von Definition 4.4).
> 2. Sind $x, y$ Lösungen des homogenen LGS, dann muss für sie $Ax = \mathcal{O}$, $Ay = \mathcal{O}$ gelten. Damit gilt aber auch $\mathcal{O} = Ax + Ay \overset{4.3(c)}{=} A(x + y)$, d. h. $x + y$ ist auch eine Lösung des homogenen LGS.
> 3. Ist $x$ eine Lösung des homogenen LGS, d. h. $Ax = \mathcal{O}$, dann gilt auch $\mathcal{O} = \lambda \mathcal{O} = \lambda(Ax) \overset{4.3(d)}{=} A(\lambda x)$, d. h. $\lambda x$ ist eine Lösung des homogenen LGS.
>
> **(b)** Sei $Ax_0 = b$.
> - Ist $Ay = \mathcal{O}$, dann ist $A(x_0 + y) \overset{4.3(c)}{=} \underbrace{Ax_0}_{b} + \underbrace{Ay}_{\mathcal{O}} = b$, was bedeutet, dass $x_0 + y$ das LGS $Ax = b$ löst.
> - Umgekehrt: Falls $Ax = b$ gilt, dann ist $\underbrace{Ax}_{b} - \underbrace{Ax_0}_{b} = A\underbrace{(x - x_0)}_{\in U} = \mathcal{O}$. Wegen $x = x_0 + \underbrace{(x - x_0)}_{\in U}$ ist $x \in x_0 + U$. $\qquad \blacksquare$

Wir wissen jetzt, dass die Lösungen des homogenen LGS $Ax = \mathcal{O}$ einen Unterraum bilden. Damit ist der Nullvektor $\mathcal{O}$ immer eine Lösung, und sobald es noch weitere Lösungen des LGS gibt, müssen auch alle skalaren Vielfache und alle Summen (also alle Linearkombinationen) davon das LGS lösen. Kann man noch mehr über Eindeutigkeit und Anzahl der Lösungen aussagen?

## Fragen 4.7

- Wann hat $Ax = b$ (mindestens) eine Lösung?
- Wann hat $Ax = b$ *genau eine* Lösung?
- Wie groß ist die Dimension des Lösungsraums von $Ax = \mathcal{O}$?
- Wenn $Ax = b$ eine Lösung besitzt, wie bestimmt man *alle* Lösungen?

Wie wir sehen werden, lassen sich diese Fragen mittels des sogenannten **Gaußschen Eliminationsverfahrens** (siehe [[Gaußsches Eliminationsverfahren zur Bestimmung der Lösung eines LGS|Algorithmus 4.20]]) beantworten. Dazu brauchen wir noch mehrere Bemerkungen und Definitionen (siehe [[Elementare Zeilenumformungen und Transformation in Zeilenstufenform]] und [[Zeilen- und Spaltenrang]]).
