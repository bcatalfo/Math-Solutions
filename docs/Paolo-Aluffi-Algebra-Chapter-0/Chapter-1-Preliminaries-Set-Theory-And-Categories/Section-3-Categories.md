---
export_on_save:
  html: true
---
<style>
.katex-display { overflow: auto hidden }
</style>
**3.1.** \(\triangleright\) Let \(\mathsf{C}\) be a category. Consider a structure \(\mathsf{C}^{op}\) with
* \(\text{Obj}(\mathsf{C}^{op}) \coloneqq \text{Obj}(\mathsf{C})\);
* for \(A, B\) objects of \(\mathsf{C}^{op}\) (hence objects of \(\mathsf{C}\)), \(\text{Hom}_{\mathsf{C}^{op}}(A, B) \coloneqq \text{Hom}_{\mathsf{C}}(B, A)\).

Show how to make this into a category (that is, define composition of morphisms in \(\mathsf{C}^{op}\) and verify the properties listed in \(\S3.1\) ).
Intuitively, the 'opposite' category \(\mathsf{C}^{op}\) is simply obtained by 'reversing all the arrows' in \(\mathsf{C}\). \(\left[5.1, \S \mathrm{VIII}.1.1, \S \mathrm{IX}.1.2, \mathrm{IX.1.10} \right]\)
Here is a test diagram with Quiver
<!-- https://q.uiver.app/#q=WzAsMixbMCwwLCJBIl0sWzIsMCwiQiJdLFswLDEsImYiXV0= -->
<iframe class="quiver-embed" src="https://q.uiver.app/#q=WzAsMixbMCwwLCJBIl0sWzIsMCwiQiJdLFswLDEsImYiXV0=&embed" width="300" height="150" style="border-radius: 8px; border: none;"></iframe>


****
**3.3.** Formulate precisely what it means to say that \(1_a\) is an identity with respect to composition in Example 3.3, and prove this assertion. \(\left[\S 3.2\right]\)
****
**3.5.** Explain in what sense Example 3.4 is an instance of the categories considered in Example 3.3. \(\left[\S 3.2\right]\)
****
**3.6.** \(\triangleright\) (Assuming some familiarity with linear algebra) Define a category \(\mathsf{V}\) by taking \(\text{Obj} = \N\) and letting \(\text{Hom}_{\mathsf{V}}(n,m) =\) the set of \(m \times n\) matrices with real entries, for all \(n, m \in \N\). (I will leave the reader the task of making sense of a matrix with \(0\) rows or columns.) Use product of matrices to define composition. Does this category 'feel' familiar? \(\left[\S \mathrm{VI}.2.1, \S \mathrm{VIII}.1.3 \right]\)
****
**3.7.** \(\triangleright\) Define carefully objects and morphisms in Example 3.7, and draw the diagram corresponding to composition. \(\left[\S 3.2\right]\)
****
**3.8.** \(\triangleright\) A *subcategory* \(\mathsf{C}'\) of a category \(\mathsf{C}\) consists of a collection of objects of \(\mathsf{C}\) with sets of morphisms \(\text{Hom}_{\mathsf{C}'}(A, B) \subseteq \text{Hom}_{\mathsf{C}}(A, B)\) for all objects \(A, B\) in \(\text{Obj}(\mathsf{C}')\), such that identities and compositions in \(\mathsf{C}\) make \(\mathsf{C'}\) into a category. A subcategory \(\mathsf{C'}\) is *full* if \(\text{Hom}_{\mathsf{C'}}(A,B) = \text{Hom}_{\mathsf{C}}(A,B)\) for all \(A, B\) in \(\text{Obj}(\mathsf{C'})\). Construct a category of *infinite sets* and explain how it may be viewed as a full subcategory of \(\mathsf{Set}\). \(\left[4.4, \S \mathrm{VI}.1.1, \S \mathrm{VIII}.1.3\right]\)
****
**3.9.** \(\triangleright\) An alternative to the notion of *multiset* introduced in \(\S 2.2\) is obtained by considering sets endowed with equivalence relations; equivalent elements are taken to be multiple instances of elements 'of the same kind'. Define a notion of morphism between such enhanced sets, obtaining a category \(\mathsf{MSet}\) containing (a 'copy' of) \(\mathsf{Set}\) as a full subcategory. (There may be more than one reasonable way to do this! This is intentionally an open-ended exercise.) Which objects in \(\mathsf{MSet}\) determine the ordinary multisets as defined in \(\S2.2\) and how? Spell out what a morphism of multisets would be from this point of view. (There are several natural notions of morphisms of multisets. Try to define morphisms in \(\mathsf{MSet}\) so that the notion you obtain for ordinary multisets captures your intuitive understanding of these objects.) \(\left[\S2.2, \S3.2, 4.5\right]\)
****
**3.11.** \(\triangleright\) Draw the relevant diagrams and define composition and identities for the category \(\mathsf{C}^{A, B}\) mentioned in Example 3.9. Do the same for the category \(\mathsf{C}^{\alpha, \beta}\) mentioned in Example 3.10. \(\left[\S5.5, 5.12\right]\)