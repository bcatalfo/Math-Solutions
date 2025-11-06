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

It is trivial that $\emptyset$ is an initial object in $\mathsf{Set}$, because for any set $S$, there is only one function $f: \emptyset \to S$.

Let $I$ be an initial object in $\mathsf{Set}$. By definition,

$$
\forall A \in \text{Obj}(\mathsf{Set}), \quad \text{Hom}_{\mathsf{Set}}(I, A) \> \text{is a singleton}.
$$

Of course, the objects of $\mathsf{Set}$ are just sets and their morphisms are just ordinary set-functions. So we know that for all sets $A$, there is only one function $f: I \to A$. In particular, there is only one function $f: I \to \{0,1\}$.

We NTS that $I = \emptyset$. Let $i \in I$. Proceed by contradiction.

Define $f: I \to \{0,1\}$ by

$$
\forall x \in I, \quad f(x) = 0,
$$

and similarly define $f': I \to \{0,1\}$ by 

$$
\forall x \in I, \quad f(x) = 1.
$$

Since there should be only one function mapping $I$ to $\{0,1\}$, we should have $f = f'$. However $f(i) = 0 \neq 1 = f'(i)$, a contradiction. $\> \square$

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