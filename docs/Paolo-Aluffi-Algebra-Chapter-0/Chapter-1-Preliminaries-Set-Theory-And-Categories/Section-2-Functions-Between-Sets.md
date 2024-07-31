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
**2.4.** \(\triangleright\) Prove that 'isomorphism' is an equivalence relation (on any set of sets). \([\S 4.1]\)
**Solution**
Let \(S\) be a set of sets and \(A, B, C \in S\). Define \(\sim\) as \(X \sim Y \iff \exists f: X \to Y\), \(f\) bijective. We now check that the properties of an equivalence relation apply.
* *reflexivity:* \(A \sim A\)
This is clear by considering \(\text{id}_A\), which is obviously a bijection.
* *symmetry:* \(A \sim B \implies B \sim A\)
Since we have \(A \sim B\) we get \(f: A \to B\), \(f\) a bijection. Since \(f\) is a bijection it has an inverse, call it \(g: B \to A\), which is also a bijection, yielding \(B \sim A\).
* *transitivity:* \(\left( A \sim B \text{ and } B \sim C\right) \implies A \sim C\)
By the hypothesis we have bijections \(f: A \to B\) and \(g: B \to C\), their composition \(g \circ f: A \to C\) is also a bijection so \(A \sim C\). \(\square\)
****
**2.5.** \(\triangleright\) Formulate a notion of *epimorphism*, in the style of the notion of *monomorphism* seen in \(\S 2.6\), and prove a result analogous to Proposition 2.3, for epimorphisms and surjections. \([\S 2.6, \S 4.2]\)
**Solution**
Define a function \(f: A \to B\) to be a *epimorphism* (or *epic*) if for all sets \(Z\) and all functions \(\alpha', \alpha'' : B \to Z\) we have \(\alpha' \circ f = \alpha'' \circ f \implies \alpha' = \alpha''\). 