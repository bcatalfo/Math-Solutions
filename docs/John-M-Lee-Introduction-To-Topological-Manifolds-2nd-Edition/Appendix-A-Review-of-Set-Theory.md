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

(b) \(\textrm{De Morgan's Laws}\):

$$
A \smallsetminus \left( \bigcap_{X \in \mathscr{C}} X \right) = \bigcup_{X \in \mathscr{C}} (A \smallsetminus X);
$$

$$
A \smallsetminus \left( \bigcup_{X \in \mathscr{C}} X \right) = \bigcap_{X \in \mathscr{C}} (A \smallsetminus X).
$$
