---
title: "Representación del Conocimiento I"
subtitle: "Ejercicio hortícola"
author: 
  - "Lucía Cabrera Luque"
  - "Marco Antonio Muñoz Gentile"
  - "Sergio García Mesa"
  - "Francisco Navarta Carvajal"
date: "2026-03-20"
output:
  pdf_document:
    extra_dependencies: ["booktabs"]
  html_document: default
---

Tenemos que Blanco $\equiv$ Verdadero y que Verde $\equiv$ Falso. Tal y como dice el enunciado, la condición B equivale a la puerta lógica NAND, también conocida como barra de Sheffer ($\uparrow$). Para cada propiedad, identificaremos a qué puerta lógica/conectivo lógico equivale y demostraremos que NAND permite generarlo.

-   **Apartados B1, B3, B5, B7 y B9: Lucía y Sergio.**
-   **Apartados B2, B4, B6, B8 y B10: Marco y Francisco.**

## B1

Esta propiedad equivale a la puerta lógica NOT/conectivo lógico $\neg$.

```{=latex}
\begin{center}
\begin{tabular}{c|c}
\toprule
$A$ & $\neg A$ \\
\midrule
1 & 0 \\
0 & 1 \\
\bottomrule
\end{tabular}
\end{center}
```

$$\neg A \equiv A \uparrow A$$

## B2

Esta propiedad equivale a la puerta lógica AND/conectivo lógico $\wedge$.

```{=latex}
\begin{center}
\begin{tabular}{c|c|c|c}
\toprule
$A$ & $B$ & $A \uparrow B$ & $A \land B$ \\
\midrule
1 & 1 & 0 & 1 \\
1 & 0 & 1 & 0 \\
0 & 1 & 1 & 0 \\
0 & 0 & 1 & 0 \\
\bottomrule
\end{tabular}
\end{center}
```

$$A \land B \equiv (A \uparrow B) \uparrow (A \uparrow B)$$

## B3

Esta propiedad equivale a la puerta lógica OR/conectivo lógico $\lor$.

```{=latex}
\begin{center}
\begin{tabular}{c|c|c|c|c}
\toprule
$A$ & $B$ & $A \uparrow A$ & $B \uparrow B$ & $A \lor B$ \\
\midrule
1 & 1 & 0 & 0 & 1 \\
1 & 0 & 0 & 1 & 1 \\
0 & 1 & 1 & 0 & 1 \\
0 & 0 & 1 & 1 & 0 \\ 
\bottomrule
\end{tabular}
\end{center}
```

$$A \lor B \equiv (A \uparrow A) \uparrow (B \uparrow B)$$

## B4

Esta propiedad equivale al conectivo lógico correspondiente a la implicacion $\to$, lo cual equivale en puertas lógicas $\neg A \lor B$.

```{=latex}
\begin{center}
\begin{tabular}{c|c|c|c|c}
\toprule
$A$ & $B$ & $A \uparrow A$ & $(A \uparrow A) \uparrow B$ & $A \to B$ \\
\midrule
1 & 1 & 0 & 1 & 1 \\
1 & 0 & 0 & 0 & 0 \\
0 & 1 & 1 & 1 & 1 \\
0 & 0 & 1 & 1 & 1 \\
\bottomrule
\end{tabular}
\end{center}
```

$$A \to B \equiv (A \uparrow A) \uparrow B$$

## B5

Esta propiedad equivale a la puerta lógica XNOR/conectivo lógico $\leftrightarrow$.

```{=latex}
\begin{center}
\begin{tabular}{c|c|c|c|c|c|c}
\toprule
$A$ & $B$ & $A \uparrow A$ & $B \uparrow B$ & $A \uparrow B$ & $(A \uparrow A) \uparrow (B \uparrow B)$ & $A \leftrightarrow B$ \\
\midrule
1 & 1 & 0 & 0 & 0 & 1 & 1 \\
1 & 0 & 0 & 1 & 1 & 1 & 0 \\
0 & 1 & 1 & 0 & 1 & 1 & 0 \\
0 & 0 & 1 & 1 & 1 & 0 & 1 \\ 
\bottomrule
\end{tabular}
\end{center}
```

$$A \leftrightarrow B \equiv (((A \uparrow A) \uparrow (B \uparrow B)) \uparrow (A \uparrow B)) \uparrow (((A \uparrow A) \uparrow (B \uparrow B)) \uparrow (A \uparrow B))$$

## B6

Esta propiedad equivale a la puerta lógica XOR/conectivo lógico $\neg (A \leftrightarrow B)$

```{=latex}
\begin{center}
\begin{tabular}{c|c|c|c|c}
\toprule
$A$ & $B$ & $A \leftrightarrow B$ & $(A \leftrightarrow B) \uparrow (A \leftrightarrow B)$ & $A \oplus B$ \\
\midrule
1 & 1 & 1 & 0 & 0 \\
1 & 0 & 0 & 1 & 1 \\
0 & 1 & 0 & 1 & 1 \\
0 & 0 & 1 & 0 & 0 \\
\bottomrule
\end{tabular}
\end{center}
```

$$A \oplus B \equiv (A \uparrow (A \uparrow B)) \uparrow (B \uparrow (A \uparrow B))$$

## B7

Esta propiedad equivale a la negación de la implicación, que se representa como $A \not\to B$, lo cual equivale a $\neg(A \rightarrow B)$.

```{=latex}
\begin{center}
\begin{tabular}{c|c|c|c|c}
\toprule
$A$ & $B$ & $B \uparrow B$ & $A \uparrow (B \uparrow B)$ & $A \not\to B$ \\
\midrule
1 & 1 & 0 & 1 & 0 \\
1 & 0 & 1 & 0 & 1 \\
0 & 1 & 0 & 1 & 0 \\
0 & 0 & 1 & 1 & 0 \\ 
\bottomrule
\end{tabular}
\end{center}
```

$$A \not\to B \equiv \neg(A \rightarrow B) \equiv ((A \uparrow (B \uparrow B))) \uparrow ((A \uparrow (B \uparrow B)))$$

## B8

Esta propiedad equivale a la puerta lógica NOR, que se representa como $\neg (A \lor B)$

```{=latex}
\begin{center}
\begin{tabular}{c|c|c|c|c|c}
\toprule
$A$ & $B$ & $A \uparrow A$ & $B \uparrow B$ & $(A \uparrow A) \uparrow (B \uparrow B)$ & $\neg (A \lor B)$ \\
\midrule
1 & 1 & 0 & 0 & 1 & 0 \\
1 & 0 & 0 & 1 & 1 & 0 \\
0 & 1 & 1 & 0 & 1 & 0 \\
0 & 0 & 1 & 1 & 0 & 1 \\
\bottomrule
\end{tabular}
\end{center}
```

$$\neg (A \lor B) \equiv \big((A \uparrow A) \uparrow (B \uparrow B)\big) \uparrow \big((A \uparrow A) \uparrow (B \uparrow B)\big)$$

## B9

Esta propiedad equivale a Verum ($\top$).

```{=latex}
\begin{center}
\begin{tabular}{c|c|c}
\toprule
$A$ & $A \uparrow A$ & $\top$ \\
\midrule
1 & 0 & 1 \\
0 & 1 & 1 \\
\bottomrule
\end{tabular}
\end{center}
```

$$\top \equiv A \uparrow (A \uparrow A)$$

## B10

Esta propiedad equivale a Falsum ($\bot$).

```{=latex}
\begin{center}
\begin{tabular}{c|c|c|c}
\toprule
$A$ & $A \uparrow A$ & $A \uparrow (A \uparrow A)$ & $\bot$ \\
\midrule
1 & 0 & 1 & 0 \\
0 & 1 & 1 & 0 \\
\bottomrule
\end{tabular}
\end{center}
```

$$\bot \equiv \big(A \uparrow (A \uparrow A)\big) \uparrow \big(A \uparrow (A \uparrow A)\big)$$

---

Enunciado:

Sabiendo que hay entre 200 y 300, y no hay dos que tengan siempre el mismo color, ¿cuántas habichuelas "mágicas" encontramos en nuestra huerta?

En el pdf se señala que estamos ante un conjunto booleano, la principal caracteristica de un conjunto booleano es que tiene $2^n$ elementos, siendo `n` un número entero.
Como el número debe estar entre 200 y 300 habichuelas deben de ser 256 para que `n` sea un número entero.
