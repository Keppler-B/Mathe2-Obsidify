---
tags: [kapitel-4, thema, definition, beispiel]
quelle: Skript S. 65–68
aliases: [Elementare Zeilenumformungen, Zeilenstufenform, Erweiterte Koeffizientenmatrix, Führende Eins]
---
# Elementare Zeilenumformungen und Transformation in Zeilenstufenform

> Kapitel 4 · Matrizen und lineare Gleichungssysteme — drittes Thema. Zurück zum [[Inhaltsverzeichnis]].
> Voriges Thema: [[Lineare Gleichungssysteme]] · Nächstes Thema: [[Zeilen- und Spaltenrang]]
> Grundlage: [[Matrix]], [[Lineare Gleichungssysteme]].

## Bemerkung 4.8 (Erlaubte Operationen an einem LGS)

Die Lösungsmenge eines LGS ändert sich nicht, wenn wir

1. ein Vielfaches einer Gleichung zu einer anderen addieren,
2. eine Gleichung mit einem Skalar $\lambda \in K$ ($\lambda \neq 0$) multiplizieren,
3. zwei Gleichungen vertauschen.

Das liegt daran, dass die Lösungsmenge eines LGS einen (affinen) [[Untervektorräume|Unterraum]] bildet. Diese Operationen entsprechen Operationen an $A$ und $b$, siehe die folgende Definition 4.9. Aus dem LGS $Ax = b$ wird durch solche Operationen ein LGS $A'x = b'$ mit derselben Lösungsmenge.

Unser Ziel ist es nun, die Koeffizientenmatrix $A$ des LGS auf eine einfache Form $A'$ zu bringen, mittels derer sich alle [[Lineare Gleichungssysteme#Fragen 4.7|Fragen aus 4.7]] leicht beantworten lassen.

## Definition 4.9 (Elementare Zeilenumformungen)

Unter **elementaren Zeilenumformungen** einer Matrix versteht man die folgenden Operationen:

1. Addition des skalaren Vielfachen einer Zeile zu einer anderen,
2. Multiplikation einer Zeile mit einem Skalar $\lambda \neq 0$,
3. Vertauschen zweier Zeilen.

Analog lassen sich **elementare Spaltenumformungen** definieren. Diese brauchen wir (bis auf (3), Vertauschung zweier Spalten) für die Behandlung von LGS aber in der Regel nicht.

## Definition 4.10 (Erweiterte Koeffizientenmatrix)

Ist $Ax = b$ ein LGS und hängt man an die Matrix $A$ den Vektor $b$ als zusätzliche Spalte an (d. h.: ist $A \in M_{m,n}(K)$, dann ist $(A, b) \in M_{m,n+1}(K)$), so heißt $(A, b)$ die **erweiterte Koeffizientenmatrix**.

## Bemerkung 4.11 (Lösungen nach elementaren Zeilenumformungen)

Nach Bemerkung 4.8 gilt: Führt man an $(A, b)$ elementare Zeilenumformungen durch und erhält dadurch die Matrix $(A', b')$, so gilt:
Der Vektor $x \in K^n$ ist Lösung von $Ax = b$ **genau dann, wenn** $x \in K^n$ Lösung von $A'x = b'$ ist.

## Zeilenstufenform

Mittels des folgenden Algorithmus (der das Kernstück des Gaußschen Eliminationsverfahrens ist) lässt sich jede Matrix $A \in M_{m,n}(K)$ durch elementare Zeilenumformungen auf **Zeilenstufenform** bringen. Das bedeutet, dass die Matrix Nulleinträge enthält, die so angeordnet sind, dass eine Stufenform entsteht. An den mit $(\ast)$ gekennzeichneten Stellen können jeweils beliebige Einträge stehen; die „Stufen" können beliebige Länge $\geq 1$, müssen aber jeweils die Tiefe $1$ haben:

$$A = \begin{pmatrix} 1 & (\ast) & (\ast) & (\ast) & (\ast) & (\ast) & (\ast) & \cdots & & & & & (\ast) \\ 0 & 1 & (\ast) & (\ast) & (\ast) & (\ast) & (\ast) & \cdots & & & & & (\ast) \\ 0 & 0 & 0 & 1 & (\ast) & (\ast) & (\ast) & \cdots & & & & & (\ast) \\ 0 & 0 & 0 & 0 & 0 & 0 & 1 & (\ast) & \cdots & & & & (\ast) \\ \vdots & & & & \vdots & & & & \ddots & & & & \vdots \\ 0 & 0 & 0 & \cdots & & & & & 0 & 1 & (\ast) & \cdots & (\ast) \\ 0 & 0 & 0 & \cdots & & & & & \cdots & \cdots & 0 & 0 & 0 \\ 0 & 0 & 0 & \cdots & & & & & \cdots & \cdots & 0 & 0 & 0 \\ \vdots & & & & \vdots & & & & & & & & \vdots \\ 0 & 0 & 0 & \cdots & & & & & \cdots & \cdots & 0 & 0 & 0 \end{pmatrix}$$

Genauer gesagt muss für die durch elementare Zeilenumformungen aus $A$ entstandene Matrix gelten:

- In jeder Zeile ist der erste Eintrag, der von null verschieden ist, gleich $1$ (**„Führende Eins"**).
- Alle Einträge unter einer führenden Eins sind null.
- Die führende Eins einer Zeile liegt rechts von der führenden Eins der darüberliegenden Zeile.[^stufe]

Die Anzahl der „Stufen" (Anzahl der Zeilen, deren Einträge nicht alle null sind) bezeichnen wir mit der Zahl $r$.

[^stufe]: Genauer: der Spaltenindex der führenden Eins einer Zeile ist echt größer (muss aber nicht unbedingt nur um eins größer sein) als der Spaltenindex der führenden Eins der darüberliegenden Zeile.

## Algorithmus 4.12 (Transformation auf Zeilenstufenform)

1. Suche die erste Spalte, die nicht nur Nullen enthält, Spalte $j_1$.
2. Falls nötig, sorge durch Zeilenvertauschung dafür, dass das Element $a$ an Stelle $(1, j_1)$ ungleich $0$ ist.
3. Multipliziere die erste Zeile mit $a^{-1}$, der Eintrag an Stelle $(1, j_1)$ ist dann $1$.
4. Mache alle Einträge in Spalte $j_1$ außer dem in der ersten Zeile zu null: Addiere dazu jeweils ein geeignetes Vielfaches der ersten Zeile zu den übrigen Zeilen.

Ab jetzt wird die erste Zeile nicht mehr benutzt und bleibt unverändert.

5. Suche die erste Spalte $j_2\ (> j_1)$, die unterhalb der ersten Zeile einen Eintrag ungleich $0$ hat.
6. Mache den Eintrag an der Stelle $(2, j_2)$ wie in (2) und (3) zu $1$.
7. Mache alle Einträge in Spalte $j_2$ unterhalb der zweiten Zeile zu null wie in (4): Addiere dazu jeweils ein geeignetes Vielfaches der zweiten Zeile zu den übrigen Zeilen.

Ab jetzt wird die zweite Zeile nicht mehr benutzt und bleibt unverändert.
Fahre mit der dritten Zeile so fort, usw., solange möglich. Am Ende hat man die Zeilenstufenform erreicht!

## Beispiel 4.13

Wir wollen die Matrix $\begin{pmatrix} 0 & 0 & 2 & 1 \\ 0 & 2 & -4 & 6 \\ 0 & 2 & 2 & 0 \\ 0 & 0 & 6 & 3 \end{pmatrix} \in M_4(\mathbb{R})$ mittels Algorithmus 4.12 auf Zeilenstufenform bringen. Die Zeilen nummerieren wir hier mit römischen Ziffern I bis IV, das Vertauschen zweier Zeilen wird mittels „$\leftrightarrow$" gekennzeichnet.

$$\begin{pmatrix} 0 & 0 & 2 & 1 \\ 0 & 2 & -4 & 6 \\ 0 & 2 & 2 & 0 \\ 0 & 0 & 6 & 3 \end{pmatrix} \xrightarrow{(2):\ \mathrm{I} \leftrightarrow \mathrm{II}} \begin{pmatrix} 0 & 2 & -4 & 6 \\ 0 & 0 & 2 & 1 \\ 0 & 2 & 2 & 0 \\ 0 & 0 & 6 & 3 \end{pmatrix} \xrightarrow{(3):\ \mathrm{I} \cdot \frac{1}{2}} \begin{pmatrix} 0 & 1 & -2 & 3 \\ 0 & 0 & 2 & 1 \\ 0 & 2 & 2 & 0 \\ 0 & 0 & 6 & 3 \end{pmatrix}$$

*(Schritt (1): Pivotspalte $j_1$ ist die zweite Spalte.)*

$$\xrightarrow{(4):\ \mathrm{III}:\ \mathrm{I} + \mathrm{III} \cdot (-\frac{1}{2})} \begin{pmatrix} 0 & 1 & -2 & 3 \\ 0 & 0 & 2 & 1 \\ 0 & 0 & -3 & 3 \\ 0 & 0 & 6 & 3 \end{pmatrix} \xrightarrow{(6):\ \mathrm{II} \cdot \frac{1}{2}} \begin{pmatrix} 0 & 1 & -2 & 3 \\ 0 & 0 & 1 & \frac{1}{2} \\ 0 & 0 & -3 & 3 \\ 0 & 0 & 6 & 3 \end{pmatrix}$$

*(Schritt (4): Zeile II und Zeile IV bleiben unverändert, da sie in Spalte $j_1$ bereits eine Null besitzen. Schritt (5): Pivotspalte $j_2$ ist die dritte Spalte.)*

$$\xrightarrow{(7):\ \mathrm{III}:\ \mathrm{II} + \frac{1}{3} \cdot \mathrm{III}} \begin{pmatrix} 0 & 1 & -2 & 3 \\ 0 & 0 & 1 & \frac{1}{2} \\ 0 & 0 & 0 & \frac{3}{2} \\ 0 & 0 & 6 & 3 \end{pmatrix} \xrightarrow{(7):\ \mathrm{IV}:\ \mathrm{II} + (-\frac{1}{6}) \cdot \mathrm{IV}} \begin{pmatrix} 0 & 1 & -2 & 3 \\ 0 & 0 & 1 & \frac{1}{2} \\ 0 & 0 & 0 & \frac{3}{2} \\ 0 & 0 & 0 & 0 \end{pmatrix}$$

$$\xrightarrow{(9):\ \mathrm{III} \cdot \frac{2}{3}} \begin{pmatrix} 0 & 1 & -2 & 3 \\ 0 & 0 & 1 & \frac{1}{2} \\ 0 & 0 & 0 & 1 \\ 0 & 0 & 0 & 0 \end{pmatrix}$$

*(Schritt (8): Pivotspalte $j_3$ ist die vierte Spalte.)*

Der Algorithmus terminiert und wir erhalten eine Matrix in **Zeilenstufenform** mit drei Stufen, also $r = 3$.
