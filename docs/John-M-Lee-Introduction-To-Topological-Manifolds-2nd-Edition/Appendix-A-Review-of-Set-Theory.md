---
export_on_save:
  html: true
---

<style>
.katex-display { overflow: auto hidden }
</style>

**Exercise A.1** Suppose \(A\) is a set and \(\mathscr{C}\) is a collection of sets. Prove the following properties of unions and intersections.
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
**Exercise A.2.** Given an equivalence relation \(\sim\) on a set \(X\), show that the set \(X/\sim\) of equivalence classes is a partition of \(X\). Conversely, given a partition of \(X\), show that there is a unique equivalence relation whose set of equivalence classes is exactly the original partition.

**Solution**
First, we need to show that \(X/\sim\) is a partition of \(X\). By the definition of a partition we need to show that \(X\) is the disjoint union of the sets in \(X/\sim\).  By the definition of a disjoint union we need to show that \(A, B \in X/\sim \text{ and } A \neq B \implies A \cap B = \emptyset\) (this is the "disjoint") and that \(\{y \in [x]: x \in X\} = X\) (this is the "union").

Let \(A, B \in X / \sim\) such that \(A \neq B\). Let \(a, b \in X\) such that \(A = [a]\), \(B = [b]\). Suppose there exists some \(c \in A \cap B\). Since \(a \sim c\) and \(b \sim c\) we have \(a \sim b \implies A = B \), a contradiction. By contradiction there exists no \(c \in A \cap B\), so we conclude that \(A \cap B = \emptyset\), the "disjoint" part of the "disjoint union".

Let \(y \in \{y \in [x]: x \in X\}\), then for some \(x \in X\) we have \(y \in [x]\implies y \sim x \implies y \in X\), so \(\{y \in [x]: x \in X\} \subseteq X\). Let \(x \in X\), then \(x \in [x]\), so \(X \subseteq \{y \in [x]: x \in X\}\). Therefore \(\{y \in [x]: x \in X\} = X\), the 'union' part of the "disjoint union".

Conversely, let \(\mathscr{C}\) be a partition of \(X\). Let \(\sim\) be a relation on \(X\) such that \(a \sim b \iff \exists U \in C \text{ s.t. } a, b \in U\). We need to show that \(\sim\) is an equivalence relation. Let \(a, b, c \in X\). Since \(X\) is the disjoint union of the sets of \(\mathscr{C}\), there must exist some \(U \in C\) such that \(a \in U\), so \(a \sim a\). It is trivial that \(a \sim b \implies b \sim a\). If \(a \sim b\) and \(b \sim c\), then there must exist \(U, V \in \mathscr{C}\) such that \(a, b \in U\) and \(b, c \in V\). Since \(U \cap V \neq \emptyset\) we must have \(U = V\) (this is the contrapositive of the disjoint rule), so \(a \sim c\). Therefore \(\sim\) is an equivalence relation as desired. \(\square\)
****
