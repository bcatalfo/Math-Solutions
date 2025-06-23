---
export_on_save:
  html: true
---
<style>
.katex-display { overflow: auto hidden }
img { display: block; margin: 0 auto }
.tikz { display: flex; justify-content: center; align-items: center }
</style>

$\textbf{5.2.} \enspace \triangleright$ Prove that $\emptyset$ is the _unique_ initial object in $\mathsf{Set}. \enspace [\S5.1]$

---

$\textbf{5.3.} \enspace \triangleright$ Prove that the final objects are unique up to isomorphism. $[\S5.1]$

---

$\textbf{5.5.} \enspace \triangleright$ What are the final objects in the category considered in $\S 5.3\text{?} \> [\S 5.3]$

**Solution**

Recall that the morphisms in $\S 5.3$ are commutative diagrams

```latex{cmd=true, hide=true, latex_zoom=200%}
\documentclass[tikz]{standalone}
\usetikzlibrary{cd}
\begin{document}
\begin{tikzcd}
Z_1 \arrow[rr,"\sigma"] & & Z_2 \\
& & \\
& A \arrow[uul,"\varphi_1"] \arrow[uur,"\varphi_2",swap] &
\end{tikzcd}
\end{document}
```

---

$\textbf{5.6} \enspace \triangleright$ Consider the category corresponding to endowing (as in Example 3.3) the set $\Z^+$ of positive integers with the _divisibility_ relation. Thus there is exactly one morphism $d \to m$ in this category if and only if $d$ divides $m$ without remainder; there is no morphism between $d$ and $m$ otherwise. Show that this category has products and coproducts. What are their 'conventional' names? $[\S\text{VII}.5.1]$

$$
\\
$$