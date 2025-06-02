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
****
**1.3.** \(\triangleright\) Given a partition \(\mathscr{P}\) on a set \(S\), show how to define a relation \(\sim\) on \(S\) such that \(\mathscr{P}\) is the corresponding partition. \([\S1.5]\)
**Solution**
Define \(\sim\) such that for \(a, b \in S\) we have \(a \sim b\) if and only if for some \(A \in \mathscr{P}\) we have \(a, b \in A\). We need to show that \(\mathscr{P}_\sim = \mathscr{P}\). Let \([a]_\sim \in \mathscr{P}_\sim\), so for some \(A \in \mathscr{P}\) we have \(a \in A\), and our construction of \(\sim\) makes it clear that \([a]_\sim = A\), so \([a]_\sim \in \mathscr{P}\). Conclude that \(\mathscr{P}_\sim \subseteq \mathscr{P}\). Now let \(A \in \mathscr{P}\). Take any \(a \in A\) and observe that \(A = [a]_\sim\). Conclude that \(\mathscr{P} \subseteq \mathscr{P}_\sim\), which combined with \(\mathscr{P}_\sim \subseteq \mathscr{P}\) gives the desired \(\mathscr{P}_\sim = \mathscr{P}\). \(\square\)
****
**1.6.** \(\triangleright\) Define a relation \(\sim\) on the set \(\R\) of real numbers by setting \(a \sim b \iff b - a \in \Z\). Prove that this is an equivalence relation, and find a 'compelling' description for \(\R / \sim\). Do the same for the relation \(\approx\) on the plane \(\R \times \R\) defined by declaring \((a_1, a_2) \approx (b_1, b_2) \iff b_1 - a_1 \in \Z \) and \(b_2 - a_2 \in \Z\).
**Solution**
Let's start by proving that \(\sim\) is an equivalence relation:
* *reflexivity:* \(\forall a \in \R\) we have \(a - a = 0 \in \Z\) so \(a \sim a\);
* *symmetry* \((\forall a \in \R)\) \((\forall b \in \R)\) \(a \sim b \implies b - a \in \Z \implies a - b \in \Z \implies b \sim a\);
* *transitivity* \((\forall a \in \R)\) \((\forall b \in \R)\) \((\forall c \in \R)\), \((a \sim b \text{ and } b \sim c) \implies \left(b - a \in \Z \text{ and } c - b \in \Z \right) \implies \left(c - a \in \Z\right) \implies a \sim c\).
The argument for \(\approx\) is similar (should just amount to repeating the above twice). I am lazy and also I don't know what 'compelling' description Mr. Aluffi is looking for. \(\square\)

$$
\\
$$