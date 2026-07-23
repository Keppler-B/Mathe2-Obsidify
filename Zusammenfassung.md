# Zusammenfassung — Lineare Algebra (Mathematik für Informatik 2)

> Der rote Faden durchs ganze Skript in verständlicher Sprache. Jeder Begriff verlinkt auf die ausführliche Themendatei.
> Navigation: [[Inhaltsverzeichnis]] · [[Formelsammlung]] · [[Checklist]] · [[Übersicht|Grundlagen]]

Die Vorlesung baut **eine Struktur nach der anderen** auf: von einer Menge mit *einer* Verknüpfung ([[Gruppe]]) über *zwei* Verknüpfungen ([[Ring]], [[Körper]]) hin zum zentralen Objekt der linearen Algebra, dem [[Vektorraum]]. Darauf folgen die Rechenwerkzeuge ([[Matrix|Matrizen]], LGS, [[Determinante|Determinanten]]) und schließlich die strukturerhaltenden Abbildungen ([[Lineare Abbildung|lineare Abbildungen]]). Ein roter Faden: **immer** wird gefragt, welche Rechenregeln gelten und wann Objekte *invertierbar* sind.

---

## 1 Gruppen — eine Menge mit einer Verknüpfung

Eine [[Gruppe]] ist eine Menge mit einer [[Verknüpfung und Abgeschlossenheit|abgeschlossenen Verknüpfung]], die **assoziativ** ist, ein **neutrales Element** besitzt und zu jedem Element ein **Inverses**. Kommt Kommutativität hinzu, heißt sie *abelsch*. Aus den Axiomen folgen schon starke Aussagen ([[Eigenschaften und Rechenregeln]]): neutrales Element und Inverse sind **eindeutig**, und Gleichungen $ax = b$ sind eindeutig lösbar.

Zwei wichtige Beispielfamilien:
- **[[Die symmetrische Gruppe Sn]]** $S_n$: alle Permutationen von $\{1,\dots,n\}$ mit der Komposition $\circ$. Sie hat $n!$ Elemente und ist für $n \geq 3$ nicht abelsch — das erste „handfeste" nicht-kommutative Beispiel.
- **[[Restklassen modulo m als Gruppe]]** $\mathbb{Z}_m$: Rechnen mit Resten. $(\mathbb{Z}_m, \oplus)$ ist immer eine abelsche Gruppe; bezüglich $\odot$ sind genau die zu $m$ **teilerfremden** Elemente invertierbar ($\mathbb{Z}_m^*$).

[[Untergruppen]] sind Teilmengen, die selbst wieder Gruppe sind — prüfbar mit dem knappen **Untergruppenkriterium** $u v^{-1} \in U$.

## 2 Ringe und Körper — zwei Verknüpfungen

Ein [[Ring]] hat **zwei** Verknüpfungen $+$ und $\cdot$, verbunden durch das **Distributivgesetz**: $(R,+)$ ist abelsche Gruppe, $(R,\cdot)$ eine Halbgruppe. Ein [[Körper]] ist ein besonders „gutartiger" kommutativer Ring mit Eins, in dem **jedes** Element $\neq 0$ multiplikativ invertierbar ist (z. B. $\mathbb{Q}, \mathbb{R}, \mathbb{C}, \mathbb{Z}_p$ für Primzahlen $p$). Körper sind **nullteilerfrei**. Der Körper $K$ liefert später die *Skalare* der Vektorräume.

[[Polynomringe]] $K[x]$ zeigen die Ring-Struktur an Polynomen: **Gradformel**, **Division mit Rest**, Nullstellen als Linearfaktoren. [[Der Körper der komplexen Zahlen]] $\mathbb{C}$ macht jedes Polynom lösbar; über [[Polarkoordinaten]] und die Eulersche Formel $e^{i\varphi} = \cos\varphi + i\sin\varphi$ werden Multiplikation und Wurzeln geometrisch.

## 3 Vektorräume — das Herzstück

Ein [[Vektorraum]] über einem [[Körper]] $K$ ist eine abelsche Gruppe $(V,+)$ zusammen mit einer **skalaren Multiplikation** $K \times V \to V$, die mit beiden Strukturen verträglich ist. Prototyp: $K^n$.

Die zentralen Begriffe:
- **[[Untervektorräume]]**: Teilmengen, die selbst Vektorraum sind (Unterraumkriterium).
- **[[Linearkombinationen und lineare (Un-)Abhängigkeit]]**: Vektoren sind *linear unabhängig*, wenn sich der Nullvektor nur trivial kombinieren lässt.
- **[[Dimension und Basis]]**: Eine **Basis** ist ein linear unabhängiges Erzeugendensystem; ihre Länge ist die **Dimension** — eine wohldefinierte Zahl (alle Basen sind gleich lang, [[Austauschsatz von Steinitz und Basisergänzungssatz|Steinitz]]).
- **[[Erzeugte Unterräume, Schnitt und Summe von Unterräumen]]**: Die **Dimensionsformel** $\dim(U+W) = \dim U + \dim W - \dim(U \cap W)$.

## 4 Matrizen und lineare Gleichungssysteme — die Rechenmaschine

Eine [[Matrix]] ist ein Zahlenschema; $M_n(K)$ bildet einen Ring, $M_{m,n}(K)$ einen Vektorraum. Matrizen kodieren **[[Lineare Gleichungssysteme]]** $Ax = b$. Das Lösen geschieht durch **[[Elementare Zeilenumformungen und Transformation in Zeilenstufenform|elementare Zeilenumformungen]]** in **Zeilenstufenform** und dann per **[[Gaußsches Eliminationsverfahren zur Bestimmung der Lösung eines LGS|Gauß-Elimination]]**.

Der **[[Zeilen- und Spaltenrang|Rang]]** (= Zahl der Stufen) misst die „effektive Größe" der Matrix; erstaunlich: **Zeilenrang = Spaltenrang**. Der Rang entscheidet über Lösbarkeit und Lösungsdimension eines LGS. Eine quadratische Matrix ist **[[Matrixinverse|invertierbar]]** genau dann, wenn $\operatorname{rg}(A) = n$ — berechnet mit Gauß-Jordan.

## 5 Determinanten — eine Zahl entscheidet über Invertierbarkeit

Die [[Determinante]] ordnet jeder quadratischen Matrix einen Skalar zu (rekursiv via [[Definition und Eigenschaften|Laplace-Entwicklung]], für $3\times3$ auch Sarrus). Ihre wichtigste Rolle: **[[Invertierbarkeit und Determinante]]** — $A$ ist invertierbar $\iff \det(A) \neq 0$. Dazu kommen Rechenregeln (D1–D8), etwa das Verhalten unter Zeilenumformungen und $\det(AB) = \det(A)\det(B)$.

## 6 Eigenwerte und Eigenvektoren — Richtungen, die erhalten bleiben

Ein **[[Eigenwert und Eigenvektor|Eigenvektor]]** $x \neq \mathcal{O}$ erfüllt $Ax = \lambda x$: $A$ streckt ihn nur um den **Eigenwert** $\lambda$. Man findet die Eigenwerte als Nullstellen des **[[Eigenwerte, Eigenvektoren, Eigenräume|charakteristischen Polynoms]]** $p_A(\lambda) = \det(A - \lambda E_n)$. Besitzt $A$ genug (nämlich $n$) linear unabhängige Eigenvektoren, ist $A$ **[[Diagonalisierbarkeit und Spektralsatz|diagonalisierbar]]**: $A = SDS^{-1}$ mit Diagonalmatrix $D$ — extrem nützlich, z. B. für Matrixpotenzen $A^k = SD^kS^{-1}$.

## 7 Norm und Skalarprodukt — Länge und Winkel

Das **[[Norm und Skalarprodukt|Skalarprodukt]]** $(v \mid w)$ misst über $\|v\|\,\|w\|\cos\alpha$ bzw. koordinatenweise $v^Tw$ **Winkel** zwischen Vektoren; die **Norm** $\|v\| = \sqrt{(v\mid v)}$ misst **Längen**, und $d(v,w) = \|v-w\|$ den **Abstand**. Damit wird der Vektorraum zum *euklidischen* Raum mit Geometrie.

## 8 Lineare Abbildungen — strukturerhaltende Abbildungen

Eine [[Lineare Abbildung]] $\varphi: V \to W$ ist mit $+$ und skalarer Multiplikation verträglich. Ihre Kennzahlen: **[[Rang und Kern linearer Abbildungen|Kern und Bild]]** (Rang $=\dim$ Bild). Der **Dimensionssatz** $\dim V = \dim(\ker\varphi) + \operatorname{rg}(\varphi)$ verknüpft alles. Auf **[[Lineare Abbildungen auf endlichdimensionalen Vektorräumen|endlichdimensionalen Räumen]]** werden lineare Abbildungen durch Matrizen dargestellt — damit schließt sich der Kreis zu Kapitel 4: injektiv $=$ surjektiv $=$ bijektiv, sobald $\dim V = \dim W$.

---

> [!tip] Wie hängt alles zusammen?
> **Gruppe → Ring/Körper → Vektorraum** ist die Struktur-Leiter. **Matrix** ist die konkrete Rechenform, **Determinante** und **Rang** sind ihre Kennzahlen, **Eigenwerte** ihre „Eigenrichtungen", **lineare Abbildungen** die abstrakte Sicht darauf. Der Begriff **Invertierbarkeit** taucht auf jeder Ebene auf (Gruppeninverse, Einheit im Ring, Matrixinverse, $\det \neq 0$, Rang $= n$, Isomorphismus) — ein guter Aufhänger zum Wiederholen.
