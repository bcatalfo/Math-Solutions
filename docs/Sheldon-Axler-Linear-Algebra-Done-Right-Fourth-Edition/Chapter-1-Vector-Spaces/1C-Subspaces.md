---
export_on_save:
  html: true
---

<style>
.katex-display { overflow: auto hidden }
</style>

**1** &nbsp; For each of the following subsets of $\mathbf{F}^3$, determine whether it is a subspace of $\mathbf{F}^3$.
(a) &nbsp; $\{ (x_1,x_2,x_3) \in \mathbf{F}^3: x_1 + 2x_2 + 3x_3 = 0 \}$
(b) &nbsp; $\{ (x_1,x_2,x_3) \in \mathbf{F}^3: x_1 + 2x_2 + 3x_3 = 4 \}$
(c) &nbsp; $\{ (x_1,x_2,x_3) \in \mathbf{F}^3:  x_1x_2x_3 = 0 \}$
(d) &nbsp; $\{ (x_1,x_2,x_3) \in \mathbf{F}^3: x_1 = 5x_3 \}$

**Solution**

Recall that three conditions are necessary and sufficient to show that a subset $U$ of a vector space $V$ over a field $\mathbf{F}$ is a subspace:

1. _additive identity_

$$
0 \in U
$$

2. _closed under addition_

$$
u, w \in U \implies u + w \in U
$$

3. _closed under scalar multiplication_

$$
a \in \mathbf{F} \land a \in U \implies au \in U
$$

(a) &nbsp; $U = \{ (x_1,x_2,x_3) \in \mathbf{F}^3: x_1 + 2x_2 + 3x_3 = 0 \}$

Clearly $0 = (0,0,0) \in U$ as $0 + 2 \times 0 + 3 \times 0 = 0$ so 1. _additive identity_ holds.

Let $u = (u_1, u_2, u_3), w = (w_1, w_2, w_3) \in U$. Then

$$
(u_1 + w_1) + 2(u_2 + w_2)  + 3(u_3 + w_3) \\
= (u_1 + 2u_2 + 3u_3) + (w_1 + 2w_2 + 3w_3) = 0 + 0 = 0,
$$

so 2. _closed under addition_ holds.

Let $a \in \mathbf{F}$. Then

$$
(au_1) + 2(au_2) + 3(au_3) = a (u_1 + 2u_2 + 3u_3) = a \cdot 0 = 0,
$$

so $au = (au_1, au_2, au_3) \in U$, so 3. _closed under scalar multiplication_ holds.

We conclude that $U$ is a subspace. $\quad \square$


---

**2** &nbsp; Verify all assertions about subspaces in Example 1.35.

---

**3** &nbsp; Show that the set of differentiable real-valued functions $f$ on the interval $(-4,4)$ such that $f'(-1)=3f(2)$ is a subspace of $\mathbf{R}^{(-4,4)}$.

---

**4** &nbsp; Suppose $b \in \mathbf{R}$. Show that the set of continuous real-valued functions $f$ on the interval $[0,1]$ such that $\int_0^1 f = b$ is a subspace of $\mathbf{R}^{[0,1]}$ if and only if $b=0$.

---

**5** &nbsp; Is $\mathbf{R}^2$ a subspace of the complex vector space $\mathbf{C}^2$?

---

**6** &nbsp; (a) Is $\{(a,b,c) \in \mathbf{R}^3: a^3 = b^3\}$ a subspace of $\mathbf{R}^3$?
(b) Is $\{(a,b,c) \in \mathbf{C}^3: a^3=b^3\}$ a subspace of $\mathbf{C}^3$?

---

**7** &nbsp; Prove or give a counterexample: If $U$ is a nonempty subset of $\mathbf{R}^2$ such that $U$ is closed under addition and under taking additive inverses (meaning $-u \in U$ whenever $u \in U$), then $U$ is not a subspace of $\mathbf{R}^2$.

---

**8** &nbsp; Give an example of a nonempty subset $U$ of $\mathbf{R}^2$ such that $U$ is closed under scalar multiplication, but $U$ is not a subspace of $\mathbf{R}^2$.

---

**9** &nbsp; A function $f: \mathbf{R} \to \mathbf{R}$ is called _periodic_ if there exists a positive number $p$ such that $f(x) = f(x+p)$ for all $x \in \mathbf{R}$. Is the set of periodic functions from $\mathbf{R}$ to $\mathbf{R}$ a subspace of $\mathbf{R}^{\mathbf{R}}$? Explain.

---

**10** &nbsp; Suppose $V_1$ and $V_2$ are subspaces of $V$. Prove that the intersection $V_1 \cap V_2$ is a subspace of $V$.

---

**11** &nbsp; Prove that the intersection of every collection of subspaces of $V$ is a subspace of $V$.

---

**12** &nbsp; Prove that the union of two subspaces of $V$ is a subspace of $V$ if and only if one of the subspaces is contained in the other.

---

**13** &nbsp; Prove that the union of three subspaces of $V$ is a subspace of $V$ if and only if one of the subspaces contains the other two.

_This exercise is surprisingly harder than Exercise 12, possibly because this exercise is not true if we replace $\mathbf{F}$ with a field containing only two elements._

---

**14** &nbsp; Suppose

$$
U = \{(x,-x,2x)\in \mathbf{F}^3: x \in \mathbf{F}\} \quad \text{and} \quad W = \{(x,x,2x) \in \mathbf{F}^3:x \in F\}.
$$

Describe $U + W$ using symbols, and also give a description of $U+W$ that uses no symbols.

---

**15** &nbsp; Suppose $U$ is a subspace of $V$. What is $U + U$?

---

**16** &nbsp; Is the operation of addition on the subspaces of $V$ commutative? In other words, if $U$ and $W$ are subspaces of $V$, is $U + W = W + U$?

---

**17** &nbsp; Is the operation of addition on the subspaces of $V$ associative? In other words, if $V_1$, $V_2$, $V_3$ are subspaces of $V$, is

$$
(V_1 + V_2) + V_3 = V_1 + (V_2 + V_3)?
$$

---

**18** &nbsp; Does this operation of addition on the subspaces of $V$ have an additive identity? Which subspaces have additive inverses?

---

**19** &nbsp; Prove or give a counterexample: If $V_1$, $V_2$, $U$ are subspaces of $V$ such that 

$$
V_1 + U = V_2 + U,
$$

then $V_1 = V_2$.

---

**20** &nbsp; Suppose 

$$
U = \{ (x,x,y,y): \in \mathbf{F}^4: x,y \in \mathbf{F} \}.
$$

Find a subspace $W$ of $\mathbf{F}^4$ such that $\mathbf{F}^4 = U \oplus W$.

---

**21** &nbsp; Suppose

$$
U = \{ (x,y,x+y,x-y,2x): \in \mathbf{F}^5: x,y \in \mathbf{F} \}.
$$

Find a subspace $W$ of $\mathbf{F}^5$ such that $\mathbf{F}^5 = U \oplus W$.

---

**22** &nbsp; Suppose

$$
U = \{(x,y,x+y,x-y,2x)\in \mathbf{F}^5: x,y\in\mathbf{F}\}.
$$

Find three subspaces $W_1$, $W_2$, $W_3$ of $\mathbf{F}^5$, none of which equals $\{0\}$, such that $\mathbf{F}^5 = U \oplus W_1 \oplus W_2 \oplus W_3$.

---

**23** &nbsp; Prove or give a counterexample: If $V_1$, $V_2$, $U$ are subspaces of $V$ such that

$$
V = V_1 \oplus U \quad \text{and} \quad V = V_2 \oplus U,
$$

then $V_1 = V_2$.

_Hint: When trying to discover whether a conjecture in linear algebra is true or false, it is often useful to start by experimenting in $\mathbf{F}^2$._

---

**24** &nbsp; A function $f: \mathbf{R} \to \mathbf{R}$ is called _even_ if

$$
f(-x) = f(x)
$$

for all $x \in \mathbf{R}$. A function $f: \mathbf{R} \to \mathbf{R}$ is called _odd_ if

$$
f(-x) = -f(x)
$$

for all $x \in \mathbf{R}$. Let $V_\text{e}$ denote the set of real-valued even functions on $\mathbf{R}$ and let $V_\text{o}$ denote the set of real-valued odd functions on $\mathbf{R}$. Show that $\mathbf{R}^\mathbf{R} = V_\text{e} \oplus V_\text{o}$.


$$
\\
$$