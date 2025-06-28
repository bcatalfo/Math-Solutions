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

As the hint suggests, let's start by working out the case $n=5$. We need to show that any arrangement of the parentheses can be rearranged to

$$
F = (((f_5f_4)f_3)f_2)f_1.
$$

Here is the basic strategy: first we want to isolate $f_5$, then for the rest of it isolate $f_4$ and shift, so on and so forth, let me give an example.

Say you start with 

$$
F' = (f_5f_4)(f_3(f_2f_1)),
$$

then by writing 

$$
F_3 = f_3(f_2f_1)
$$

we can subsitute to get 

$$
F' = (f_5f_4)F_3
$$

and then use the associative property to get

$$
F' = f_5(f_4F_3).
$$

Next we can look at $F_3$ and rewrite it as 

$$
F_3 = f_3F_2, \enspace F_2 = f_2f_1
$$

so we can plug back into $F'$ to get 

$$
F' = (f_5f_4)(f_3F_2),
$$

and if we let 

$$
F_5 = f_5f_4,
$$

then we can rewrite $F'$ as 

$$
F' = F_5(f_3F_2),
$$

apply the associative property 

$$
F' = (F_5f_3)F_2,
$$

and subsitute to get 

$$
F' = ((f_5f_4)f_3)f_2f_1,
$$

repeating the process one more time will give 

$$
F' = (((f_5f_4)f_3)f_2)f_1.
$$


---

$\textbf{4.2.} \enspace \triangleright$ In Example 3.3 we have seen how to construct a category from a set endowed with a relation, provided this latter is reflexive and transitive. For what types of relations is the corresponding category a groupoid (cf. Example 4.6)? $[\S 4.1]$