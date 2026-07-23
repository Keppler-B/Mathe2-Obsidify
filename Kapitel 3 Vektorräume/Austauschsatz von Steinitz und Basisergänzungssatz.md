---
tags: [kapitel-3, thema, satz, beispiel]
quelle: Skript S. 52–53
aliases: [Austauschlemma, Austauschsatz von Steinitz, Basisergänzungssatz]
---
# Austauschsatz von Steinitz und Basisergänzungssatz

> Kapitel 3 · Vektorräume. Zurück zum [[Inhaltsverzeichnis]].
> Voriges Thema: [[Dimension und Basis]] · Nächstes Thema: [[Erzeugte Unterräume, Schnitt und Summe von Unterräumen]]
> Grundlage: [[Dimension und Basis]], [[Linearkombinationen und lineare (Un-)Abhängigkeit]]

Die folgenden (Hilfs-)Sätze zeigen, wie man eine gegebene [[Dimension und Basis|Basis]] eines Vektorraums in eine andere umwandeln kann, indem man manche Basisvektoren geschickt durch neue Vektorraumelemente ersetzt. Das ist vor allem dann hilfreich, wenn man eine Basis konstruieren möchte, die bestimmte vorgegebene Vektoren enthält.

## Satz 3.25 (Austauschlemma)

Sei $B = \{v_1, \dots, v_n\}$ eine Basis von $V$, sei $\mathcal{O} \neq w \in V,\; w = \sum_{i=1}^n \lambda_i v_i$. Ist $\lambda_j \neq 0$ für ein $j \in \{1, \dots, n\}$, so bilden die Vektoren
$$v_1, \dots, v_{j-1}, w, v_{j+1}, \dots, v_n,$$
also die Menge
$$(B \setminus \{v_j\}) \cup \{w\},$$
ebenfalls eine Basis von $V$.

Das bedeutet also, dass man den Basisvektor $v_j$ gegen $w$ austauschen kann, wenn das zugehörige Skalar $\lambda_j$ in der Linearkombination für $w$ ungleich $0$ ist.

> [!note]- Beweis
> Wir nehmen o. B. d. A. an, dass $\lambda_1 \neq 0$ in der Linearkombination für $w$ ist und zeigen: Dann sind die Vektoren $w, v_2, \dots, v_n$ (der Vektor $v_1$ wurde durch $w$ ersetzt) linear unabhängig. Das genügt nach Satz 3.20 und Satz 3.23.
> Sei dazu $\mu_1 w + \mu_2 v_2 + \cdots + \mu_n v_n = \mathcal{O}$ mit $\mu_i \in K$. Einsetzen von $w = \sum_{i=1}^n \lambda_i v_i$ ergibt
> $$\mu_1 \lambda_1 v_1 + (\mu_1 \lambda_2 + \mu_2) v_2 + \cdots + (\mu_1 \lambda_n + \mu_n) v_n = \mathcal{O}.$$
> Da $v_1, \dots, v_n$ linear unabhängig sind, müssen die in dieser Linearkombination des Nullvektors verwendeten Skalare alle $0$ sein, also $\mu_1 \lambda_1 = 0,\; \mu_1 \lambda_2 + \mu_2 = 0, \dots, \mu_1 \lambda_n + \mu_n = 0$. Da nach Voraussetzung $\lambda_1 \neq 0$, muss $\mu_1 = 0$ gelten und damit auch $\mu_2 = \cdots = \mu_n = 0$. Also sind $w, v_2, \dots, v_n$ linear unabhängig. $\qquad \blacksquare$

## Satz 3.26 (Austauschsatz von Steinitz[^steinitz])

Seien $v_1, \dots, v_n$ eine Basis von $V$ und seien $w_1, \dots, w_m \in V$ linear unabhängige Vektoren.[^mkleinern] Dann kann man $n - m$ Vektoren aus den $n$ Vektoren $v_1, \dots, v_n$ auswählen, die zusammen mit $w_1, \dots, w_m$ eine Basis von $V$ bilden.

[^steinitz]: Ernst Steinitz, deutscher Mathematiker
[^mkleinern]: Nach den bisherigen Sätzen können wir direkt folgern, dass dann $m \leq n$ gelten muss.

> [!note]- Beweis
> Wir wenden das Austauschlemma 3.25 sukzessive an:
>
> **(1)** Sei $w_1 \in V$, d. h. $w_1 = \sum_{j=1}^n \lambda_j v_j$. Wären alle $\lambda_j = 0$, so wäre $w_1 = \mathcal{O}$. Dann wären aber nach Bemerkung 3.12(b) $w_1, \dots, w_n$ nicht linear unabhängig. Also muss mindestens ein $\lambda_j$ ungleich $0$ sein. Sei o. B. d. A. $\lambda_1 \neq 0$. Nach Satz 3.25 kann man dann $v_1$ gegen $w_1$ austauschen und $w_1, v_2, \dots, v_n$ bilden eine Basis von $V$.
>
> **(2)** Sei $w_2 \in V$, d. h. $w_2 = \mu_1 w_1 + \sum_{j=2}^n \mu_j v_j$. Wären $\mu_2 = \cdots = \mu_n = 0$, so wäre $w_2 = \mu_1 w_1$ und demnach wären $w_1, w_2$ linear abhängig. Also muss mindestens ein $\mu_j$ ($j = 2, \dots, n$) ungleich $0$ sein. Sei o. B. d. A. $\mu_2 \neq 0$. Nach Satz 3.25 kann man dann $v_2$ gegen $w_2$ austauschen und $w_1, w_2, \dots, v_n$ bilden eine Basis von $V$.
>
> **(3)** Analog fährt man fort, bis schließlich $w_m$ eingetauscht wurde. $\qquad \blacksquare$

## Korollar 3.27 (Basisergänzungssatz)

Sei $V$ ein endlichdimensionaler Vektorraum. Dann lässt sich jede linear unabhängige Teilmenge von $V$ zu einer Basis von $V$ ergänzen.

> [!note]- Beweis
> Wähle eine beliebige Basis von $V$ und tausche mittels Satz 3.26 aus. $\qquad \blacksquare$

## Beispiel 3.28

Sei $V = \mathbb{R}^4,\; u_1 = \begin{pmatrix} 1 \\ 2 \\ 0 \\ 1 \end{pmatrix},\; u_2 = \begin{pmatrix} 0 \\ 2 \\ 1 \\ 0 \end{pmatrix} \in \mathbb{R}^4$. Die Vektoren $u_1, u_2$ sind linear unabhängig.

Wie kann man $u_1, u_2$ zu einer Basis von $V$ ergänzen? Wir wenden die Austauschsätze 3.25 und 3.26 an:

Die Menge $\{e_1, e_2, e_3, e_4\}$ ist die kanonische Basis von $V$. Es gilt
$$u_1 = 1 e_1 + 2 e_2 + 0 e_3 + 1 e_4,$$
d. h., man kann $u_1$ gegen einen der Vektoren $e_1, e_2, e_4$ eintauschen. Wir wählen z. B. den Vektor $e_1$ und erhalten $\{u_1, e_2, e_3, e_4\}$ als weitere Basis von $V$. Nun gilt
$$u_2 = 0 u_1 + 2 e_2 + 1 e_3 + 0 e_4,$$
d. h., man kann $u_2$ gegen einen der Vektoren $e_2, e_3$ eintauschen. Wir wählen z. B. den Vektor $e_3$ und erhalten $\{u_1, e_2, u_2, e_4\}$ als weitere Basis von $V$.

> [!info] Warum nicht gegen $e_1$ bzw. $u_1$?
> Im ersten Schritt darf $u_1$ nur gegen einen Basisvektor mit **von $0$ verschiedenem** Koeffizienten getauscht werden: $u_1 = 1 e_1 + 2 e_2 + 0 e_3 + 1 e_4$ — der Koeffizient von $e_3$ ist $0$, also kommt $e_3$ nicht in Frage. Im zweiten Schritt stellt man $u_2$ bezüglich der **neuen** Basis $\{u_1, e_2, e_3, e_4\}$ dar; der Koeffizient von $u_1$ ist $0$ und der von $e_4$ ist $0$, also bleiben nur $e_2$ und $e_3$.

## Weiter

- [[Erzeugte Unterräume, Schnitt und Summe von Unterräumen]] — der Basisergänzungssatz wird im Beweis der Dimensionsformel (Satz 3.34) verwendet
