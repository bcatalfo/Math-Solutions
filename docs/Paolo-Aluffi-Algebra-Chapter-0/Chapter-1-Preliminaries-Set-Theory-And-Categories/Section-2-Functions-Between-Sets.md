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
Define a function \(f: A \to B\) to be a *epimorphism* (or *epic*) if for all sets \(Z\) and all functions \(\alpha', \alpha'' : B \to Z\) we have \(\alpha' \circ f = \alpha'' \circ f \implies \alpha' = \alpha''\). We propose that \(f\) is surjective if and only if it is epic. 
\(\left(\implies\right)\) We are given that \(f\) is surjective. By Problem 2.2 we get a right inverse \(g: B \to A\), i.e. \(f \circ g = \text{id}_B\). Let \(\alpha', \alpha'' : B \to Z\) satisfy
$$
\alpha' \circ f = \alpha'' \circ f.
$$
Compose on the right by \(g\), and use associativity of composition:
$$
\alpha' \circ (f \circ g) = (\alpha' \circ f) \circ g = (\alpha'' \circ f) \circ g = \alpha'' \circ (f \circ g);
$$
since \(g\) is a right-inverse of \(f\), this says 
$$
\alpha' \circ \text{id}_B = \alpha'' \circ \text{id}_B,
$$
and therefore
$$
\alpha' = \alpha'',
$$
as needed to conclude that \(f\) is an epimorphism.
\(\left(\impliedby\right)\) We are given that \(f\) is an epimorphism. Let \(Z = \{0, 1\}\). We define \(\alpha': B \to Z\) piecewise:
$$
\alpha'(b) = \begin{cases}
  1 &\text{if } b \in \text{Im}(f) \\
  0 &\text{otherwise } 
\end{cases}
$$
Next, we define \(\alpha'': B \to Z\) more simply, taking \(\alpha''(b) = 1\) for all \(b \in B\). It is obvious that
$$
\alpha' \circ f = \alpha'' \circ f
$$
as both functions map every element of \(B\) to \(1\). By the definition of an epimorphism we conclude that
$$
\alpha' = \alpha''.
$$
Now let \(b \in B\). If \(b \notin \text{Im}(f)\) then \(\alpha'(b) = 0\), but this is a contradiction as \(\alpha'' = \alpha'\) and \(\alpha''(b) = 1\) by its definition. So we must have \(b \in \text{Im}(f)\) for each \(b \in B\). We conclude that \(f\) is surjective. \(\square\)
****
**2.9.** \(\triangleright\) Show that if \(A' \cong A''\) and \(B' \cong B''\), and further \(A' \cap B' = \emptyset\) and \(A'' \cap B'' = \emptyset\), then \(A' \cup B' \cong A'' \cup B''\). Conclude that the operation \(A \amalg B\) (as described in \(\S 1.4\)) is well-defined *up to isomorphism* (cf. \(\S 2.9\)). \(\left[\S2.9, 5.7\right]\)
**Solution**
We are given bijections \(f: A' \to A''\) and \(g: B' \to B''\). Define \(h: A' \cup B' \to A'' \cup B''\) piecewise:
$$
h(x) = \begin{cases}
  f(x) &\text{if } x \in A' \\
  g(x) &\text{if } x \in B'
\end{cases}
$$
Since \(A' \cap B' = \emptyset\) it is evident that \(h\) is well-defined, so it is sufficient to prove that it is a bijection. 
First let's show injectivity. Let \(h(x') = h(x'')\). Since \(A'' \cap B'' = \emptyset\) we have either \(h(x') = h(x'') \in A''\) or \(h(x') = h(x'') \in B''\), but not both. We start by assuming the former, that is \(h(x') = h(x'') \in A''\). If we were to have \(x \in \{x', x''\}\) such that \(x \in B'\) then \(h(x) \in B''\), contradicting \(A'' \cap B'' = \emptyset\). We conclude that \(x', x'' \in A'\). Thus, \(h(x') = h(x'') = f(x') = f(x'')\). Since \(f\) is a bijection it is injective, so we conclude that \(x' = x''\). The other case, that is \(h(x') = h(x'') \in B''\), is handled by extremely similar reasoning.
Next we show surjectivity, which is even easier. Let \(y \in A'' \cup B''\). If \(y \in A''\) then we get \(x \in A'\) such that \(f(x) = y\) by \(f\)'s surjectivity. If \(y \in B''\) then we get \(x \in B'\) such that \(g(x) = y\) by \(g\)'s surjectivity. Either way \(h(x) = y\), so we conclude that \(h\) is surjective.
Since \(h\) is well-defined, and both injective and surjective and hence a bijection, we can conclude that \(A' \cup B' \cong A'' \cup B''\) and that \(A \amalg B\) is well-defined up to isomorphism. \(\square\)
****