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
