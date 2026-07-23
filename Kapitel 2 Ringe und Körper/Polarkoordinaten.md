---
tags: [kapitel-2, thema, definition, beispiel]
quelle: Skript S. 33–36
aliases: [Polarform, Eulersche Formel, Einheitswurzeln]
---
# Polarkoordinaten

> Kapitel 2 · Ringe und Körper — Unterabschnitt von [[Der Körper der komplexen Zahlen]]: zweite Darstellungsform komplexer Zahlen. Zurück zum [[Inhaltsverzeichnis]].
> Voriges Thema: [[Der Körper der komplexen Zahlen]]
> Grundlage: [[Der Körper der komplexen Zahlen]].

Zur Darstellung der komplexen Zahlen haben wir bisher die **Normalform** (oder **kartesische Form**) mit Real- und Imaginärteil verwendet und ihre Veranschaulichung in der Gaußschen Zahlenebene kennengelernt. Eine weitere Darstellung benutzt die sogenannten **Polarkoordinaten**. Damit wird jeder Punkt der Ebene unter Angabe seines Abstands zum Ursprung (also dem Betrag) und eines Winkels (der „Richtung") beschrieben. Die Darstellung mittels Polarkoordinaten erleichtert Rechnungen, insbesondere Multiplikation, Division, Potenzieren und Wurzelziehen von komplexen Zahlen.

## Bemerkung 2.25 (Darstellung mittels Polarkoordinaten)

Zu jedem $z = x + iy \in \mathbb{C}$ gibt es eine eindeutig bestimmte Zahl $r \geq 0 \in \mathbb{R}$ und einen Winkel $\varphi \in \mathbb{R}$ (nicht eindeutig, Winkel im Bogenmaß, wird auch **Argument** genannt) mit
$$z = r \cdot (\cos \varphi + i \sin \varphi) \qquad \text{(\textbf{Polarkoordinatendarstellung} von } z),$$
und zwar ist
$$r = |z| = \sqrt{x^2 + y^2},$$
und es gilt (vgl. Skizze)
$$\frac{x}{r} = \cos \varphi, \quad \frac{y}{r} = \sin \varphi, \quad \text{d. h. } x = r \cdot \cos \varphi, \; y = r \cdot \sin \varphi.$$

> [!info] Skizze (Polarkoordinaten)
> Im Koordinatensystem mit reeller Achse $\mathbb{R}$ (waagrecht) und imaginärer Achse $i\mathbb{R}$ (senkrecht) zeigt ein Zeiger der Länge $r$ vom Ursprung zum Punkt $z = x + iy$. Der Winkel $\varphi$ zwischen der positiven reellen Achse und diesem Zeiger ist das **Argument**. Es entsteht ein rechtwinkliges Dreieck mit Ankathete $x = r\cos\varphi$ (waagrecht) und Gegenkathete $y = r\sin\varphi$ (senkrecht) sowie Hypotenuse $r = |z|$.

und damit
$$z = x + iy = (r \cdot \cos \varphi) + i(r \cdot \sin \varphi) = r \cdot (\cos \varphi + i \sin \varphi).$$

Aus den **Additionstheoremen**[^additions] für $\sin$ und $\cos$ folgt für $z = r \cdot (\cos \varphi + i \sin \varphi)$, $z' = r' \cdot (\cos \varphi' + i \sin \varphi')$:
$$z \cdot z' = r \cdot r' \cdot \big(\cos(\varphi + \varphi') + i \cdot \sin(\varphi + \varphi')\big) \quad \text{(Beträge multipliziert, Winkel addiert)}$$
$$z^2 = r^2 \cdot \big(\cos(2\varphi) + i \cdot \sin(2\varphi)\big)$$
$$\pm \sqrt{z} = \pm \sqrt{r} \cdot \left(\cos\left(\tfrac{\varphi}{2}\right) + i \cdot \sin\left(\tfrac{\varphi}{2}\right)\right)$$
usw.

[^additions]: vgl. *Mathematik 1*: $\sin(x + y) = \sin x \cos y + \cos x \sin y$, $\cos(x + y) = \cos x \cos y - \sin x \sin y$.

## Beispiel 2.26

**(a)** $z_1 = 1 = 1 + 0i$. Hier ist $r_1 = 1$, $\varphi_1 = 0$.

**(b)** $z_2 = i = 0 + 1i$. Hier ist $r_2 = 1$, $\varphi_2 = \tfrac{\pi}{2}$.

**(c)** $z_3 = 1 + i$. Hier ist $r_3 = \sqrt{2}$, $\varphi_3 = \tfrac{\pi}{4}$.

## Schreibweise 2.27 (Eulersche Formel)

Wir definieren
$$e^{i\varphi} := \cos \varphi + i \sin \varphi.$$
Damit lässt sich die komplexe Zahl $z = r \cdot (\cos \varphi + i \sin \varphi)$ schreiben als
$$z = r \cdot e^{i\varphi}.$$

Diese Schreibweise beruht auf der Konvergenz der **Exponentialreihe**. Wie in *Mathematik 1* gezeigt wird, konvergiert die Potenzreihe $\sum_{k=0}^{\infty} \tfrac{x^k}{k!}$ für alle $x \in \mathbb{R}$, daher lässt sich auf ganz $\mathbb{R}$ die Abbildung $\exp : \mathbb{R} \to \mathbb{R}$ als $\exp(x) = \sum_{k=0}^{\infty} \tfrac{x^k}{k!}$ definieren. Wegen $\exp(1) = e$ (die **Eulersche Zahl**) schreibt man auch $\exp(x) = e^x$. Man kann für alle $z \in \mathbb{C}$ ebenfalls die Konvergenz der Reihe $\sum_{k=0}^{\infty} \tfrac{z^k}{k!}$ zeigen und darüber auf ganz $\mathbb{C}$ die Funktion $\exp(z) =: e^z$ definieren. Es gilt also $e^{i\varphi} = \sum_{k=0}^{\infty} \tfrac{(i\varphi)^k}{k!}$. Wegen $i^0 = 1$, $i^1 = i$, $i^3 = -i$, $i^4 = 1 = i^0$ lässt sich diese Reihe folgendermaßen aufteilen:
$$\underbrace{\sum_{k=0}^{\infty} \frac{(i\varphi)^k}{k!}}_{e^{i\varphi}} = \underbrace{\sum_{k=0}^{\infty} (-1)^k \cdot \frac{\varphi^{2k}}{(2k)!}}_{\cos \varphi} + i \cdot \underbrace{\sum_{k=0}^{\infty} (-1)^k \cdot \frac{\varphi^{2k+1}}{(2k+1)!}}_{i \sin \varphi}.$$

## Beispiel/Bemerkung 2.28

**(a)** $e^{i0}$ ist die Zahl, die auf dem Kreis um den Nullpunkt mit Radius $1$ liegt und den Winkel $0^\circ$ mit der positiven $x$-Achse einschließt, also $1$.

**(b)** $e^{i\pi} = -1$. Es gilt also
$$e^{i\pi} + 1 = 0.$$
Diese Gleichung wird auch als die „schönste Formel der Mathematik" bezeichnet, da sie einen einfachen Zusammenhang zwischen fünf wichtigen Konstanten (der Eulerschen Zahl $e$, der Kreiszahl $\pi$, der imaginären Einheit $i$, der reellen Einheit $1$, der Null $0$) herstellt.

**(c)** Wo liegen $2e^{2\pi i}$ und $3e^{i\pi/2}$ in der Gaußschen Zahlenebene? Die Zahl $2e^{2\pi i}$ entspricht dem Punkt $(2 \mid 0)$, die Zahl $3e^{i\pi/2}$ dem Punkt $(0 \mid 3)$.

**(d)** Für $z = r \cdot e^{i\varphi}$, $z' = r' \cdot e^{i\varphi'} \in \mathbb{C}$ ist
$$z \cdot z' = r \cdot r' \cdot e^{i(\varphi + \varphi')} \quad \text{(Beträge werden multipliziert, Winkel werden addiert)}$$
$$\frac{z}{z'} = \frac{r}{r'} \cdot e^{i(\varphi - \varphi')} \quad \text{(falls } z' \neq 0)$$
$$z^n = r^n \cdot e^{n \cdot i\varphi} \quad \text{für } n \in \mathbb{N}.$$

Die Polarkoordinatendarstellung erleichtert also den Aufwand beim Rechnen mit komplexen Zahlen enorm (im Vergleich zur Darstellung in der kartesischen Form, etwa bei Quotienten von komplexen Zahlen).

**(e) Die $n$-ten Einheitswurzeln:**
In $\mathbb{R}$ besitzt die Gleichung $x^n = 1$ (mit $n \in \mathbb{N}$) *eine* Lösung ($x = 1$), falls $n$ ungerade ist, und *zwei* Lösungen ($x_1 = 1$, $x_2 = -1$), falls $n$ gerade ist.
In $\mathbb{C}$ gilt: Die Gleichung
$$z^n = 1$$
besitzt $n$ verschiedene Lösungen $z_0, z_1, \dots, z_{n-1}$, nämlich
$$z_k = e^{\frac{2\pi i}{n} \cdot k} \quad (k \in \{0, 1, \dots, n-1\}),$$
diese werden als die **$n$-ten Einheitswurzeln** bezeichnet.

Wir rechnen nach: Für jedes $z_k$ muss $(z_k)^n = 1$ gelten. Tatsächlich ist
$$(z_k)^n = \left(e^{\frac{2\pi i}{n} \cdot k}\right)^n = e^{2\pi i k} = (\underbrace{e^{2\pi i}}_{= 1})^k = 1.$$

Für $n = 3$ erhält man beispielsweise die dritten Einheitswurzeln (also die komplexen Lösungen der Gleichung $z^3 = 1$) als
$$z_0 = e^{\frac{2\pi i}{3} \cdot 0} = e^0 = 1, \qquad z_1 = e^{\frac{2\pi i}{3} \cdot 1}, \qquad z_2 = e^{\frac{2\pi i}{3} \cdot 2}.$$
