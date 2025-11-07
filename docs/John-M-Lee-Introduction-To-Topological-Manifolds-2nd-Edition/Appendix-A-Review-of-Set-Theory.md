---
export_on_save:
  html: true
---

<style>
.katex-display { overflow: auto hidden }
</style>

# Introduction to Topological Manifolds, John M. Lee, Second Edition

## Appendix A: Review of Set Theory

### Basic Concepts

\(\blacktriangleright\) **Exercise A.1** &nbsp; Suppose \(A\) is a set and \(\mathscr{C}\) is a collection of sets. Prove the following properties of unions and intersections.
(a) \(\textrm{Distributive Laws}\):

$$
A \cup \left( \bigcap_{X \in \mathscr{C}} X \right) = \bigcap_{X \in \mathscr{C}} (A \cup X);
$$

$$
A \cap \left( \bigcup_{X \in \mathscr{C}} X \right) = \bigcup_{X \in \mathscr{C}} (A \cap X).
$$

**Solution**
Let \(x \in A \cup \left( \bigcap_{X \in \mathscr{C}} X \right)\). If \(x \in A\) then clearly we have \(x \in \bigcap_{X \in \mathscr{C}} (A \cup X)\) because \(x \in A \implies x \in A \cup X \text{ for all } X \in \mathscr{C}\). Alternatively if \(x \in \bigcap_{X \in \mathscr{C}} X\) we also have \(x \in \bigcap_{X \in \mathscr{C}} (A \cup X)\) because for each \(X \in \mathscr{C}\) we have \(x \in X \subseteq A \cup X\). Therefore \( A \cup \left( \bigcap_{X \in \mathscr{C}} X \right) \subseteq \bigcap_{X \in \mathscr{C}} (A \cup X)\).

Let \(x \in \bigcap_{X \in \mathscr{C}} (A \cup X)\). We propose that \(x \in A \cup \left( \bigcap_{X \in \mathscr{C}} X \right)\). If \(x \in A\) than this is trivial. If \(x \notin A\), then we can use the fact that for each \(X \in \mathscr{C}\) we have \(x \in A \cup X\) to conclude that \(x \in X\) for each \(X \in \mathscr{C}\). This can be rewritten as \(x \in \bigcap_{X \in \mathscr{C}} X\). This implies that the proposition is true. Therefore \(\bigcap_{X \in \mathscr{C}} (A \cup X) \subseteq A \cup \left( \bigcap_{X \in \mathscr{C}} X \right)\).

Let \( x \in A \cap \left( \bigcup_{X \in \mathscr{C}} X \right) \). This means that \(x \in A\) and that for some \(X' \in \mathscr{C}\) we have \(x \in X'\). Therefore \(x \in A \cap X'\), so \(x \in \bigcup_{X \in \mathscr{C}} (A \cap X)\). Since \(x\) is arbitrary we have \(A \cap \left( \bigcup_{X \in \mathscr{C}} X \right) \subseteq \bigcup_{X \in \mathscr{C}} (A \cap X) \).

Let \(x \in \bigcup_{X \in \mathscr{C}} (A \cap X)\). Then for some \(X' \in \mathscr{C}\) we have \(x \in A \cap X'\). Since we have \(x \in A\) and \(x \in \bigcup_{X \in \mathscr{C}} X\) (since \(X' \subseteq \bigcup_{X \in \mathscr{C}} X\)) we have \(x \in A \cap \left(\bigcup_{X \in \mathscr{C}} X\right) \). Therefore \(\bigcup_{X \in \mathscr{C} (A \cap X)} \subseteq A \cap \left( \bigcup_{X \in \mathscr{C} X} \right) \).

Combining the four subset relations at the end of each paragraph gives the two desired set equalities. \( \square \)

---

(b) \(\textrm{De Morgan's Laws}\):

$$
A \smallsetminus \left( \bigcap_{X \in \mathscr{C}} X \right) = \bigcup_{X \in \mathscr{C}} (A \smallsetminus X);
$$

$$
A \smallsetminus \left( \bigcup_{X \in \mathscr{C}} X \right) = \bigcap_{X \in \mathscr{C}} (A \smallsetminus X).
$$

**Solution** 
Let \(x \in A \smallsetminus \left( \bigcap_{X \in \mathscr{C}} X \right)\). Then there must exist some \(X' \in \mathscr{C}\) such that \(x \notin X'\), because if there wasn't we would have \(x \in \bigcap_{X \in \mathscr{C}} X\), contradicting our choice of \(x\). Since \(x \in A\) as well we have \(x \in A \smallsetminus X'\). Since \(X' \in \mathscr{C}\) we have \(x \in \bigcup_{X \in \mathscr{C}} (A \smallsetminus X)\). Since our choice of \(x\) was arbitrary we have \(A \smallsetminus \left( \bigcap_{X \in \mathscr{C}} X \right) \subseteq \bigcup_{X \in \mathscr{C}} (A \smallsetminus X) \).

Let \( x \in \bigcup_{X \in \mathscr{C}} (A \smallsetminus X) \). Then there exists some \( X' \in \mathscr{C} \) such that \( x \in A \smallsetminus X' \). So \(x \in A\) and \( x \notin X'\). Since \(x \notin X'\) we must have \(x \notin \bigcap_{X \in \mathscr{C}} X\) because \(x \in \bigcap_{X \in \mathscr{C}} \implies x \in X'\). Since \(x \in A\) and \(x \notin \bigcap_{X \in \mathscr{C}} X\) we have \(x \in A \smallsetminus \left( \bigcap_{X \in \mathscr{C}} X \right)\). Since our choice of \(x\) was arbitrary we have \( \bigcup_{X \in \mathscr{C}} (A \smallsetminus X) \subseteq A \smallsetminus \left( \bigcap_{X \in \mathscr{C}} X \right) \).

Let \(x \in A \smallsetminus \left( \bigcup_{X \in \mathscr{C}} X \right)\). Let \(X' \in \mathscr{C}\). By our choice of \(x\) we have \(x \in A\) and \(x \notin \bigcup_{X \in \mathscr{C}} X\). We must have \(x \notin X'\), because \(x \in X' \implies x \in \bigcup_{X \in \mathscr{C}} X\). So we have \(x \in A \smallsetminus X'\) for each \(X' \in \mathscr{C}\) as our choice of \(X'\) was arbitrary. We can rewrite this as \(x \in \bigcap_{X \in \mathscr{C}}(A \smallsetminus X)\). Since our choice of \(x\) was arbitrary we have \(A \smallsetminus \left( \bigcup_{X \in \mathscr{C}} X \right) \subseteq \bigcap_{X \in \mathscr{C}}(A \smallsetminus X) \).

Let \( x \in \bigcap_{X \in \mathscr{C}} (A \smallsetminus X) \). Clearly \(x \in A\). Let \(X \in \mathscr{C}\). By our choice of \(x\) we have \(x \in A \smallsetminus X\), so \(x \notin X\). Since this applies to all \(X \in \mathscr{C}\), we have \(x \notin \bigcup_{X \in \mathscr{C}} X\). So \(x \in A \smallsetminus \left(\bigcap_{X \in \mathscr{C}} X\right)\). Since our choice of \(x\) was arbitrary, we have \(\bigcap_{X \in \mathscr{C}} (A \smallsetminus X) \subseteq A \smallsetminus \left(\bigcap_{X \in \mathscr{C}} X\right) \).


Combining the four subset relations at the end of each paragraph gives the two desired set equalities. \( \square \)
****

### Cartesian Products, Relations, and Functions

#### Relations

\(\blacktriangleright\) **Exercise A.2.** &nbsp; Given an equivalence relation \(\sim\) on a set \(X\), show that the set \(X/\sim\) of equivalence classes is a partition of \(X\). Conversely, given a partition of \(X\), show that there is a unique equivalence relation whose set of equivalence classes is exactly the original partition.

**Solution**
First, we need to show that \(X/\sim\) is a partition of \(X\). By the definition of a partition we need to show that \(X\) is the disjoint union of the sets in \(X/\sim\).  By the definition of a disjoint union we need to show that \(A, B \in X/\sim \text{ and } A \neq B \implies A \cap B = \emptyset\) (this is the "disjoint") and that \(\{y \in [x]: x \in X\} = X\) (this is the "union").

Let \(A, B \in X / \sim\) such that \(A \neq B\). Let \(a, b \in X\) such that \(A = [a]\), \(B = [b]\). Suppose there exists some \(c \in A \cap B\). Since \(a \sim c\) and \(b \sim c\) we have \(a \sim b \implies A = B \), a contradiction. By contradiction there exists no \(c \in A \cap B\), so we conclude that \(A \cap B = \emptyset\), the "disjoint" part of the "disjoint union".

Let \(y \in \{y \in [x]: x \in X\}\), then for some \(x \in X\) we have \(y \in [x]\implies y \sim x \implies y \in X\), so \(\{y \in [x]: x \in X\} \subseteq X\). Let \(x \in X\), then \(x \in [x]\), so \(X \subseteq \{y \in [x]: x \in X\}\). Therefore \(\{y \in [x]: x \in X\} = X\), the 'union' part of the "disjoint union".

Conversely, let \(\mathscr{C}\) be a partition of \(X\). Let \(\sim\) be a relation on \(X\) such that \(a \sim b \iff \exists U \in C \text{ s.t. } a, b \in U\). We need to show that \(\sim\) is an equivalence relation. Let \(a, b, c \in X\). Since \(X\) is the disjoint union of the sets of \(\mathscr{C}\), there must exist some \(U \in C\) such that \(a \in U\), so \(a \sim a\). It is trivial that \(a \sim b \implies b \sim a\). If \(a \sim b\) and \(b \sim c\), then there must exist \(U, V \in \mathscr{C}\) such that \(a, b \in U\) and \(b, c \in V\). Since \(U \cap V \neq \emptyset\) we must have \(U = V\) (this is the contrapositive of the disjoint rule), so \(a \sim c\). Therefore \(\sim\) is an equivalence relation as desired. \(\square\)
****
\(\blacktriangleright\) **Exercise A.3.** &nbsp; Let \(R \subseteq X \times X\) be any relation on \(X\), and define \(\sim\) to be the intersection of all equivalence relations in \(X \times X\) that contain \(R\).
\(\quad \text{(a)}\) Show that \(\sim\) is an equivalence relation.
**Solution**
Let \(x, y, z \in X\). First we show that \(x \sim x\). This is obvious because, for each equivalence relation \(\sim' \supseteq R\), we have \((x, x) \in \sim'\), so we have \((x, x) \in \bigcap_{\sim' \supseteq R, \sim' \text{an equiv relation}} \sim' = \sim\). The same argument works for showing symmetry and trasitivity.

---

\(\quad \text{(b)}\) Show that \(x \sim y\) if and only if at least one of the following statements is true: \(x = y\), or \(x \> R' \> y\), or there is a finite sequence of elements \(z_1, \dots, z_n \in X\) such that \(x \> R' \> z_1 \>  R' \cdots R' \> z_n \> R' \> y\), where \(x \> R' \> y\) means "\(x \> R \> y\) or \(y \> R \> x\)." 
**Solution**
Assume \(x \nsim y\), so there is some equivalence relation \(\sim' \supseteq R\) such that \(x \nsim' y\). We can not have \(x = y\), because it would contadict \(x \sim' x\) (since \(\sim'\) is an equivalence relation). Since \(\sim' \supseteq R\), we have \(x \> R' \> y \implies x \> R \> y \text{ or } y \> R \> x \implies x \sim' y \text{ or } y \sim' x \implies x \sim' y\), so we can not have \(x \> R' \> y\). Similarly, \(x \> R' \> z_1 \>  R' \cdots R' \> z_n \> R' \> y \implies x \sim' z_1 \sim' \cdots \sim' z_n \sim' y \implies x \sim' y\), so we can not have \(x \> R' \> z_1 \>  R' \cdots R' \> z_n \> R' \> y\). 
Alternatively, assume that none of the three conditions are true. We need to show that \(x \nsim y\), and we can do this by constructing an equivalence relation \(\sim' \supseteq R\) such that \(x \nsim' y\). Use the three conditions to construct the equivalence relation. This construction is indeed an equivalence relation (does this need a quick verification?) and does not contain \((x, y)\). \(\square\)

---

#### Functions

$\blacktriangleright \>$ **Exercise A.4.** &nbsp; Let $f:X \to Y$ and $g:W \to X$ be maps, and suppose $R \subseteq W,S,S' \subseteq X$, and $T,T' \subseteq Y$. Prove the following:
$\quad \text{(a)} \quad T \supseteq f(f^{-1}(T))$.

**Solution**
Let $x \in f(f^{-1}(T))$. NTS that $x \in T$.

By our choice of $x$, there must exist some $y \in f^{-1}(T)$ such that $x = f(y)$. Since $y \in f^{-1}(T)$, we have $x = f(y) \in T$. $\> \square$

---

$\quad \text{(b)} \quad T \subseteq T' \implies f^{-1}(T) \subseteq f^{-1}(T')$.

**Solution**

Let $T \subseteq T'$. NTS $f^{-1}(T) \subseteq f^{-1}(T')$.

Let $x \in f^{-1}(T)$. NTS $x \in f^{-1}(T')$.

Since $x \in f^{-1}(T)$ by definition $f(x) \in T$. Since $T \subseteq T'$, $f(x) \in T'$. By definition, $x \in f^{-1}(T)$. $\> \square$

---

$\quad \text{(c)} \quad f^{-1}(T \cup T') = f^{-1}(T) \cup f^{-1}(T')$.

**Solution**

$\subseteq \quad$ First we will show that $f^{-1}(T \cup T') \subseteq f^{-1}(T) \cup f^{-1}(T')$.

Let $x \in f^{-1}(T \cup T')$. NTS $x \in f^{-1}(T) \cup f^{-1}(T')$. 

By our choice of $x$, we have $f(x) \in T \cup T'$. If $f(x) \in T$ then $x \in f^{-1}(T) \subseteq f^{-1}(T) \cup f^{-1}(T')$ and we are done. So WLOG $f(x) \notin T$.

Since $f(x) \notin T$ and $f(x) \in T \cup T'$, we must have $f(x) \in T'$, equivalentally $x \in f^{-1}(T) \subseteq f^{-1}(T) \cup f^{-1}(T')$, so we are done.

---

$\quad \text{(d)} \quad f^{-1}(T \cap T') = f^{-1}(T) \cap f^{-1}(T')$.

---

$\quad \text{(e)} \quad f^{-1}(T \setminus T') = f^{-1}(T) \setminus f^{-1}(T')$.

---

$\quad \text{(f)} \quad S \subseteq f^{-1}(f(S))$.

---

$\quad \text{(g)} \quad S \subseteq S' \implies f(S) \subseteq f(S')$.

---

$\quad \text{(h)} \quad f(S \cup S') = f(S) \cup f(S')$.

---

$\quad \text{(i)} \quad f(S \cap S') \subseteq f(S) \cap f(S')$.

---

$\quad \text{(j)} \quad f(S \setminus S') \supseteq f(S) \setminus f(S')$.

---

$\quad \text{(k)} \quad f(S) \cap T = f(S \cap f^{-1}(T))$.

---

$\quad \text{(l)} \quad f(S) \cup T \supseteq f(S \cup f^{-1}(T))$.

---

$\quad \text{(m)} \quad S \cap f^{-1}(T) \subseteq f^{-1}(f(S) \cap T)$.

---

$\quad \text{(n)} \quad S \cup f^{-1}(T) \subseteq f^{-1}(f(S) \cup T)$.

---

$\quad \text{(o)} \quad (f \circ g)^{-1}(T) = g^{-1}(f^{-1}(T))$.

---

$\quad \text{(p)} \quad (f \circ g)(R) = f(g(R))$.

---

$\blacktriangleright \>$ **Exercise A.5.** &nbsp; With notation as in the previous exercise, give counterexamples to show that the following equalities do not necessarily hold true.

$\quad \text{(a)} \quad T = f(f^{-1}(T))$.

---

$\quad \text{(b)} \quad S=f^{-1}(f(S))$.

---

$\quad \text{(c)} \quad f(S \cap S') = f(S) \cap f(S')$.

---

$\quad \text{(d)} \quad f(S \setminus S') = f(S) \setminus f(S')$.

---

$\blacktriangleright \>$ **Exercise A.6.** &nbsp; Show that a composition of injective functions is injective, a composition of surjective functions is surjective, and a composition of bijective functions is bijective.

---

$\blacktriangleright \>$ **Exercise A.7.** &nbsp; Show that equality $\text{(a)}$ in Exercise A.5. holds for every $T \subseteq Y$ if and only if $f$ is surjective, and each of the equalities $\text{(b)—(d)}$ holds for every $S,S' \subseteq X$ if and only if $f$ is injective.

---

$\blacktriangleright \>$ **Exercise A.8.** &nbsp; Let $f: X \to Y$ be a function.
$\quad \text{(a)} \quad$ Show that $f$ has an inverse if and only if it is bijective.

---

$\quad \text{(b)} \quad$ Show that if $f$ has an inverse, its inverse is unique.

---

$\quad \text{(c)} \quad$ Show that if $f: X \to Y$ and $g: Y \to Z$ are both bijective, then $(g \circ f)^{-1} = f^{-1}\circ g^{-1}$.

---

$\blacktriangleright \>$ **Exercise A.10.** &nbsp; Show that if $f: X \to Y$ is bijective, then any left or right inverse for $f$ is equal to $f^{-1}$.

---

### Number Systems and Cardinality

$\blacktriangleright \>$ **Exercise A.11.** &nbsp; Show that the real numbers are unique, in the sense that any complete ordered field admits a bijection with $\R$ that preserves addition, multiplication, and order.

---

$\blacktriangleright \>$ **Exercise A.12.** &nbsp; Show that an interval must be one of the nine types of sets $[a,b]$, $(a,b)$, $[a,b)$, $(a,b]$, $(-\infty,b]$, $(-\infty,b)$, $[a,\infty)$, $(a,\infty)$, or $(-\infty, \infty)$.

---

$\blacktriangleright \>$ **Exercise A.13.** &nbsp; Prove that any susbset of a countable set is countable.

---

$\blacktriangleright \>$ **Exercise A.14.** &nbsp; Prove that the Cartesian product of two countable sets is countable.

---

### Indexed Families

$\blacktriangleright \>$ **Exercise A.15.** &nbsp; Complete the proof of Lemma A.9 by showing that every surjective function has a right inverse.

---

$\blacktriangleright \>$ **Exercise A.16.** &nbsp; Prove that if there exists a surjective map from a countable set onto $S$, then $S$ is countable.

---

$\blacktriangleright \>$ **Exercise A.17.** &nbsp; Prove that the union of a countable collection of countable sets is countable.

$$
\\
$$