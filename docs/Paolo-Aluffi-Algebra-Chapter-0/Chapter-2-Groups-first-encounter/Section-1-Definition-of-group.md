---
export_on_save:
  html: true
---
<style>
.katex-display { overflow: auto hidden }
img { display: block; margin: 0 auto }
.tikz { display: flex; justify-content: center; align-items: center }
</style>

$\textbf{1.1.} \enspace \triangleright$ Write a careful proof that every group is the group of isomorphisms of a groupoid. In particular, every group is the group of automorphisms of some object in some category. $[\S2.1]$

---

$\textbf{1.2.} \enspace \triangleright$ Consider the 'set of numbers' listen in $\S1.1$, and decide which are made into groups by conventional operations such as $+$ and $\cdot$. Even if the answer is negative (for example, $(\R,\cdot)$ is not a group), see if variations on the definition of these sets lead to groups (for example, ($\R^*,\cdot$) _is_ a group; c.f. $\S1.4$). $[\S1.2]$

---

$\textbf{1.12.} \enspace \triangleright$ In the group of invertible $2 \times 2$ matrices, consider

$$
g=
\begin{pmatrix}
  0 & -1 \\
  1 & 0
\end{pmatrix}, \quad 
h=
\begin{pmatrix}
  0 & 1 \\
  -1 & -1
\end{pmatrix}.
$$

Verify that $|g| = 4$, $|h| = 3$, and $|gh| = \infty. \enspace [\S1.6]$ 

---

$\textbf{1.13.} \enspace \triangleright$ Give an example showing that $|gh|$ is not necessarily equal to $\text{lcm}(|g|, |h|)$, even if $g$ and $h$ commute. $[\S1.6, 1.14]$

---

$\textbf{1.14.} \enspace \triangleright$ As a counterpoint to Exercise $1.13$, prove that if $g$ and $h$ commute _and_ $\text{gcd}(|g|,|h|) = 1$, then $|gh| = |g| |h|$. (Hint: Let $N = |gh|$; then $g^N = (h^{-1})^N$. What can you say about this element?) $[\S1.6, 1.15, \S\text{IV}.2.5]$

$$
\\
$$