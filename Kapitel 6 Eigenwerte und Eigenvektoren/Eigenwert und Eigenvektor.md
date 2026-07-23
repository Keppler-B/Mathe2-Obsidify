---
tags: [kapitel-6, definition]
quelle: Skript S. 89
aliases: [Eigenwert, Eigenvektor, Eigenraum, Eig]
---
# Eigenwert und Eigenvektor

> Kapitel 6 · Eigenwerte und Eigenvektoren — atomare Kern-Definition. Zurück zum [[Inhaltsverzeichnis]].
> Verwendet in: [[Eigenwerte, Eigenvektoren, Eigenräume]], [[Diagonalisierbarkeit und Spektralsatz]].
> Grundlage: [[Matrix]], [[Vektorraum]], [[Determinante]].

## Definition 6.1 (Eigenwert, Eigenvektor, Eigenraum)

Sei $A \in M_n(K)$ eine quadratische [[Matrix]] über dem Körper $K$.

Ein Skalar $\lambda \in K$ heißt **Eigenwert** von $A$, wenn es einen Vektor $\mathcal{O} \neq x \in K^n$ gibt (also einen vom Nullvektor verschiedenen Vektor des [[Vektorraum|Vektorraums]] $K^n$) mit

$$Ax = \lambda x.$$

Anschaulich bedeutet das: Der Vektor $x$ wird von $A$ nur um den Faktor $\lambda$ gestreckt (skaliert), sonst nicht verändert.

Jeder solche Vektor $x$ heißt dann ein zu $\lambda$ zugehöriger **Eigenvektor** von $A$, und

$$\operatorname{Eig}(\lambda) = \operatorname{Eig}_A(\lambda) = \{x \in K^n \mid Ax = \lambda x\}$$

(also alle zu $\lambda$ gehörenden Eigenvektoren zusammen mit dem Nullvektor $\mathcal{O}$) heißt der $\lambda$ zugeordnete **Eigenraum**.

> [!info] Nichttriviale Lösung
> „Nichttrivial" bedeutet: ungleich dem Nullvektor $\mathcal{O}$, der stets eine Lösung der Gleichung $Ax = \lambda x$ ist (er wird aber nicht als Eigenvektor bezeichnet).
