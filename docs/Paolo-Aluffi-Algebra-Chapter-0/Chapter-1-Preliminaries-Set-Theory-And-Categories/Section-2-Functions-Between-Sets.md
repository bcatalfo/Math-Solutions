---
export_on_save:
  html: true
---
<style>
.katex-display { overflow: auto hidden }
</style>
**2.1.** \(\triangleright\) How many different bijections are there between a set \(S\) with \(n\) elements and itself? \(\S \mathrm{II}2.1\) 
**Solution**  
\(n!\) of course :3 As there are \(n\) choices as to where to send the first element, \(n - 1\) choices for the second element, etc. \(\square\)
****
**2.2.** \(\triangleright\) Prove statement (2) in Proposition 2.1. You may assume that given a family of disjoint nonempty subsets of a set, there is a way to choose one element in each member of the family. \([\S 2.5, \mathrm{V}. 3.3]\)
**Solution**
Assume \(A \neq \emptyset\) and let \(f: A \to B\) be a function. Statement (2) in Proposition 2.1 asks us to prove that \(f\) has a right-inverse if and only if it is surjective.
\((\implies)\) Assume that \(f\) has a right inverse. This means that we have some \(g: B \to A\) such that \(f \circ g = \text{id}_B\). Let \(b \in B\). To show that \(f\) is surjective it is sufficient to find \(a \in A\) such that \(f(a) = b\). By our assumption \(f(g(b)) = (f \circ g) (b) = \text{id}_B(b) = b\). Hence, \(g(b) \in A\) is our desired \(a\).
\((\impliedby)\) Assume that \(f\) is surjective. We need to construct some \(g: B \to A\) such that \(f \circ g = \text{id}_B\). For each \(b \in B\), since \(f\) is surjective there exists \(a \in A\) such that \(f(a) = b\). So we define \(g(b) = a\) with the axiom of choice, clearly \(f \circ g = \text{id}_B\) as desired. \(\square\)
****
**2.4.** \(\triangleright\) Prove that 'isomorphism' is an equivalence relation (on any set of sets). \([\S 2.5, \mathrm{V}.3.3]\)
**Solution**
