---
export_on_save:
  html: true
---

<style>
.katex-display { overflow: auto hidden }
</style>

**1** &nbsp; Prove that $-(-v) = v$ for every $v \in V$.

---

**2** &nbsp; Suppose $a \in \mathbf{F}$, $v \in V$, and $av = 0$. Prove that $a = 0$ or $v = 0$.

---

**3** &nbsp; Suppose $v,w \in V$. Explain why there exists a unique $x \in V$ such that $v + 3x = w$.

---

**4** &nbsp; The empty set is not a vector space. The empty set fails to satisft only one of the reqirements listed in the definition of a vector space (1.20). Which one?

---

**5** &nbsp; Show that in the definition of a vector space (1.20), the additive inverse condition can be replaced with the condition that

$$
0v = 0 \text{ for all } v \in V.
$$

Here the $0$ on the left side is the number $0$, and the $0$ on the right side is the additive identity of $V$.

_The phrase a "condition can be replaced" in a definition means that the collection of objects satisfying the definition is unchanged if the original condition is replaced with the new condition._

---

**6** &nbsp; Let $\infty$ and $-\infty$ denote two distinct objects, neither of which is in $\mathbf{R}$. Define an addition and scalar multiplication on $\mathbf{R} \cup \{\infty, -\infty\}$ as you could guess from the notation. Specifically, the sum and product of two real numbers is as usual, and for $t \in \mathbf{R}$ define

$$
t \infty =
\begin{cases}
    -\infty &\text{if } t < 0, \\
    0 &\text{if } t = 0, \\
    \infty &\text{if } t > 0, \\
\end{cases}
\quad
t(-\infty) =
\begin{cases}
    \infty &\text{if } t < 0, \\
    0 &\text{if } t = 0, \\
    -\infty &\text{if } t > 0,
\end{cases}
$$

and

$$
t + \infty = \infty + t = \infty + \infty = \infty, \\
t + (-\infty) = (\infty) + t = (-\infty) + (-\infty) = -\infty, \\
\infty + (-\infty) = (-\infty) + \infty = 0.
$$

With these operations of addition and scalar multiplication, is $\mathbf{R} \cup \{\infty, -\infty\}$ a vector space over $\mathbf{R}$? Explain.

---

**7** &nbsp; Suppose $S$ is a nonempty set. Let $V^S$ denote the set of functions from $S$ to $V$. Define a natural addition and scalar multiplication on $V^S$, and show that $V^S$ is a vector space with these definitions.

---

**8** &nbsp; Suppose $V$ is a real vector space.

- The _complexification_ of $V$, denoted by $V_{\mathbf{C}}$, equals $V \times V$. An element of $V_{\mathbf{C}}$ is an ordered pair $(u,v)$, where $u,v \in V$, but we write this as $u+iv$.
- Addition on $V_{\mathbf{C}}$ is defined by
  $$
  (u_1 + iv_1) + (u_2 + iv_2) = (u_1 + u_2) + i (v_1+v_2)
  $$
  for all $u_1, v_1, u_2, v_2 \in V$.
- Complex scalar multiplication on $V_{\mathbf{C}}$ is defined by
  $$
  (a+bi)(u+iv) = (au - bv) + i(av+bu)
  $$
  for all $a,b\in \mathbf{R}$ and all $u,v \in V$.

Prove that with the definitions of addition and scalar multiplication as above, $V_{\mathbf{C}}$ is a complex vector space.
