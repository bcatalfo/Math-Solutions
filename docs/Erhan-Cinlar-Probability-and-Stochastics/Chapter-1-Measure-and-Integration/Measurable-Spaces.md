---
export_on_save:
  html: true
---
<style>
.katex-display { overflow: auto hidden }
img {display: block; margin: 0 auto;}
</style>
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
\(\quad \text{b)} \>\) Let \(\mathcal{C}\) be a (countable) partition of \(E\). Show that every element of \(\sigma \mathcal{C}\) is a countable union of elements taken from \(\mathcal{C}\). Hint: Let \(\mathcal{E}\) be the collection of all sets that are countable unions of elements taken from \(\mathcal{C}\). Show that \(\mathcal{E}\) is a \(\sigma\)-algebra, and argue that \(\mathcal{E} = \sigma \mathcal{C}\).
\(\quad \text{c)} \>\) Let \(E = \R\), the set of all real numbers. Let \(\mathcal{C}\) be the collection of all singleton subsets of \(\R\), that is, each element of \(\mathcal{C}\) is a set that consists of exactly one point in \(\R\). Show that every element of \(\sigma \mathcal{C}\) is either a countable set or the complement of a countable set. Incidentally, \(\sigma \mathcal{C}\) is much smaller than \(\mathcal{B}(\R)\); for instance, the interval \((0, 1)\) belongs to the latter but not to the former.