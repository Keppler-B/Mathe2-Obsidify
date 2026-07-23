---
tags: [grundlagen, wiederholung, beweismethode]
quelle: Wiederholung aus Mathematik 1
---
# Vollständige Induktion

> Wiederholung aus *Mathematik 1*. Die im Skript am häufigsten genannte **Beweismethode** für Aussagen über alle $n \in \mathbb{N}$.
> Zurück: [[Übersicht|Grundlagen]]

> [!info] Hinweis
> Das Skript verweist an mehreren Stellen auf „Beweis durch vollständige Induktion", ohne die Methode neu einzuführen. Diese Notiz fasst sie zusammen.

## Das Prinzip

Um eine Aussage $A(n)$ für alle $n \in \mathbb{N}$ (ab einem Startwert $n_0$) zu beweisen, zeigt man:

1. **Induktionsanfang (IA):** $A(n_0)$ ist wahr (oft $n_0 = 0$ oder $1$).
2. **Induktionsschritt (IS):** Aus der **Induktionsvoraussetzung (IV)** „$A(n)$ ist wahr" folgt „$A(n+1)$ ist wahr".

Dann gilt $A(n)$ für **alle** $n \geq n_0$ (Dominoeffekt: der erste Stein fällt, und jeder Stein wirft den nächsten um).

## Wo im Skript verwendet

- $\lvert S_n \rvert = n!$ ([[Die symmetrische Gruppe Sn]], Bemerkung 1.10)
- Division mit Rest — Existenz von $q, r$ ([[Restklassen modulo m als Gruppe]], Vorbemerkung 1.16)
- **Binomialsatz** in kommutativen Ringen ([[Ringe]], Bemerkung 2.4)
- Zusammenhang Dimension/Basis ([[Dimension und Basis]], Satz 3.21) und weitere Sätze in [[Vektorräume (Kapitel 3)|Kapitel 3]]

## Schema (zum Abschreiben)

> **Behauptung:** $A(n)$ gilt für alle $n \geq n_0$.
> **IA:** Zeige $A(n_0)$.
> **IV:** Angenommen, $A(n)$ gilt für ein festes $n \geq n_0$.
> **IS:** Zeige mit der IV, dass dann auch $A(n+1)$ gilt. $\;\blacksquare$
