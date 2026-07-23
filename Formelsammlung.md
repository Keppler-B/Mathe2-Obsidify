# Formelsammlung — Lineare Algebra (Mathematik für Informatik 2)

> Alle klausurrelevanten Definitionen, Sätze und Formeln kompakt. Jeder Eintrag verlinkt auf die ausführliche Herleitung.
> Navigation: [[Inhaltsverzeichnis]] · [[Zusammenfassung]] · [[Checklist]]

---

## 1 Gruppen

**[[Gruppe]]** $(G, \ast)$: abgeschlossen, und
1. $(a \ast b) \ast c = a \ast (b \ast c)$ (Assoziativität)
2. $\exists\, e:\ a \ast e = e \ast a = a$ (neutrales Element)
3. $\forall a\ \exists\, a^{-1}:\ a \ast a^{-1} = a^{-1} \ast a = e$ (Inverse)
4. *abelsch*, falls zusätzlich $a \ast b = b \ast a$. **Ordnung** $|G|$ = Anzahl der Elemente. **Halbgruppe** = nur (1).

**Rechenregeln** ([[Eigenschaften und Rechenregeln]]): neutrales Element & Inverse eindeutig; $(ab)^{-1} = b^{-1}a^{-1}$; $ax = b \Rightarrow x = a^{-1}b$; Kürzungsregel.

**[[Die symmetrische Gruppe Sn|Symmetrische Gruppe]]** $S_n$: Permutationen von $\{1,\dots,n\}$ mit $(\sigma \circ \tau)(i) = \sigma(\tau(i))$. $\;|S_n| = n!$. Für $n \geq 3$ nicht abelsch. Neutrales Element $\varepsilon = \mathrm{id}$.

**[[Restklassen modulo m als Gruppe|Restklassen]]** $\mathbb{Z}_m = \{0,\dots,m-1\}$: $r_1 \oplus r_2 = (r_1+r_2)\bmod m$, $\ r_1 \odot r_2 = (r_1 r_2)\bmod m$.
- $n_1 \equiv n_2 \bmod m \iff m \mid (n_1 - n_2)$.
- $(\mathbb{Z}_m, \oplus)$ ist abelsche Gruppe; additiv Inverses $-a = m - a$ (für $a \neq 0$).
- $x$ invertierbar bzgl. $\odot \iff \gcd(x, m) = 1$. &nbsp; $\mathbb{Z}_m^* = \{x \mid \gcd(x,m)=1\}$, &nbsp; $\varphi(m) = |\mathbb{Z}_m^*|$, &nbsp; $\varphi(p) = p-1$ ($p$ prim).

**[[Untergruppen|Untergruppenkriterium]]** ($U \leq G$): $\emptyset \neq U \subseteq G$ und $\;u \cdot v^{-1} \in U$ für alle $u, v \in U$.

## 2 Ringe und Körper

**[[Ring]]** $(R, +, \cdot)$: $(R,+)$ abelsche Gruppe, $(R,\cdot)$ Halbgruppe, **Distributivgesetze** $a(b+c) = ab + ac$, $(a+b)c = ac + bc$. *Ring mit Eins*: $\exists\, 1 \neq 0$. **Einheiten** $R^*$ = invertierbare Elemente.
Rechenregeln: $a \cdot 0 = 0$; $(-a)b = -(ab)$; $(-a)(-b) = ab$.

**[[Körper]]** $K$: kommutativer Ring mit Eins, in dem **jedes** $a \neq 0$ invertierbar ist ($K^* = K \setminus \{0\}$). Körper sind **nullteilerfrei**: $ab = 0 \Rightarrow a = 0$ oder $b = 0$. Beispiele: $\mathbb{Q}, \mathbb{R}, \mathbb{C}, \mathbb{Z}_p$ ($p$ prim).

**[[Polynomringe]]** $K[x]$: **Gradformel** $\operatorname{grad}(f \cdot g) = \operatorname{grad}(f) + \operatorname{grad}(g)$; Division mit Rest $f = q \cdot g + r$ mit $\operatorname{grad}(r) < \operatorname{grad}(g)$; $a$ Nullstelle $\iff (x-a) \mid f$.

**[[Der Körper der komplexen Zahlen|Komplexe Zahlen]]** $\mathbb{C} = \{a + bi \mid a,b \in \mathbb{R}\}$, $i^2 = -1$. Konjugierte $\overline{z} = a - bi$, Betrag $|z| = \sqrt{a^2 + b^2} = \sqrt{z\overline{z}}$, $z^{-1} = \overline{z}/|z|^2$.
**[[Polarkoordinaten]]**: $z = r(\cos\varphi + i\sin\varphi) = r\,e^{i\varphi}$ mit $r = |z|$. **Eulersche Formel** $e^{i\varphi} = \cos\varphi + i\sin\varphi$. Multiplikation: Beträge multiplizieren, Winkel addieren.

## 3 Vektorräume

**[[Vektorraum|$K$-Vektorraum]]** $V$: $(V,+)$ abelsche Gruppe (Nullvektor $\mathcal{O}$) + skalare Multiplikation $K \times V \to V$ mit
$(\lambda\mu)v = \lambda(\mu v)$, &nbsp; $(\lambda+\mu)v = \lambda v + \mu v$, &nbsp; $\lambda(v+w) = \lambda v + \lambda w$, &nbsp; $1 \cdot v = v$.

**[[Untervektorräume|Unterraumkriterium]]**: $\emptyset \neq U \subseteq V$ ist Unterraum $\iff$ $u + w \in U$ und $\lambda u \in U$ für alle $u, w \in U$, $\lambda \in K$ (äquiv.: $\mathcal{O} \in U$ und abgeschlossen unter Linearkombination).

**[[Linearkombinationen und lineare (Un-)Abhängigkeit|Lineare (Un-)Abhängigkeit]]**: $v_1,\dots,v_k$ **linear unabhängig** $\iff$ aus $\sum \lambda_i v_i = \mathcal{O}$ folgt $\lambda_1 = \dots = \lambda_k = 0$.

**[[Dimension und Basis|Basis & Dimension]]**: Basis = linear unabhängiges Erzeugendensystem. Alle Basen eines Vektorraums sind gleich lang; ihre Länge ist $\dim V$. Jeder Vektor hat **eindeutige** Koordinaten bzgl. einer geordneten Basis. $\dim(K^n) = n$, $\dim(M_{m,n}(K)) = m \cdot n$.

**[[Austauschsatz von Steinitz und Basisergänzungssatz|Steinitz / Basisergänzung]]**: Man kann linear unabhängige Vektoren gegen Basisvektoren tauschen; jede l.u. Menge lässt sich zu einer Basis ergänzen.

**Dimensionsformel** ([[Erzeugte Unterräume, Schnitt und Summe von Unterräumen]]):
$$\dim(U + W) = \dim U + \dim W - \dim(U \cap W).$$

## 4 Matrizen und lineare Gleichungssysteme

**[[Matrix]]** $A = (a_{ij}) \in M_{m,n}(K)$. Transponierte $A^T$, Einheitsmatrix $E_n = (\delta_{ij})$.
**Matrixprodukt** ($A \in M_{m,n}$, $B \in M_{n,l}$): $\;(AB)_{ik} = \sum_{j=1}^{n} a_{ij} b_{jk}$ &nbsp;(Spalten von $A$ = Zeilen von $B$!).
$M_n(K)$ ist Ring mit Eins $E_n$. $A$ **invertierbar**: $AA^{-1} = A^{-1}A = E_n$.

**[[Lineare Gleichungssysteme|LGS]]** $Ax = b$: **erweiterte Koeffizientenmatrix** $(A \mid b)$. Elementare Zeilenumformungen ändern die Lösungsmenge nicht.

**[[Zeilen- und Spaltenrang|Rang]]** $\operatorname{rg}(A)$ = Zahl der Stufen der [[Elementare Zeilenumformungen und Transformation in Zeilenstufenform|Zeilenstufenform]] = Zeilenrang = **Spaltenrang**.
- LGS lösbar $\iff \operatorname{rg}(A) = \operatorname{rg}(A \mid b)$.
- Lösungsraum von $Ax = 0$ (Kern) hat Dimension $n - \operatorname{rg}(A)$.
- Allgemeine Lösung = spezielle Lösung $+$ Kern ([[Gaußsches Eliminationsverfahren zur Bestimmung der Lösung eines LGS|Gauß]]).

**[[Matrixinverse|Invertierbarkeit]]** (Satz 4.26):
$$A \text{ invertierbar} \iff \operatorname{rg}(A) = n.$$
Berechnung: Gauß-Jordan an $(A \mid E_n) \to (E_n \mid A^{-1})$.

## 5 Determinanten

**[[Determinante]]** rekursiv (Laplace nach 1. Zeile): $\det(a) = a$ und
$$\det(A) = \sum_{j=1}^{n} (-1)^{1+j} a_{1j} \det(A_{1j}).$$
- $2\times2$: $\det\begin{pmatrix} a & b \\ c & d \end{pmatrix} = ad - bc$.
- $3\times3$: **Regel von Sarrus** (nur $3\times3$!).
- **[[Definition und Eigenschaften|Eigenschaften]]** (D1–D8): $\det(E_n) = 1$; Dreiecksmatrix = Produkt der Diagonale; $\det(A^T) = \det(A)$; $\det(AB) = \det(A)\det(B)$; Zeilentausch $\Rightarrow$ Vorzeichenwechsel; Zeile $\cdot \lambda \Rightarrow \det \cdot \lambda$.

**[[Invertierbarkeit und Determinante]]** (Satz 5.9):
$$A \text{ invertierbar} \iff \det(A) \neq 0.$$
**Inverse einer $2\times2$-Matrix**: $\;A^{-1} = \dfrac{1}{\det(A)} \begin{pmatrix} d & -b \\ -c & a \end{pmatrix}$ (für $\det(A) \neq 0$).

## 6 Eigenwerte und Eigenvektoren

**[[Eigenwert und Eigenvektor]]**: $\lambda \in K$ Eigenwert, $x \neq \mathcal{O}$ Eigenvektor $\iff Ax = \lambda x$. **Eigenraum** $\operatorname{Eig}(\lambda) = \{x \mid Ax = \lambda x\} = \ker(A - \lambda E_n)$.

**[[Eigenwerte, Eigenvektoren, Eigenräume|Berechnung]]** (Satz 6.2 / charakteristisches Polynom):
$$\lambda \text{ Eigenwert} \iff \det(A - \lambda E_n) = 0, \qquad p_A(\lambda) := \det(A - \lambda E_n).$$
Eigenvektoren zu $\lambda$ = nichttriviale Lösungen von $(A - \lambda E_n)x = \mathcal{O}$. *Algebraische Vielfachheit* = Vielfachheit der Nullstelle; *geometrische Vielfachheit* $= \dim \operatorname{Eig}(\lambda)$.

**[[Diagonalisierbarkeit und Spektralsatz|Diagonalisierbarkeit]]**: $A = SDS^{-1}$ mit Diagonalmatrix $D$. **Spektralsatz**:
$$A \text{ diagonalisierbar} \iff A \text{ besitzt } n \text{ linear unabhängige Eigenvektoren}.$$
Dann sind die Spalten von $S$ die Eigenvektoren, die Diagonale von $D$ die Eigenwerte. Anwendung: $A^k = S D^k S^{-1}$.

## 7 Norm und Skalarprodukt

**[[Norm und Skalarprodukt|Skalarprodukt]]**: geometrisch $(v \mid w) = \|v\|\,\|w\|\cos\alpha$; koordinatenweise $(v \mid w) = \sum_i v_i w_i = v^T w$.
Eigenschaften (Satz 7.4): symmetrisch, bilinear (linear in beiden Argumenten), positiv definit $(v \mid v) > 0$ für $v \neq \mathcal{O}$.

**Norm** (Länge): $\;\|v\| = \sqrt{(v \mid v)} = \left(\sum_{i=1}^n v_i^2\right)^{1/2}$.
Eigenschaften (Satz 7.2): $\|v\| \geq 0$ ($=0 \iff v = \mathcal{O}$); $\|\lambda v\| = |\lambda|\,\|v\|$; **Dreiecksungleichung** $\|v + w\| \leq \|v\| + \|w\|$.

**Abstand** $d(v, w) = \|v - w\|$. &nbsp; **Winkel** $\cos\alpha = \dfrac{(v \mid w)}{\|v\|\,\|w\|}$. &nbsp; Orthogonal $\iff (v \mid w) = 0$.

## 8 Lineare Abbildungen

**[[Lineare Abbildung]]** $\varphi: V \to W$: $\varphi(v_1 + v_2) = \varphi(v_1) + \varphi(v_2)$ und $\varphi(\lambda v) = \lambda \varphi(v)$; kurz $\varphi(\lambda v_1 + \mu v_2) = \lambda\varphi(v_1) + \mu\varphi(v_2)$. **Isomorphismus** = bijektive lineare Abbildung ($V \cong W$).

**[[Rang und Kern linearer Abbildungen|Kern & Bild]]**: $\ker\varphi = \{v \mid \varphi(v) = \mathcal{O}\}$ (Unterraum von $V$), $\operatorname{Bild}(\varphi) = \varphi(V)$ (Unterraum von $W$), $\operatorname{rg}(\varphi) = \dim\varphi(V)$. $\varphi$ injektiv $\iff \ker\varphi = \{\mathcal{O}\}$.

**[[Lineare Abbildungen auf endlichdimensionalen Vektorräumen|Dimensionssatz]]** (Satz 8.11):
$$\dim V = \dim(\ker\varphi) + \operatorname{rg}(\varphi).$$
**Äquivalenzsatz** (Kor 8.12, für $\dim V = \dim W < \infty$): $\varphi$ injektiv $\iff$ surjektiv $\iff$ bijektiv.

---

> [!tip] Prüfungs-Trigger „Invertierbarkeit"
> Für $A \in M_n(K)$ sind äquivalent: $A$ invertierbar $\iff \det(A) \neq 0 \iff \operatorname{rg}(A) = n \iff$ Spalten linear unabhängig $\iff \ker(A) = \{\mathcal{O}\} \iff 0$ ist **kein** Eigenwert $\iff Ax = b$ eindeutig lösbar für alle $b$.
