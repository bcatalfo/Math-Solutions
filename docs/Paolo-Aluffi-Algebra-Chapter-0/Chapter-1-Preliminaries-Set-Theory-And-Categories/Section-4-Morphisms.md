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
  A \arrow[r, "f"] & B \arrow[r,"g"] & C \arrow[r, "h"] & D \arrow[r,"i"] & E,
\end{tikzcd}
\end{document}
```

then one can compose them in several ways, for example:

$$
(ih)gf, \quad (i(hg))f, \quad i((hg)f), \quad \text{etc.}
$$

so that at every step one is only composing two morphisms. Prove that the result of any such nested composition is independent of the placement of the parentheses. 
(Hint: Use induction on $n$ to show that any such choice for $f_nf_{n-1}\cdots f_{1}$ equals

$$
((\cdots((f_nf_{n-1})f_{n-2})\cdots)f_1).
$$

Carefully working out the case $n=5$ is helpful.) $[\S4.1, \S\textrm{II}.1.3]$

**Solution**

Let $S(n)$ be the following proposition. 

$f_nf_{n-1}f_{n-2}\cdots f_1$. $f$ is independent of the placement of the parentheses.

Proceed by induction.

$S(0)$ is just the associative law.

Assume $S(n)$. NTS $S(n+1)$. We know that

$$
f = gh
$$

where $g$ is a composition of 

$$
f_n\cdots f_k
$$

and $h$ is a composition of

$$
f_{k-1} \cdots f_1
$$

By $S(n)$

$$
f = ((\cdots((f_nf_{n-1})f_{n-2})\cdots)f_{k}) (f_{k-1}(f_{k-2}(f_{k-3}(\cdots )f_1),
$$

apply the associative law to get


$$
f = (((\cdots((f_nf_{n-1})f_{n-2})\cdots)f_{k})f_{k-1})(f_{k-2}(f_{k-3}(f_{k-4}(\cdots )f_1),
$$

and finally repeat this inductively to get 

$$
f = (( \cdots ((f_nf_{n-1})f_{n-2})\cdots)f_1). \quad \square
$$


---

$\textbf{4.2.} \enspace \triangleright$ In Example 3.3 we have seen how to construct a category from a set endowed with a relation, provided this latter is reflexive and transitive. For what types of relations is the corresponding category a groupoid (cf. Example 4.6)? $[\S 4.1]$