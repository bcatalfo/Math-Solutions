---
export_on_save:
  html: true
---
<style>
.katex-display { overflow: auto hidden }
img {display: block; margin: 0 auto;}
</style>

# Probability and Stochastics (Graduate Texts in Mathematics 261)
## Erhan Cinlar

## Chapter 1: Measure and Integration

### Exercises

1.9 &nbsp; *Partition generated \(\sigma\)-algebras*.
\(\quad \text{a)} \>\) Let \(\mathcal{C} = \{A, B, C\}\) be a partition of \(E\). List the elements of \(\sigma \mathcal{C}\).
**Solution**
We start off with the elements that are members of all \(\sigma\)-algebras
$$
\emptyset, E
$$
Then we go on to list the elements of \(\mathcal{C}\)
$$
A, B, C
$$
We also need the complements of each of those
$$
B \cup C, A \cup C, A \cup B
$$
where we are using the fact that \(\mathcal{C}\) is a partition to deduce that \(E \setminus A = B \cup C\), etc. I would go on to list their unions but I would just be repeating elements (because \(A \cup B \cup C = E\)). So far what I have is
$$
\sigma \mathcal{C} = \{\emptyset, A, B, C, B \cup C, A \cup C, A \cup B, E\}
$$
This should be correct as it is closed under finite unions and complements, and is the smallest such algebra containing \(\mathcal{C}\). \(\square\)

---

\(\quad \text{b)} \>\) Let \(\mathcal{C}\) be a (countable) partition of \(E\). Show that every element of \(\sigma \mathcal{C}\) is a countable union of elements taken from \(\mathcal{C}\). Hint: Let \(\mathcal{E}\) be the collection of all sets that are countable unions of elements taken from \(\mathcal{C}\). Show that \(\mathcal{E}\) is a \(\sigma\)-algebra, and argue that \(\mathcal{E} = \sigma \mathcal{C}\).
**Solution**
First let's use the fact that \(\mathcal{C}\) is a countable partition of \(E\), so we have \(\mathcal{C} = \{C_i: i \in I\}\), such that \(\bigcup_{i \in I} C_i = E\) and \(i \neq j \implies C_i \cap C_j = \emptyset\). Let \(\mathcal{E}\) be the collection of all sets that are countable unions of elements taken from \(\mathcal{C}\). We proceed by showing that \(\mathcal{E}\) is a \(\sigma\)-algebra.
Let \(A \in \mathcal{E}\), so for some \(J \subseteq I\) we have \(A = \bigcup_{j \in J}C_j\). Let \(B = \bigcup_{k \in I, k \notin J} C_k\). Clearly \(B \in \mathcal{E}\), and propose that \(E \setminus A = B\). Let \(x \in E \setminus A\), since \(x \in E\) and \(\bigcup_{i \in I} C_i = E\) we have some \(i \in I\) such that \(x \in C_i\), and since \(x \notin A\) we have \(i \notin J\), so by our definition of \(B\) we have \(x \in B\). Alternatively, if \(x \in B\) and \(x \notin E \setminus A\) then \(x \in A \cap B = \emptyset\), so we can not have this. We justify \(A \cap B = \emptyset\) as follows: let \(x \in A \cap B\). Then for some \(j \in J\) we have \(x \in C_j\) and for some \(k \notin J\) we have \(x \in C_k\). Since \(\mathcal{C}\) is a partition and \(k \neq j\) we have \(C_j \cap C_k = \emptyset\). Anyways, since \(E \setminus A = B \in \mathcal{E}\) for all \(A \in \mathcal{E}\), we have shown \(\text{1.3 a)}\).
Showing \(\text{1.3 b)}\) is trivial, as the countable union of a countable union is a countable union.
Combining \(\text{1.3 a)}\) and \(\text{1.3 b)}\) shows that \(\mathcal{E}\) is a \(\sigma\)-algebra.
To finish the proof we need to show that \(\mathcal{E} = \sigma \mathcal{C}\). It is obvious that \(\mathcal{E}\) contains \(\mathcal{C}\) and we know that \(\mathcal{E}\) is a \(\sigma\)-algebra so it is obvious that \(\sigma \mathcal{C} \subseteq \mathcal{E}\). Because a \(\sigma\)-algebra is by definition closed under countable unions we must also have \(\mathcal{E} \subseteq \sigma \mathcal{C}\), so \(\mathcal{E} = \sigma \mathcal{C}\). \(\square\)

---

\(\quad \text{c)} \>\) Let \(E = \R\), the set of all real numbers. Let \(\mathcal{C}\) be the collection of all singleton subsets of \(\R\), that is, each element of \(\mathcal{C}\) is a set that consists of exactly one point in \(\R\). Show that every element of \(\sigma \mathcal{C}\) is either a countable set or the complement of a countable set. Incidentally, \(\sigma \mathcal{C}\) is much smaller than \(\mathcal{B}(\R)\); for instance, the interval \((0, 1)\) belongs to the latter but not to the former.
**Solution**
Let \(\mathcal{E}\) be the set of all finite unions of singletons and their complements. We propose that \(\sigma \mathcal{C} = \mathcal{E}\).
First we show that \(\mathcal{E}\) is indeed a \(\sigma\)-algebra. By definition this means showing that
* \(A \in \mathcal{E} \implies \R \setminus A \in \mathcal{E}\)
This is obvious from construction.
* \(A_1, A_2, \dots \in \mathcal{E} \implies \bigcup_{n}A_n \in \mathcal{E}\)
Some examples
$\{1,\frac{1}{2}\} \cup \{\pi\} = \{1, \frac{1}{2}, \pi\}$, which is countable
$\{1,2,3, \dots,\} \cup \{2\}^c = \R$, which is the complement of $\emptyset$
Let $I$ be a countable set and consider $\bigcup_{i \in I}A_i$. Let $I = U \cup V$, where this union is disjoint and if $u \in U$ then $A_u$ is countable and if $v \in V$ then $A_v$ is the complement of a countable set. Then 
$$
\bigcup_{i \in I} A_i = \bigcup_{u \in U} A_u \cup \bigcup_{v \in V} A_v 
$$
Since each $A_v$ is the complement of a countable set we can write $A_v = (B_v)^{c}$ where $B_v$ is a countable subset of $\R$. Plugging in
$$
= \bigcup_{u \in U}A_u \cup \bigcup_{v \in V} (B_v)^{c}
$$
applying DeMorgan's Law
$$
= \bigcup_{u \in U}A_u \cup \left(\bigcap_{v \in V} B_v\right)^{c}
$$
If $V$ is empty then $\bigcap_{v\in V}B_v = \R$ and so the whole union is just the countable $\bigcup_{u \in U} A_u$. Otherwise $\bigcap_{v\in V}B_v$ is countable and so we are left with the union of a countable set and the complement of a countable set, which is the complement of a countable set.

Anyways after having showed that \(\mathcal{E}\) is a \(\sigma\)-algebra the rest of this problem is trivial. \(\mathcal{C} \subset \mathcal{E}\) is obvious by construction, so by the definition of a \(\sigma\)-algebra being generated we have \(\sigma \mathcal{C} \subset \mathcal{E}\). \(\mathcal{E} \subset \sigma \mathcal{C}\) is trivial because \(\sigma\)-algebras are closed under finite unions and complements. $\quad \square$

---

1.10 &nbsp; _Comparisons_. Let $\mathcal{C}$ and $\mathcal{D}$ be two collections of subsets of $E$. Show the following:
$\quad \text{a)} \quad$ If $\mathcal{C} \subset \mathcal{D}$ then $\sigma \mathcal{C} \subset \sigma \mathcal{D}$
$\quad \text{b)} \quad$ If $\mathcal{C} \subset \sigma \mathcal{D}$ then $\sigma C \subset \sigma D$
$\quad \text{c)} \quad$ If $C \subset \sigma \mathcal{D}$ and $\mathcal{D} \subset \sigma \mathcal{C}$, then $\sigma \mathcal{C} = \sigma \mathcal{D}$
$\quad \text{d)} \quad$ If $\mathcal{C} \subset \mathcal{D} \subset \sigma \mathcal{C}$, then $\sigma \mathcal{C} = \sigma \mathcal{D}$

---

1.11 &nbsp; _Borel $\sigma$-algebra on $\R$_. Every open subset of $\R = (-\infty, +\infty)$, the real line, is a countable union of open intervals. Use this fact to show that $\mathcal{B}_\R$ is generated by the collection of all open intervals.

---

1.12 &nbsp; _Continuation_. Show that every interval of $\R$ is a Borel set. In particular, $(-\infty, x)$, $(-\infty,x]$, $(x,y]$, $[x,y]$ are all Borel sets. For each $x$, the singleton $\{x\}$ is a Borel set.

---

1.13 &nbsp; _Continuation_. Show that $\mathcal{B}_\R$ is also generated by any one of the following (and many others):
$\quad \text{a)} \quad$ The collection of all intervals of the form $(-\infty, x]$.
$\quad \text{b)} \quad$ The collection of all intervals of the form $(x,y]$.
$\quad \text{c)} \quad$ The collection of all intervals of the form $[x,y]$.
$\quad \text{d)} \quad$ The collection of all intervals of the form $(x, \infty)$.

Moreover, in each case, $x$ and $y$ can be limited to rationals.

---

$$
\\
$$