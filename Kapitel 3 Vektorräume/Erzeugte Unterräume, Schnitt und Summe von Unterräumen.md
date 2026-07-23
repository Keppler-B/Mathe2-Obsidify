---
tags: [kapitel-3, thema, definition, satz, beispiel]
quelle: Skript S. 54–57
aliases: [erzeugter Unterraum, aufgespannter Unterraum, Erzeugendensystem, Schnitt von Unterräumen, Summe von Unterräumen, Dimensionsformel]
---
# Erzeugte Unterräume, Schnitt und Summe von Unterräumen

> Kapitel 3 · Vektorräume — letzter Abschnitt. Zurück zum [[Inhaltsverzeichnis]].
> Voriges Thema: [[Austauschsatz von Steinitz und Basisergänzungssatz]] · Nächstes Thema: [[Matrizen und Operationen mit Matrizen]] (Kapitel 4)
> Grundlage: [[Untervektorräume]], [[Linearkombinationen und lineare (Un-)Abhängigkeit]], [[Dimension und Basis]]

## Definition 3.29 (Erzeugter Unterraum)

Sei $V$ ein $K$-Vektorraum und $M \subseteq V$.

**(a)** Der von $M$ **erzeugte** oder **aufgespannte Unterraum** $\langle M \rangle_K$ (oder nur $\langle M \rangle$) ist die Menge aller endlichen Linearkombinationen, die man mit Vektoren aus $M$ bilden kann, also
$$\langle M \rangle_K := \left\{ \sum_{i=1}^n \lambda_i v_i \;\middle|\; \lambda_i \in K,\; v_i \in M,\; n \in \mathbb{N} \right\}.$$
Dabei definieren wir
$$\langle \emptyset \rangle_K := \{\mathcal{O}\}.$$
Für $M = \{v_1, \dots, v_m\}$ schreiben wir auch $\langle v_1, \dots, v_m \rangle_K$.

**(b)** Ist $V = \langle M \rangle$, so heißt $M$ ein **Erzeugendensystem** von $V$.

## Bemerkung 3.30

**(a)** $\langle M \rangle_K$ ist wegen [[Untervektorräume|Satz 3.7 (Unterraumkriterium)]] tatsächlich ein Unterraum, und zwar der **kleinste**, der $M$ enthält: $M \subseteq \langle M \rangle_K$ gilt, und ist $U$ ein Unterraum von $V$ mit $M \subseteq U$, so enthält $U$ alle endlichen Linearkombinationen von Elementen aus $M$ (Satz 3.7), kann also nicht kleiner als $\langle M \rangle_K$ sein.

**(b)** Nach unseren Definitionen/Sätzen über die Dimension gilt
$$\dim \left( \langle v_1, \dots, v_m \rangle_K \right) \leq m$$
und
$$\dim \left( \langle v_1, \dots, v_m \rangle_K \right) = m \iff v_1, \dots, v_m \text{ sind linear unabhängig.}$$

**(c)** Man nennt $M \subseteq V$ eine **Basis** von $V$, wenn $\langle M \rangle = V$ gilt und die Vektoren aus $M$ linear unabhängig sind. Dieser „neue" Basisbegriff stimmt im Falle $\dim V < \infty$ mit dem [[Dimension und Basis|bisherigen]] überein, gilt aber auch für $\dim V = \infty$. Zum Beispiel ist damit $M = \{1, x, x^2, \dots\}$ eine Basis von $\{p : \mathbb{R} \to \mathbb{R},\; p \text{ ist Polynom}\} \subseteq \mathcal{F}(\mathbb{R}, \mathbb{R})$.

## Definition/Satz 3.31 (Schnitt und Summe von Unterräumen)

Sei $V$ ein $K$-Vektorraum und $U_1, U_2$ Unterräume von $V$.

**(a)** Der **Durchschnitt** von $U_1$ und $U_2$,
$$U_1 \cap U_2 := \{ u \in V \mid u \in U_1 \wedge u \in U_2 \},$$
ist ein Unterraum von $V$.

**(b)** Die **Summe** von $U_1$ und $U_2$,
$$U_1 + U_2 := \{ u_1 + u_2 \mid u_1 \in U_1,\; u_2 \in U_2 \},$$
ist ein Unterraum von $V$.

> [!note]- Beweis
> Jeweils durch Nachrechnen des Unterraumkriteriums (Satz 3.7).
>
> **(a)** &nbsp;**(1)** Der Nullvektor liegt in $U_1 \cap U_2$: $\mathcal{O} \in U_1$, da $U_1$ Unterraum ist, und $\mathcal{O} \in U_2$, da $U_2$ Unterraum ist, damit also auch $\mathcal{O} \in U_1 \cap U_2$.
> &nbsp;&nbsp;**(2)** Sei $\lambda \in K,\; v \in U_1 \cap U_2$, d. h. $v \in U_1$ und $v \in U_2$. Dann ist $\lambda v \in U_1$ (da $U_1$ Unterraum ist) und $\lambda v \in U_2$ (da $U_2$ Unterraum ist), also gilt $\lambda v \in U_1 \cap U_2$.
> &nbsp;&nbsp;**(3)** Seien $u, v \in U_1 \cap U_2$, d. h. $u, v \in U_1$ und $u, v \in U_2$. Dann ist $u + v \in U_1$ (da $U_1$ Unterraum) und $u + v \in U_2$ (da $U_2$ Unterraum), also gilt $u + v \in U_1 \cap U_2$.
>
> **(b)** &nbsp;**(1)** Der Nullvektor liegt in $U_1 + U_2$ (muss aber nicht unbedingt geprüft werden, wenn (2) und (3) unten erfüllt sind): $\mathcal{O} = \underbrace{\mathcal{O}}_{\in U_1} + \underbrace{\mathcal{O}}_{\in U_2} \in U_1 + U_2$.
> &nbsp;&nbsp;**(2)** Sei $v = \underbrace{u_1}_{\in U_1} + \underbrace{u_2}_{\in U_2} \in U_1 + U_2,\; \lambda \in K$. Dann ist $\lambda \cdot v = \lambda(u_1 + u_2) = \underbrace{\lambda u_1}_{\in U_1} + \underbrace{\lambda u_2}_{\in U_2} \in U_1 + U_2$.
> &nbsp;&nbsp;**(3)** Seien $v = \underbrace{u_1}_{\in U_1} + \underbrace{u_2}_{\in U_2},\; w = \underbrace{u_1'}_{\in U_1} + \underbrace{u_2'}_{\in U_2} \in U_1 + U_2$. Dann ist $v + w = u_1 + u_2 + u_1' + u_2' = \underbrace{(u_1 + u_1')}_{\in U_1} + \underbrace{(u_2 + u_2')}_{\in U_2} \in U_1 + U_2$. $\qquad \blacksquare$

## Bemerkung 3.32

**(a)** Satz 3.31(a) gilt auch für unendlich viele Unterräume, 3.31(b) hingegen nur für endlich viele. Die Vereinigung zweier Unterräume (also $U_1 \cup U_2$ für zwei Unterräume $U_1, U_2$) ist im Allgemeinen **kein** Unterraum.

**(b)** Der Schnitt zweier Unterräume ist nie leer, da $\mathcal{O}$ Element jedes Unterraums ist.

## Beispiel 3.33

Seien $v = \begin{pmatrix} 1 \\ 0 \end{pmatrix},\; w = \begin{pmatrix} 2 \\ 1 \end{pmatrix} \in \mathbb{R}^2,\; G_1 = \{\lambda v \mid \lambda \in \mathbb{R}\},\; G_2 = \{\mu w \mid \mu \in \mathbb{R}\}$. Die Mengen $G_1, G_2$ sind Geraden durch den Ursprung $\mathcal{O}$ und damit Unterräume von $\mathbb{R}^2$.

**(a)** $G_1 + G_2 = \{\lambda v + \mu w \mid \lambda, \mu \in \mathbb{R}\}$ ist eine Ebene durch $\mathcal{O}$ und Unterraum des $\mathbb{R}^2$ (hier: ganz $\mathbb{R}^2$).

**(b)** $G_1 \cap G_2 = \left\{ \begin{pmatrix} 0 \\ 0 \end{pmatrix} \right\}$:
$$\lambda \begin{pmatrix} 1 \\ 0 \end{pmatrix} = \mu \begin{pmatrix} 2 \\ 1 \end{pmatrix} \iff \begin{pmatrix} \lambda \\ 0 \end{pmatrix} = \begin{pmatrix} 2\mu \\ \mu \end{pmatrix} \iff \lambda = 2\mu \text{ und } 0 = \mu \iff \mu = 0 = \lambda.$$

**(c)** $G_1 \cup G_2$ ist die Vereinigung der beiden Geraden (also alle Punkte, die auf $G_1$ oder $G_2$ (oder beiden, also dem Ursprung) liegen).

## Satz 3.34 (Dimensionsformel für Unterräume)

Seien $U, W$ Unterräume eines endlichdimensionalen $K$-Vektorraums $V$. Dann gilt:
$$\dim(U + W) = \dim U + \dim W - \dim(U \cap W).$$
Insbesondere gilt: Falls $U \cap W = \{\mathcal{O}\}$, dann ist $\dim(U + W) = \dim U + \dim W$, da $\dim(U \cap W) = \dim(\{\mathcal{O}\}) = 0$.

> [!note]- Beweis
> Sei $k$ die Dimension des Schnittraums, also $\dim(U \cap W) = k \in \mathbb{N}_0$, und sei $v_1, \dots, v_k$ eine Basis des Schnittraums. Die Dimension von $U$ sei $n$, die Dimension von $W$ sei $m$ (es gilt: $m, n \geq k$). Als Ausgangspunkt nutzen wir die Basis des Schnittraums: Da die Vektoren dieser Basis sowohl in $U$ als auch in $W$ liegen, können wir sie nach dem [[Austauschsatz von Steinitz und Basisergänzungssatz|Basisergänzungssatz]] (Satz 3.26, Korollar 3.27) zu einer Basis von $U$ ausbauen (dazu müssen wir $n - k$ geeignete Vektoren $u_{k+1}, \dots, u_n$ aus $U$ hinzunehmen), und wir können sie auch zu einer Basis von $W$ ausbauen (dazu müssen wir $m - k$ geeignete Vektoren $w_{k+1}, \dots, w_m$ aus $W$ hinzunehmen). Wir müssen dann nur noch zeigen, dass die Vektoren $v_1, \dots, v_k, u_{k+1}, \dots, u_n, w_{k+1}, \dots, w_m$ eine Basis des Summenraums $U + W$ bilden. In diesem Fall ist dann die Dimension von $U + W$ gleich der Anzahl der Basisvektoren, und das sind $k + (n - k) + (m - k) = n + m - k$ Stück, was genau mit $\dim U + \dim W - \dim(U \cap W)$ übereinstimmt.
>
> **Erzeugendensystem.** Wir zeigen zuerst, dass sich jeder Vektor aus dem Summenraum $U + W$ als Linearkombination der angegebenen Vektoren $v_1, \dots, v_k, u_{k+1}, \dots, u_n, w_{k+1}, \dots, w_m$ schreiben lässt. Sei dazu $v \in U + W$ beliebig, also $v = u_1 + u_2$, wobei $u_1 \in U$ und $u_2 \in W$. Der Vektor $u_1$ lässt sich aber (da $v_1, \dots, v_k, u_{k+1}, \dots, u_n$ eine Basis von $U$ bilden) als Linearkombination von $v_1, \dots, v_k, u_{k+1}, \dots, u_n$ darstellen. Ebenso lässt sich $u_2$ (da $v_1, \dots, v_k, w_{k+1}, \dots, w_m$ eine Basis von $W$ bilden) als Linearkombination von $v_1, \dots, v_k, w_{k+1}, \dots, w_m$ darstellen. Daraus folgt, dass sich auch die Summe von $u_1$ und $u_2$ als Linearkombination von $v_1, \dots, v_k, u_{k+1}, \dots, u_n, w_{k+1}, \dots, w_m$ darstellen lässt.
>
> **Lineare Unabhängigkeit.** Schließlich müssen wir noch zeigen, dass die Vektoren $v_1, \dots, v_k, u_{k+1}, \dots, u_n, w_{k+1}, \dots, w_m$ linear unabhängig sind. Dazu stellen wir den Nullvektor $\mathcal{O}$ als Linearkombination dieser Vektoren dar und zeigen, dass dann die Koeffizienten der Linearkombination alle gleich null sein müssen. Seien dazu $\lambda_1, \dots, \lambda_k, \mu_{k+1}, \dots, \mu_n, \rho_{k+1}, \dots, \rho_m \in \mathbb{R}$ mit
> $$\mathcal{O} = \sum_{j=1}^k \lambda_j v_j + \sum_{j=k+1}^n \mu_j u_j + \sum_{j=k+1}^m \rho_j w_j.$$
> Die erste Summe ergibt einen Vektor $v \in U \cap W$, die zweite einen Vektor $u \in U$ und die dritte einen Vektor $w \in W$ (da jeweils nur Vektoren aus diesen Räumen benutzt werden). Es gilt nun aber: Der Vektor $w$ liegt ebenfalls in $U$, da $w = -v - u$ (obige Gleichung nach $w$ auflösen) und $-v$ und $-u$ beide in $U$ liegen. Außerdem gilt natürlich auch $w \in W$. Also gilt auch, dass $w \in U \cap W$. Da $v_1, \dots, v_k$ eine Basis dieses Schnittraums bildet, folgt, dass sich $w$ als LK von $v_1, \dots, v_k$ darstellen lässt, und damit die Koeffizienten $\rho_{k+1}, \dots, \rho_m$ alle gleich $0$ sein müssen.
> Da die Vektoren $v_1, \dots, v_k, u_{k+1}, \dots, u_n$ eine Basis von $U$ bilden und damit linear unabhängig sind, folgt, dass auch $\lambda_1, \dots, \lambda_k, \mu_{k+1}, \dots, \mu_n$ alle gleich $0$ sein müssen. $\qquad \blacksquare$

## Abschluss von Kapitel 3

Damit endet Kapitel 3. Es folgt [[Matrizen und Operationen mit Matrizen|Kapitel 4: Matrizen und lineare Gleichungssysteme]], in dem lineare Zusammenhänge mehrerer Variablen mithilfe von Matrizen dargestellt werden.
