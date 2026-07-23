---
tags: [kapitel-4, thema, satz, beispiel]
quelle: Skript S. 71–77
aliases: [Gauß-Verfahren, Gaußsches Eliminationsverfahren, Kern, freie Variablen, Korollar 4.21]
---
# Gaußsches Eliminationsverfahren zur Bestimmung der Lösung eines LGS

> Kapitel 4 · Matrizen und lineare Gleichungssysteme — fünftes Thema. Zurück zum [[Inhaltsverzeichnis]].
> Voriges Thema: [[Zeilen- und Spaltenrang]] · Nächstes Thema: [[Matrixinverse]]
> Grundlage: [[Lineare Gleichungssysteme]], [[Elementare Zeilenumformungen und Transformation in Zeilenstufenform]], [[Zeilen- und Spaltenrang]].

Wir wenden nun den Algorithmus zur Transformation in Zeilenstufenform ([[Elementare Zeilenumformungen und Transformation in Zeilenstufenform#Algorithmus 4.12 (Transformation auf Zeilenstufenform)|4.12]]) auf die erweiterte Koeffizientenmatrix eines LGS an, um dessen Lösungsmenge zu bestimmen. Alle Fälle, die dabei auftreten können, sind in folgendem Algorithmus beschrieben, der als **Gaußsches Eliminationsverfahren** bekannt ist. Die Matrizen in den Beispielen sind hier alle über $\mathbb{R}$.

## Algorithmus 4.20 (Gaußsches Eliminationsverfahren zur Lösung von LGS)

Gegeben sei das LGS $Ax = b$ über einem Körper $K$.

- Bilde die erweiterte Koeffizientenmatrix $(A, b)$.
- Wende Algorithmus 4.12 (Umformung auf Zeilenstufenform) auf $(A, b)$ an, erhalte Matrix $(\widetilde{A}, b')$ mit $\widetilde{A}$ in Zeilenstufenform.
- Bei Bedarf können auch **Spalten** in $\widetilde{A}$ vertauscht werden.
  > [!warning] Achtung (Spaltenvertauschung)
  > Eine Vertauschung von Spalte $i$ und Spalte $k$ bedeutet, dass die Unbekannten $x_i$ und $x_k$ vertauscht werden!
- Erhalte so eine Matrix $(A', b')$ der Form
  $$\left( \begin{array}{ccccccc|c} 1 & a'_{12} & \cdots & & \cdots & & a'_{1n} & b'_1 \\ 0 & 1 & a'_{23} & \cdots & & & a'_{2n} & b'_2 \\ 0 & 0 & \ddots & \cdots & & & \vdots & \vdots \\ 0 & 0 & 0 & 1 & a'_{r,r+1} & \cdots & a'_{rn} & b'_r \\ 0 & 0 & 0 & 0 & \cdots & & 0 & \vdots \\ 0 & 0 & 0 & 0 & \cdots & & 0 & \vdots \\ 0 & 0 & 0 & 0 & \cdots & & 0 & b'_m \end{array} \right)$$
  mit $r = \operatorname{rg}(A') = \operatorname{rg}(A)$. Es gilt offensichtlich $r \leq m$, $r \leq n$.
- Das neue LGS ist $A'x' = b'$. Der Vektor $x' = \begin{pmatrix} x'_1 \\ \vdots \\ x'_n \end{pmatrix}$ entsteht aus $x$ durch Vertauschen der Koordinaten entsprechend der durchgeführten Spaltenvertauschungen.
- Ermittle nun die Lösungsmenge des LGS:

### Fall 1 (keine Lösung)

Falls $r < m$ gilt und eines der Elemente $b'_{r+1}, \dots, b'_m$ ungleich $0$ ist, so ist das LGS **nicht lösbar**.
In diesem Fall gilt $\operatorname{rg}(A', b') > \operatorname{rg}(A')$ (die Matrix $(A', b')$ besitzt mehr Zeilen ungleich $\mathcal{O}^T$ als $A'$), also auch $\operatorname{rg}(A, b) > \operatorname{rg}(A)$.

Beispiel:
$$\left( \begin{array}{ccc|c} 1 & 2 & 3 & 2 \\ 0 & 1 & 4 & 7 \\ 0 & 0 & 0 & 3 \end{array} \right) \qquad (\text{hier ist } r = 2,\ m = 3)$$
Die dritte Zeile entspricht der Gleichung $0x_1 + 0x_2 + 0x_3 = 3$, die nie erfüllt ist. Das LGS besitzt also keine Lösung.

### Fall 2 (mindestens eine Lösung)

Falls $r = m$ oder ($r < m$ und $b'_{r+1} = \cdots = b'_m = 0$), so besitzt das LGS **mindestens eine Lösung**.
In diesem Fall gilt $\operatorname{rg}(A', b') = \operatorname{rg}(A')$, also auch $\operatorname{rg}(A, b) = \operatorname{rg}(A)$.

Beispiel:
$$\left( \begin{array}{ccccc|c} 1 & 2 & 3 & 4 & & 5 \\ 0 & 1 & 2 & 2 & & 7 \\ 0 & 0 & 1 & 4 & & 3 \end{array} \right), \qquad \left( \begin{array}{ccc|c} 1 & 2 & 3 & 5 \\ 0 & 1 & 2 & 7 \\ 0 & 0 & 1 & 3 \end{array} \right) \qquad (\text{hier ist jeweils } m = 3,\ r = 3,\ \text{also } r = m)$$
$$\left( \begin{array}{cccc|c} 1 & 2 & 3 & 4 & 5 \\ 0 & 1 & 2 & 2 & 7 \\ 0 & 0 & 0 & 0 & 0 \end{array} \right) \qquad (\text{hier ist } m = 3,\ r = 2,\ \text{also } r < m,\ \text{und } b'_{r+1} (= b'_3) = 0)$$

### Fall 2a (genau eine Lösung)

Ist $r = m = n$, so gibt es **genau eine Lösung**. Die $x'_1, \dots, x'_n$ sind eindeutig bestimmt und können durch rekursives Einsetzen ermittelt werden:

$$x'_n = b'_n, \qquad x'_{n-1} = b'_{n-1} - a'_{n-1,n} x'_n, \qquad \dots, \qquad x'_1 = b'_1 - \sum_{k=2}^{n} a'_{1k} x'_k.$$

Beispiel:
$$\left( \begin{array}{ccc|c} 1 & 2 & 3 & 5 \\ 0 & 1 & 4 & 4 \\ 0 & 0 & 1 & 3 \end{array} \right) \qquad (\text{hier ist } r = m = n = 3)$$
Ermitteln der Lösung: Aus der dritten Zeile ergibt sich direkt $x_3 = 3$. Eingesetzt in die zweite Zeile erhält man $x_2 + 4x_3 = 4 \Rightarrow x_2 + 12 = 4 \Rightarrow x_2 = -8$. Beide Werte eingesetzt in die erste Zeile ergibt $x_1 + 2x_2 + 3x_3 = 5 \Rightarrow x_1 - 16 + 9 = 5 \Rightarrow x_1 = 12$.

### Fall 2b (mehrere Lösungen)

Ist $r < n$ und $b'_{r+1} = \cdots = b'_m = 0$, so gibt es **mehrere Lösungen** (endlich viele, falls $K$ ein endlicher Körper ist, andernfalls unendlich viele Lösungen).

Wähle $x'_{r+1}, \dots, x'_n$ frei, die restlichen $x'_r, \dots, x'_1$ lassen sich dann rekursiv aus den vorhandenen Gleichungen bestimmen.

Beispiel:
$$\left( \begin{array}{ccc|c} 1 & 2 & 2 & 2 \\ 0 & 1 & 3 & 4 \\ 0 & 0 & 0 & 0 \end{array} \right) \qquad (\text{hier ist } m = 3,\ r = 2,\ b'_3 = 0)$$
Wähle $x_3$ frei, z. B. $x_3 = 0$. Berechne damit die Werte der übrigen Unbekannten $x_2, x_1$:
$x_3 = 0$ eingesetzt in die zweite Zeile ergibt $x_2 + 3x_3 = 4$, also $x_2 = 4$. Beide Werte eingesetzt in die erste Zeile ergibt $x_1 + 2x_2 + 2x_3 = 2 \Rightarrow x_1 + 8 + 0 = 2 \Rightarrow x_1 = -6$.
Also ist $x = (-6, 4, 0)^T$ eine Lösung von unendlich vielen (da das LGS über $\mathbb{R}$ definiert ist). Will man eine weitere Lösung angeben, kann man $x_3$ anders wählen, z. B. $x_3 = 1$, und damit wieder die restlichen Unbekannten bestimmen.

Um den ganzen **Lösungsraum** (der, wie wir inzwischen wissen, ein Unterraum ist) zu beschreiben, gibt man eine **Basis** dieses Raums an:

- Finde eine **spezielle Lösung** $x_0$ von $A'x' = b'$: Wähle dazu z. B. $x'_{r+1} = \cdots = x'_n = 0$, berechne damit $x'_1, \dots, x'_r$.
- Bestimme eine **Basis des Lösungsraums $U$** des zugehörigen homogenen LGS $A'x' = \mathcal{O}$: Setze dazu $(x'_{r+1}, \dots, x'_n)$ nacheinander
  $$(1, 0, 0, \dots, 0),\quad (0, 1, 0, \dots, 0),\quad \dots,\quad (0, 0, \dots, 0, 1),$$
  und berechne damit $x'_1, \dots, x'_r$.
- Nach Satz 4.6 ist die Lösung von $A'x' = b'$ dann $x_0 + U$.

Die Variablen $x'_{r+1}, \dots, x'_n$ bezeichnen wir als **freie Variablen** (man kann ihre Werte frei wählen und damit die Werte der restlichen Variablen bestimmen).

## Korollar 4.21 (Zusammenhang von Lösungsraum und Rang)

Am Rang von $(A, b)$ bzw. $A$ kann man die wichtigsten Informationen zur Lösungsmenge des LGS ablesen:

**(a)** $Ax = b$ ist genau dann **lösbar**, wenn $\operatorname{rg}(A, b) = \operatorname{rg}(A)$.

**(b)** $Ax = b$ ist genau dann **eindeutig lösbar**, wenn $\operatorname{rg}(A, b) = \operatorname{rg}(A) = n$, wobei $n$ die Anzahl der Unbekannten ist.

**(c)** Die Dimension des Lösungsraums von $Ax = \mathcal{O}$ (homogenes LGS) ist
$$n - \operatorname{rg}(A) \qquad (\underbrace{x'_{r+1}, \dots, x'_n}_{n - r \text{ Stück}} \text{ sind frei wählbar}).$$

## Definition/Bemerkung 4.22 (Kern der Koeffizientenmatrix)

Der Lösungsraum eines homogenen LGS $Ax = \mathcal{O}$ wird auch als **Kern von $A$** bezeichnet, geschrieben $\ker(A)$. Es gilt also

$$\dim(\ker(A)) = n - \operatorname{rg}(A).$$

## Beispiel 4.23 (LGS über $\mathbb{R}$)

**(a)** Homogenes LGS:
$$\begin{cases} x_1 + 2x_2 + x_3 + x_4 = 0 \\ x_1 - x_2 + 2x_3 - x_4 = 0 \end{cases}$$
$$\left( \begin{array}{cccc|c} 1 & 2 & 1 & 1 & 0 \\ 1 & -1 & 2 & -1 & 0 \end{array} \right) \xrightarrow{\mathrm{II}:\ \mathrm{I} \cdot (-1) + \mathrm{II}} \left( \begin{array}{cccc|c} 1 & 2 & 1 & 1 & 0 \\ 0 & -3 & 1 & -2 & 0 \end{array} \right) \xrightarrow{\mathrm{II} \cdot (-\frac{1}{3})} \left( \begin{array}{cccc|c} 1 & 2 & 1 & 1 & 0 \\ 0 & 1 & -\frac{1}{3} & \frac{2}{3} & 0 \end{array} \right)$$

Hier ist $\operatorname{rg}(A) = \operatorname{rg}(A, b) = 2 < n = 4$, das LGS hat also mindestens eine Lösung. Nach obigen Überlegungen (Korollar 4.21(c), Bemerkung 4.22) hat der Lösungsraum $U$ des homogenen LGS (der Kern von $A$) die Dimension $n - \operatorname{rg}(A) = 4 - 2 = 2$. Dies entspricht der Anzahl der freien Variablen: In der Zeilenstufenform des LGS sieht man, dass die beiden Variablen $x_3$ und $x_4$ frei wählbar sind. Um den Lösungsraum zu beschreiben, geben wir eine Basis von $U$ an:

Dazu wählen wir die Werte für $x_3$ und $x_4$ wie in [[#Fall 2b (mehrere Lösungen)|4.20 (Fall 2b)]] beschrieben und bestimmen damit jeweils die Werte der restlichen Variablen:

- $x_3 = 1,\ x_4 = 0$ gibt $x_2 = \frac{1}{3}$ und $x_1 = -\frac{2}{3} - 1 = -\frac{5}{3}$.
  $$\Rightarrow v_1 = \begin{pmatrix} -\frac{5}{3} \\ \frac{1}{3} \\ 1 \\ 0 \end{pmatrix} \text{ ist der 1. Basisvektor von } U.$$
- $x_3 = 0,\ x_4 = 1$ gibt $x_2 = -\frac{2}{3}$ und $x_1 = 0 + \frac{4}{3} + 0 - 1 = \frac{1}{3}$.
  $$\Rightarrow v_2 = \begin{pmatrix} \frac{1}{3} \\ -\frac{2}{3} \\ 0 \\ 1 \end{pmatrix} \text{ ist der 2. Basisvektor von } U.$$

Also erhalten wir

$$U = \langle v_1, v_2 \rangle_{\mathbb{R}} = \left\langle \underbrace{\begin{pmatrix} -5 \\ 1 \\ 3 \\ 0 \end{pmatrix}}_{3 v_1}, \underbrace{\begin{pmatrix} 1 \\ -2 \\ 0 \\ 3 \end{pmatrix}}_{3 v_2} \right\rangle = \left\{ \alpha \cdot \begin{pmatrix} -5 \\ 1 \\ 3 \\ 0 \end{pmatrix} + \beta \cdot \begin{pmatrix} 1 \\ -2 \\ 0 \\ 3 \end{pmatrix} \ \middle|\ \alpha, \beta \in \mathbb{R} \right\},$$

es handelt sich also um eine **Ebene durch den Nullpunkt** mit Richtungsvektoren $v_1$ und $v_2$.

**(b)** Nun betrachten wir ein **inhomogenes** LGS, das zum homogenen LGS aus (a) gehört:
$$\begin{cases} x_1 + 2x_2 + x_3 + x_4 = 7 \\ x_1 - x_2 + 2x_3 - x_4 = -2 \end{cases}$$
$$\left( \begin{array}{cccc|c} 1 & 2 & 1 & 1 & 7 \\ 1 & -1 & 2 & -1 & -2 \end{array} \right) \xrightarrow{\mathrm{II}:\ \mathrm{I} \cdot (-1) + \mathrm{II}} \left( \begin{array}{cccc|c} 1 & 2 & 1 & 1 & 7 \\ 0 & -3 & 1 & -2 & -9 \end{array} \right) \xrightarrow{\mathrm{II} \cdot (-\frac{1}{3})} \left( \begin{array}{cccc|c} 1 & 2 & 1 & 1 & 7 \\ 0 & 1 & -\frac{1}{3} & \frac{2}{3} & 3 \end{array} \right)$$

Um eine spezielle Lösung $x_0$ zu erhalten, wählt man $x_3, x_4$ frei, beispielsweise als $x_3 = 0$ und $x_4 = 0$. Damit erhält man $x_2 = 3$, $x_1 = 7 - 2 \cdot 3 = 1$, insgesamt also die spezielle Lösung $x_0 = \begin{pmatrix} 1 \\ 3 \\ 0 \\ 0 \end{pmatrix}$. Dies ist eine mögliche Lösung von unendlich vielen.

Um die allgemeine Lösung des inhomogenen LGS zu erhalten, verwenden wir (wie in 4.20 (Fall 2b) bzw. Satz 4.6 beschrieben) den Lösungsraum $U$ des entsprechenden homogenen LGS (aus Teil (a)). Die allgemeine Lösung des inhomogenen LGS hat damit die Form

$$\begin{pmatrix} 1 \\ 3 \\ 0 \\ 0 \end{pmatrix} + U = \left\{ \begin{pmatrix} 1 \\ 3 \\ 0 \\ 0 \end{pmatrix} + \alpha \cdot \begin{pmatrix} -5 \\ 1 \\ 3 \\ 0 \end{pmatrix} + \beta \cdot \begin{pmatrix} 1 \\ -2 \\ 0 \\ 3 \end{pmatrix} \ \middle|\ \alpha, \beta \in \mathbb{R} \right\},$$

es handelt sich also um eine **Ebene durch den Punkt** $\begin{pmatrix} 1 \\ 3 \\ 0 \\ 0 \end{pmatrix}$ (auch **Stützvektor** genannt) mit Richtungsvektoren $\begin{pmatrix} -5 \\ 1 \\ 3 \\ 0 \end{pmatrix}$ und $\begin{pmatrix} 1 \\ -2 \\ 0 \\ 3 \end{pmatrix}$.

> [!info] Weitere Beispiele
> Weitere Beispiele zur Bestimmung des Lösungsraums eines linearen Gleichungssystems finden sich auf den Vorlesungsfolien und in den Tafelanschrieben vom 24.06.2026.

## Beispiel/Bemerkung 4.24 (Rang zur Basisbestimmung)

**(a)** Sei $V = \mathbb{R}^3$, $W = \left\{ \begin{pmatrix} 2 \\ 1 \\ 1 \end{pmatrix}, \begin{pmatrix} 0 \\ 3 \\ -1 \end{pmatrix}, \begin{pmatrix} 2 \\ 7 \\ -1 \end{pmatrix}, \begin{pmatrix} -2 \\ -4 \\ 0 \end{pmatrix} \right\} \subseteq V$ eine Teilmenge von Vektoren aus $V$ und $U = \langle W \rangle$ der von $W$ erzeugte Unterraum.

Wie viele linear unabhängige Vektoren enthält $W$? Oder anders ausgedrückt, was ist die Dimension von $U$? Welche der gegebenen Vektoren aus $W$ lassen sich als Basis von $U$ verwenden? Diese Fragen können wir nun einfach mit dem Rang einer passenden Matrix (mit 4.12, wegen 4.17) beantworten. Es gilt (die Vektoren stehen als Spalten):

$$\dim U = \operatorname{rg} \begin{pmatrix} 2 & 0 & 2 & -2 \\ 1 & 3 & 7 & -4 \\ 1 & -1 & -1 & 0 \end{pmatrix} \qquad (\mathrm{II}:\ (-2) \cdot \mathrm{II} + \mathrm{I},\ \mathrm{III}:\ (-2) \cdot \mathrm{III} + \mathrm{I})$$
$$= \operatorname{rg} \begin{pmatrix} 2 & 0 & 2 & -2 \\ 0 & -6 & -12 & 6 \\ 0 & 2 & 4 & -2 \end{pmatrix} \qquad (\mathrm{III}:\ 3 \cdot \mathrm{III} + \mathrm{II})$$
$$= \operatorname{rg} \begin{pmatrix} 2 & 0 & 2 & -2 \\ 0 & -6 & -12 & 6 \\ 0 & 0 & 0 & 0 \end{pmatrix} = 2.$$

Also gibt es zwei linear unabhängige Vektoren in $U$. Das sind beispielsweise die Vektoren, die den **Stufenspalten** (hier die erste und zweite Spalte) entsprechen, nämlich $(2, 1, 1)^T$, $(0, 3, -1)^T$. Diese beiden Vektoren bilden eine Basis von $U$.

Würde die Matrix in Zeilenstufenform beispielsweise so aussehen: $\begin{pmatrix} 1 & 0 & 2 & 3 & 4 \\ 0 & 0 & 1 & 0 & 0 \\ 0 & 0 & 0 & 1 & 1 \end{pmatrix}$, so würden die Vektoren, die jeweils zum 1., 3. und 4. Spaltenvektor gehören, eine Basis bilden.

**(b)** Ein ähnliches Beispiel in einem **Funktionenraum**:
$V = \{p \mid p \text{ ist Polynom von Grad} \leq p\} \subseteq \mathcal{F}(\mathbb{R}, \mathbb{R})$,
$U = \langle 3x,\ 4x^2 + 2x + 2,\ 2x^2 + x + 1,\ 2x^2 + 1 \rangle \subseteq V$.

Wir wollen wieder $\dim U$ und eine Basis von $U$ aus den gegebenen Vektoren bestimmen. Dazu erstellen wir eine Matrix aus den Koordinatenvektoren der gegebenen Polynome bezüglich der geordneten Basis $(1, x, x^2)$ von $V$. Das Polynom $3x$ hat den Koordinatenvektor $(0, 3, 0)^T$, das Polynom $4x^2 + 2x + 2$ hat den Koordinatenvektor $(2, 2, 4)^T$, usw. Wir erhalten

$$\dim U = \operatorname{rg} \begin{pmatrix} 0 & 2 & 1 & 1 \\ 3 & 2 & 1 & 0 \\ 0 & 4 & 2 & 2 \end{pmatrix} \qquad (3x = 0 \cdot 1 + 3 \cdot x + 0 \cdot x^2)$$
$$= \operatorname{rg} \begin{pmatrix} 3 & 2 & 1 & 0 \\ 0 & 4 & 2 & 2 \\ 0 & 0 & 0 & 0 \end{pmatrix} = 2.$$

Wieder nehmen wir die Vektoren in die Basis auf, die den Stufenspalten entsprechen. Eine mögliche Basis von $U$ ist also $\{3x,\ 4x^2 + 2x + 2\}$.

> [!warning] Anmerkung zur Quelle
> Im Skript steht die (offenbar verkürzte) Schreibweise „$V = \{p \mid p$ ist Polynom von Grad $\leq p\}$"; gemeint ist der Raum der Polynome vom Grad $\leq 2$ (mit Basis $(1, x, x^2)$).
