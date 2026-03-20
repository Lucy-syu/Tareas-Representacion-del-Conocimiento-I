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

Holaaaaa, prueba.

Ejemplo tabla de verdad:

```{=latex}
\begin{center}
\begin{tabular}{c|c|c|c|c|c|c|c}
\toprule
$p$ & $q$ & $r$ & $q \lor r$ & $C_1 \rightarrow C_4$ & $p \land \neg q$ & $C_6 \rightarrow C_3$ & A \\
\midrule
1 & 1 & 1 & 1 & 1 & 0 & 1 & 1 \\
1 & 1 & 0 & 1 & 1 & 0 & 1 & 1 \\
1 & 0 & 1 & 1 & 1 & 1 & 1 & 1 \\
1 & 0 & 0 & 0 & 0 & 1 & 0 & 0 \\
0 & 1 & 1 & 1 & 1 & 0 & 1 & 1 \\
0 & 1 & 0 & 1 & 1 & 0 & 1 & 1 \\
0 & 0 & 1 & 1 & 1 & 0 & 1 & 1 \\
0 & 0 & 0 & 0 & 1 & 0 & 1 & 1 \\
\bottomrule
\end{tabular}
\end{center}
```