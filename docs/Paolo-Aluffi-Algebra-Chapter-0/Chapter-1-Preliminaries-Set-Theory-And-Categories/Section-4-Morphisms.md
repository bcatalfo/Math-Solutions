---
export_on_save:
  html: true
---
<style>
.katex-display { overflow: auto hidden }
img { display: block; margin: 0 auto }
.tikz { display: flex; justify-content: center; align-items: center }
</style>

$\textbf{4.1.} \enspace \triangleright$ Composition is defined for _two_ morphisms. If more than two morphisms are given, e.g.,

```latex {cmd=true, hide=true, latex_zoom=200%}
\documentclass[tikz]{standalone}
\usetikzlibrary{cd}
\begin{document}
\begin{tikzcd}
  A \arrow[r] & B
\end{tikzcd}
\end{document}
```