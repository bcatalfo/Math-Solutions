---
export_on_save:
  html: true
---
<style>
.katex-display { overflow: auto hidden }
</style>
**1.2.**  \(\triangleright\) Prove that if \(\sim\) is an equivalence relation on a set \(S\), then the corresponding family \(\mathscr{P}_\sim\) defined in \(\S1.5\) is indeed a partition of \(S\): that is, its elements are nonempty, disjoint, and their union is \(S\). \([\S1.5]\)
**Solution**
First recall that \(\mathscr{P}_\sim\) is defined as the set of all equivalence classes, where for each \(a \in S\) we have the equivalence class
$$
[a]_\sim \coloneqq \{b \in S \mid b \sim a\} .
$$
Each \([a]_\sim\) is nonempty as \(a \in [a]_\sim\). For some \(a, b \in S\) if \(x \in [a]_\sim \cap [b]_\sim\) then we have both \(x \sim a\) and \(x \sim b\) so by symmetry and transitivity \(a \sim b\), so our equivalence classes are disjoint. Finally, since we have an equivalence class for each \(a \in S\) of course the union of all the elements is \(S\). \(\square\)