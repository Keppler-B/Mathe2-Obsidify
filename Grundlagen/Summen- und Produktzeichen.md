---
tags: [grundlagen, wiederholung, referenz]
quelle: Wiederholung aus Mathematik 1
---
# Summen- und Produktzeichen

> Wiederholung aus *Mathematik 1*. Das Summenzeichen $\sum$ taucht in vielen zentralen Formeln des Skripts auf.
> Zurück: [[Übersicht|Grundlagen]]

## Summenzeichen $\sum$

$$\sum_{i=1}^{n} a_i := a_1 + a_2 + \dots + a_n.$$

$i$ heißt **Laufindex**, $1$ ist die untere, $n$ die obere Grenze. Der Index ist „gebunden" (der Name ist beliebig: $\sum_i a_i = \sum_k a_k$).

**Rechenregeln:**
$$\sum_{i=1}^n (a_i + b_i) = \sum_{i=1}^n a_i + \sum_{i=1}^n b_i, \qquad \sum_{i=1}^n \lambda a_i = \lambda \sum_{i=1}^n a_i.$$

## Produktzeichen $\prod$

$$\prod_{i=1}^{n} a_i := a_1 \cdot a_2 \cdots a_n. \qquad \text{Speziell: } n! = \prod_{i=1}^{n} i.$$

## Wo im Skript verwendet

- **[[Matrix|Matrixprodukt]]**: $\;(AB)_{ik} = \sum_{j=1}^{n} a_{ij} b_{jk}$
- **[[Determinante]]** (Laplace): $\;\det(A) = \sum_{j=1}^{n} (-1)^{1+j} a_{1j} \det(A_{1j})$
- **[[Norm und Skalarprodukt|Norm]]**: $\;\|v\| = \left(\sum_{i=1}^{n} v_i^2\right)^{1/2}$, &nbsp; Skalarprodukt $\;(v \mid w) = \sum_i v_i w_i$
- **Binomialsatz** ([[Ringe]]): $\;(a+b)^n = \sum_{k=0}^{n} \binom{n}{k} a^k b^{n-k}$
- **[[Linearkombinationen und lineare (Un-)Abhängigkeit|Linearkombination]]**: $\;\sum_{i=1}^{k} \lambda_i v_i$
