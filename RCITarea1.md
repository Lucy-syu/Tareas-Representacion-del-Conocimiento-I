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

Tenemos que Blanco $\equiv$ Verdadero y que Verde $\equiv$ Falso. Tal y como dice el enunciado, la condición B equivale a la puerta lógica NAND, también conocida como barra de Sheffer ($\uparrow$).
Para cada propiedad, identificaremos a qué puerta lógica/conectivo lógico equivale y demostraremos que NAND permite generarlo.

- **Apartados B1, B3, B5, B7 y B9: Lucía y Sergio.**
- **Apartados B2, B4, B6, B8 y B10: Marco y Francisco.**

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