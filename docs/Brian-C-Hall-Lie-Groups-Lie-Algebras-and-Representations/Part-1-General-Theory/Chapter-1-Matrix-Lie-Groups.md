---
export_on_save:
  html: true
---

# Chapter 1
# Matrix Lie Groups

## Problem 1

Let \([ \cdot , \cdot ]_{n,k}\) be the symmetric bilinear form on \(\mathbb{R}^{n+k}\) defined in (1.5). Let \( g \) be the \((n + k) \times (n + k)\) diagonal matrix with the first \( n \) diagonal entries equal to one and the last \( k \) diagonal entries equal to minus one:

$$
g = \begin{pmatrix}
I_n & 0 \\
0 & -I_k
\end{pmatrix}.
$$

Show that for all \( x, y \in \mathbb{R}^{n+k} \),

$$
[ x, y ]_{n,k} = \langle x, g y \rangle.
$$

Show that a \((n + k) \times (n + k)\) real matrix \( A \) belongs to \( O(n; k) \) if and only if

$$
g A^T g = A^{-1}.
$$