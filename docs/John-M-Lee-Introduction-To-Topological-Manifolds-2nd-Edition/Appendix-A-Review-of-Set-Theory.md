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
