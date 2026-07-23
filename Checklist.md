# Checklist zur Prüfungsvorbereitung — Lineare Algebra

> Hake jeden Punkt ab, wenn du ihn **verstanden hast** *und* **anwenden kannst** (nicht nur wiedererkennst). Jeder Checkpoint verlinkt auf das zugehörige Thema.
> Navigation: [[Inhaltsverzeichnis]] · [[Zusammenfassung]] · [[Formelsammlung]]

---

## Kapitel 1 — Gruppen

### [[Verknüpfungen, Gruppen, erste Beispiele]]
- [ ] Ich kann bei einer gegebenen Menge & Verknüpfung prüfen, ob sie **[[Verknüpfung und Abgeschlossenheit|abgeschlossen]]** ist.
- [ ] Ich kenne die **[[Gruppe|Gruppenaxiome]]** (Assoziativität, Neutrales, Inverse) und kann für ein Beispiel nachweisen, ob eine Gruppe / abelsche Gruppe / Halbgruppe vorliegt.
- [ ] Ich kann eine **Verknüpfungstafel** lesen und daraus Eigenschaften ablesen.

### [[Eigenschaften und Rechenregeln]]
- [ ] Ich kann begründen, warum neutrales Element und Inverse **eindeutig** sind, und $(ab)^{-1} = b^{-1}a^{-1}$ anwenden.
- [ ] Ich kann Gleichungen $ax = b$ in einer Gruppe lösen ($x = a^{-1}b$) — auch wenn $G$ nicht abelsch ist.

### [[Die symmetrische Gruppe Sn]]
- [ ] Ich kann Permutationen in Zweizeilen-Notation schreiben und **verknüpfen** ($\sigma \circ \tau$ = „$\sigma$ nach $\tau$").
- [ ] Ich kenne $|S_n| = n!$ und weiß, dass $S_n$ für $n \geq 3$ nicht abelsch ist.
- [ ] Ich kann die **Inverse** einer Permutation bestimmen und Gleichungen wie $\sigma \circ x = \tau$ lösen.

### [[Restklassen modulo m als Gruppe]]
- [ ] Ich kann modulo $m$ rechnen ($\oplus, \odot$) und mit $\equiv$ / $\bmod$ sicher umgehen (Unterschied Zahl vs. Relation).
- [ ] Ich kann additive und multiplikative Inverse in $\mathbb{Z}_m$ bestimmen und weiß: $x$ invertierbar $\iff \gcd(x,m) = 1$.
- [ ] Ich kann $\mathbb{Z}_m^*$ und $\varphi(m)$ bestimmen.

### [[Untergruppen]]
- [ ] Ich kann mit dem **Untergruppenkriterium** ($uv^{-1} \in U$) nachweisen, ob eine Teilmenge Untergruppe ist.

## Kapitel 2 — Ringe und Körper

### [[Ringe]]
- [ ] Ich kenne die **[[Ring|Ringaxiome]]** (inkl. Distributivgesetz) und die Begriffe *Ring mit Eins*, *Einheit*, *kommutativ*.
- [ ] Ich kann die Rechenregeln $a \cdot 0 = 0$, $(-a)(-b) = ab$ begründen und anwenden.

### [[Körper]]
- [ ] Ich kenne die Definition eines **[[Körper|Körpers]]** und kann prüfen, ob eine Struktur ein Körper ist (jedes $a \neq 0$ invertierbar).
- [ ] Ich verstehe **Nullteilerfreiheit** und weiß, warum $\mathbb{Z}_p$ genau für Primzahlen $p$ ein Körper ist.

### [[Polynomringe]]
- [ ] Ich kann die **Gradformel** anwenden und **Polynomdivision mit Rest** durchführen.
- [ ] Ich verstehe den Zusammenhang **Nullstelle $\leftrightarrow$ Linearfaktor** $(x - a)$.

### [[Der Körper der komplexen Zahlen]]
- [ ] Ich rechne sicher in $\mathbb{C}$ (Addition, Multiplikation, Konjugierte, Betrag, Inverse).

### [[Polarkoordinaten]]
- [ ] Ich kann komplexe Zahlen in **Polarform** $r\,e^{i\varphi}$ umrechnen und damit multiplizieren / Wurzeln (Einheitswurzeln) ziehen.
- [ ] Ich kenne die **Eulersche Formel**.

## Kapitel 3 — Vektorräume

### [[Vektorräume (Kapitel 3)|Vektorräume]]
- [ ] Ich kenne die **[[Vektorraum|Vektorraumaxiome]]** und kann für Beispiele ($K^n$, Funktionen, $\mathbb{Z}_p^n$) nachweisen, dass ein Vektorraum vorliegt.

### [[Untervektorräume]]
- [ ] Ich kann mit dem **Unterraumkriterium** entscheiden, ob eine Teilmenge Untervektorraum ist.

### [[Linearkombinationen und lineare (Un-)Abhängigkeit]]
- [ ] Ich kann eine **Linearkombination** bilden und **lineare Unabhängigkeit** nachweisen (bzw. widerlegen) — auch über einem endlichen Körper.

### [[Dimension und Basis]]
- [ ] Ich kann prüfen, ob eine Menge eine **Basis** ist, und die **Dimension** eines Vektorraums / Unterraums bestimmen.
- [ ] Ich kann **Koordinaten** eines Vektors bzgl. einer geordneten Basis berechnen.

### [[Austauschsatz von Steinitz und Basisergänzungssatz]]
- [ ] Ich verstehe den **Austauschsatz von Steinitz** und kann eine l.u. Menge zu einer **Basis ergänzen**.

### [[Erzeugte Unterräume, Schnitt und Summe von Unterräumen]]
- [ ] Ich kann erzeugte Unterräume, Schnitt und Summe bestimmen und die **Dimensionsformel** $\dim(U+W) = \dim U + \dim W - \dim(U \cap W)$ anwenden.

## Kapitel 4 — Matrizen und lineare Gleichungssysteme

### [[Matrizen und Operationen mit Matrizen]]
- [ ] Ich kann **[[Matrix|Matrizen]]** addieren, mit Skalar multiplizieren, transponieren und **multiplizieren** (Typ-Bedingung beachten!).

### [[Lineare Gleichungssysteme]]
- [ ] Ich kann ein LGS als $Ax = b$ / erweiterte Koeffizientenmatrix $(A \mid b)$ schreiben und die Struktur des Lösungsraums beschreiben.

### [[Elementare Zeilenumformungen und Transformation in Zeilenstufenform]]
- [ ] Ich kann eine Matrix durch **elementare Zeilenumformungen** in **Zeilenstufenform** bringen.

### [[Zeilen- und Spaltenrang]]
- [ ] Ich kann den **Rang** aus der Zeilenstufenform ablesen und weiß, dass **Zeilenrang = Spaltenrang** gilt.

### [[Gaußsches Eliminationsverfahren zur Bestimmung der Lösung eines LGS]]
- [ ] Ich kann ein LGS mit dem **Gauß-Verfahren** vollständig lösen (keine / genau eine / unendlich viele Lösungen) und die Lösung als *speziell + Kern* angeben.
- [ ] Ich kann die Lösbarkeit über $\operatorname{rg}(A)$ vs. $\operatorname{rg}(A\mid b)$ entscheiden.

### [[Matrixinverse]]
- [ ] Ich kann mit **Gauß-Jordan** die Inverse berechnen und weiß: $A$ invertierbar $\iff \operatorname{rg}(A) = n$.

## Kapitel 5 — Determinanten

### [[Definition und Eigenschaften]]
- [ ] Ich kann **[[Determinante|Determinanten]]** per **Laplace-Entwicklung** berechnen (und $2\times2$ / Sarrus für $3\times3$).
- [ ] Ich kenne die **Rechenregeln** (D1–D8): Verhalten bei Zeilenumformungen, $\det(AB) = \det(A)\det(B)$, $\det(A^T) = \det(A)$, Dreiecksmatrix.

### [[Invertierbarkeit und Determinante]]
- [ ] Ich weiß: $A$ invertierbar $\iff \det(A) \neq 0$, und kann die **$2\times2$-Inverse** über die Determinantenformel angeben.

## Kapitel 6 — Eigenwerte und Eigenvektoren

### [[Eigenwerte, Eigenvektoren, Eigenräume]]
- [ ] Ich verstehe die Gleichung $Ax = \lambda x$ und den Begriff **[[Eigenwert und Eigenvektor|Eigenraum]]**.
- [ ] Ich kann das **charakteristische Polynom** $p_A(\lambda) = \det(A - \lambda E_n)$ aufstellen und die **Eigenwerte** als Nullstellen bestimmen.
- [ ] Ich kann zu jedem Eigenwert die **Eigenvektoren / den Eigenraum** berechnen und algebraische vs. geometrische Vielfachheit unterscheiden.

### [[Diagonalisierbarkeit und Spektralsatz]]
- [ ] Ich kann entscheiden, ob $A$ **diagonalisierbar** ist (genug l.u. Eigenvektoren), und $S$, $D$ mit $A = SDS^{-1}$ aufstellen.
- [ ] Ich kann Diagonalisierung anwenden (z. B. **Matrixpotenzen** $A^k = SD^kS^{-1}$).

## Kapitel 7 — Norm und Skalarprodukt

### [[Norm und Skalarprodukt]]
- [ ] Ich kann das **Skalarprodukt** geometrisch und koordinatenweise ($v^T w$) berechnen und seine Eigenschaften (Symmetrie, Bilinearität, positiv definit) nennen.
- [ ] Ich kann **Norm** (Länge), **Abstand** und **Winkel** zwischen Vektoren berechnen und **Orthogonalität** prüfen.
- [ ] Ich kenne die **Dreiecksungleichung**.

## Kapitel 8 — Lineare Abbildungen

### [[Lineare Abbildungen (Kapitel 8)|Lineare Abbildungen]]
- [ ] Ich kann nachweisen, ob eine Abbildung **[[Lineare Abbildung|linear]]** ist (Additivität + Homogenität), und kenne den Begriff **Isomorphismus**.

### [[Rang und Kern linearer Abbildungen]]
- [ ] Ich kann **Kern** und **Bild** einer linearen Abbildung bestimmen, ihren **Rang** angeben und Injektivität über $\ker\varphi = \{\mathcal{O}\}$ prüfen.

### [[Lineare Abbildungen auf endlichdimensionalen Vektorräumen]]
- [ ] Ich kann den **Dimensionssatz** $\dim V = \dim(\ker\varphi) + \operatorname{rg}(\varphi)$ anwenden.
- [ ] Ich verstehe den **Äquivalenzsatz**: bei $\dim V = \dim W$ ist injektiv = surjektiv = bijektiv, und den Zusammenhang zu Matrizen.

---

> [!tip] Kapitelübergreifend verstehen
> - [ ] Ich kann die **Struktur-Leiter** [[Gruppe]] → [[Ring]]/[[Körper]] → [[Vektorraum]] erklären.
> - [ ] Ich kann die vielen **Invertierbarkeits-Kriterien** einer Matrix verknüpfen ($\det \neq 0$, $\operatorname{rg} = n$, Kern trivial, $0$ kein Eigenwert, Spalten l.u.) — siehe [[Formelsammlung]].
