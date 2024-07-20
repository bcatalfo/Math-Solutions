---
export_on_save:
  html: true
---
**Exercise 2.2**
Verify that each of the following examples is in fact a topology.
(a) Let \( X \) be any set whatsoever, and let \( \mathcal{T} = \mathcal{P}(X)\) (the ***power set of X***, which is the set of all subsets of \(X \)), so every subset of \(X\) is open. 
**Solution**
Let's verify each axiom one by one.
(i) \( X \) and \( \emptyset \) are elements of \( \mathcal{T}\).
This is obvious as \( X \) and \( \emptyset \) are both subsets of \( X \).
(ii) \( \mathcal{T} \) is closed under finite intersections.
Let \( U_1, \ldots, U_n \) be elements of \( \mathcal{T}\), then  \( U_1 \cap \cdots \cap U_n \subset U_1 \subset X\) so \( U_1 \cap \cdots \cap U_n \in \mathcal{P}(X) = \mathcal{T}\).
(iii) \( \mathcal{T}\) is closed under arbitrary unions.
Let \( (U_\alpha)_{\alpha \in A} \) be a family of elements of \( \mathcal{T}\), and let \( x \in \bigcup_{\alpha \in A} U_\alpha\). Then there must exist \( \alpha \in A\) such that \( x \in U_\alpha \subset X\), so \( x \in X\), hence \( \bigcup_{\alpha \in A} U_\alpha \in \mathcal{T}\). \( \square\)
(b) Let \( Y \) be any set, and let \( \mathcal{T} = \{Y, \emptyset \}\).
**Solution**
(i) \( Y \) and \( \emptyset \) are elements of \( \mathcal{T}\).
This is obvious by our definition of \( \mathcal{T}\).
(ii) \( \mathcal{T} \) is closed under finite intersections.
The only intersection we can construct is \( Y \cap \emptyset = \emptyset \in \mathcal{T}\).
(iii) \( \mathcal{T}\) is closed under arbitrary unions.
The only union we can construct is \( Y \cup \emptyset = Y \in \mathcal{T}\). \( \square\)
(c) Let \( Z \) be the set \( \{1, 2, 3\}\) and declare the open subsets to be \( \{1\}, \{ 1, 2\}, \{ 1, 2, 3\}\), and the empty set.
**Solution**
(i) \( Z\) and the empty set are open by definition.
(ii) Any intersection of finitely many open subsets of \( Z \) is an open subset of \( Z \).
Let's calculate some intersections:
\( \{1\} \cap \{1, 2\} = \{1\} \)
\( \{1\} \cap \{1, 2, 3\} = \{1\} \)
\( \{1, 2\} \cap \{1, 2, 3\} = \{1, 2\} \)
(iii) Any union of arbitrarily many open subsets of \( Z \) is an open subset of \( Z \). 
Let's calculate some unions:
\( \{1\} \cup \{1, 2\} = \{1, 2\} \)
\( \{1\} \cup \{1, 2, 3\} = \{1, 2, 3\} \)
\( \{1, 2\} \cup \{1, 2, 3\} = \{1, 2, 3\}\) \( \square\)

**Exercise 2.4**
(a) Suppose that \( M \) is a set and \( d, d'\) are two different metrics on \( M \). Prove that \( d \) and \( d' \) generate the same topology on \( M \) if and only if the following condition is satisfied: for every \( x \in M\) and every \( r > 0\), there exist positive numbers \( r_1 \) and \( r_2\) such that \( B_{r_1}^{d'}(x) \subseteq B_{r}^{(d)}(x)\) and \(B_{r_2}^{(d)}(x) \subseteq B_{r}^{(d')}(x)\).