---
export_on_save:
  html: true
---
<style>
.katex-display { overflow: auto hidden }
iframe {display: block; margin: 0 auto;}
</style>
**3.1.** \(\triangleright\) Let \(\mathsf{C}\) be a category. Consider a structure \(\mathsf{C}^{op}\) with
* \(\text{Obj}(\mathsf{C}^{op}) \coloneqq \text{Obj}(\mathsf{C})\);
* for \(A, B\) objects of \(\mathsf{C}^{op}\) (hence objects of \(\mathsf{C}\)), \(\text{Hom}_{\mathsf{C}^{op}}(A, B) \coloneqq \text{Hom}_{\mathsf{C}}(B, A)\).

Show how to make this into a category (that is, define composition of morphisms in \(\mathsf{C}^{op}\) and verify the properties listed in \(\S3.1\) ).
Intuitively, the 'opposite' category \(\mathsf{C}^{op}\) is simply obtained by 'reversing all the arrows' in \(\mathsf{C}\). \(\left[5.1, \S \mathrm{VIII}.1.1, \S \mathrm{IX}.1.2, \mathrm{IX.1.10} \right]\)

**Solution**
First we'll define an identity morphism. Since \(\mathsf{C}\) is a category, for every object \(A\) of \(\mathsf{C}\), there exists an identity morphism \(1_A \in \text{Hom}_\mathsf{C}(A, A)\). By our definition of \(\mathsf{C}^{op}\) we have \(\text{Obj}(\mathsf{C}^{op}) = \text{Obj}(\mathsf{C})\) and \(\text{Hom}_{\mathsf{C}^{op}}(A, A) = \text{Hom}_\mathsf{C}(A, A)\), so we can just use \(1_A\) as is for \(C^{op}\).
Now for the heart of the matter, defining the composition of morphisms in \(\mathsf{C}^{op}\) and verifying the properties of \(\S 3.1\). Let \(A, B\) be objects of \(\mathsf{C}^{op}\) (which is the same as being an object of \(\mathsf{C}\)), and let \(f \in \text{Hom}_{\mathsf{C}^{op}}(A, B)\) and \(g \in \text{Hom}_{\mathsf{C}^{op}}(B, C)\). By definition we have \(f \in \text{Hom}_{\mathsf{C}}(B, A)\) and \(g \in \text{Hom}_{\mathsf{C}}(C, B)\). This gives us \(fg \in \text{Hom}_{\mathsf{C}}(C, A) = \text{Hom}_{\mathsf{C}^{op}}(A, C)\) by composition. Define \(gf = fg\). This notation is a bit confusing because the LHS is composition in \(\mathsf{C}^{op}\) and the RHS is composition in \(\mathsf{C}\). We proceed by verifying that this composition is associative and respects the identity.
Let \(f \in \text{Hom}_{\mathsf{C}^{op}}(A, B)\), \(g \in \text{Hom}_{\mathsf{C}^{op}}(B, C)\), and \(h \in \text{Hom}_{\mathsf{C}^{op}}(C, D)\). Then \((hg)f = (gh)f\), where now on the RHS we are using composition in \(\mathsf{C}\) in the parentheses. Applying the definition of composition in \(\mathsf{C}^{op}\) again we get \((hg)f = f(gh)\). Now that on the RHS we are entirely in \(\mathsf{C}\) we can use associativity in \(\mathsf{C}\) to get \((hg)f = (fg)h\). Then using the definition of composition in \(\mathsf{C}^{op}\) twice we get \((hg)f = (fg)h = (gf)h = h(gf)\) proving associativity.
This is a bit unclear, so let me rewrite this denoting composition in \(\mathsf{C}^{op}\) as \(\circ '\) and composition in \(\mathsf{C}\) as \(\circ\). Then
$$
(h \circ' g) \circ' f = (g \circ h) \circ' f = f \circ (g \circ h) \\
 = (f \circ g) \circ h = (g \circ' f) \circ h = h \circ' (g \circ' f).
$$
It is pretty clear that the identity respects composition, let \(f \in \text{Hom}_{\mathsf{C}^{op}}(A, B) = \text{Hom}_{\mathsf{C}}(B, A)\). Because the identity respects composition in \(\mathsf{C}\) we have
$$
f \circ 1_B = f, \quad 1_A \circ f = f
$$
So by the definition of composition in \(\mathsf{C}^{op}\) and because the identities are the same in both \(\mathsf{C}\) and \(\mathsf{C}^{op}\)
$$
1_B \circ' f = f, \quad f \circ' 1_A = f;
$$
which is exactly what we set out to show. \(\square\)

****
**3.3.** \(\triangleright\) Formulate precisely what it means to say that \(1_a\) is an identity with respect to composition in Example 3.3, and prove this assertion. \(\left[\S 3.2\right]\)
**Solution**
In this example \(1_a\) is the relation \(a \sim a\) which can also be viewed as the pair \((a, a)\), to show that it is the identity with respect to composition we need to show that for all \(f \in \text{Hom}(a, b)\) we have
$$
f1_a = f, \quad 1_bf = f
$$
In our category the only element of \(\text{Hom}(a,b)\) is the pair \((a, b)\) representing the true statement \(a \sim b\), so the above is equivalent to
$$
(a, b) (a, a) = (a, b), \quad (b, b)(a, b) = (a, b);
$$
which follows directly from the definition of composition in the example. \(\square\)
****
**3.5.** \(\triangleright\) Explain in what sense Example 3.4 is an instance of the categories considered in Example 3.3. \(\left[\S 3.2\right]\)
**Solution**
Let \(A, B, C \subseteq S\) and define \(A \sim B \iff A \subseteq B\). Because \(A \subseteq B\) and \(B \subseteq C\) implies that \(A \subseteq C\), \(\sim\) is transitive. Because \(A \subseteq A\), \(\sim\) is reflective. Because \(\mathscr{P}(S)\) is a set and \(\sim\) is a reflexive and transitive relation on \(\mathscr{P}(S)\), Example 3.4 is an instance of the categories considered in Example 3.3. \(\square\)
****
**3.6.** \(\triangleright\) (Assuming some familiarity with linear algebra) Define a category \(\mathsf{V}\) by taking \(\text{Obj} = \N\) and letting \(\text{Hom}_{\mathsf{V}}(n,m) =\) the set of \(m \times n\) matrices with real entries, for all \(n, m \in \N\). (I will leave the reader the task of making sense of a matrix with \(0\) rows or columns.) Use product of matrices to define composition. Does this category 'feel' familiar? \(\left[\S \mathrm{VI}.2.1, \S \mathrm{VIII}.1.3 \right]\)
**Solution**
It 'feels' like the category of finite dimensional vector spaces, as each object is a natural number (the dimension) and the morphisms correspond to linear transformations.
****
**3.7.** \(\triangleright\) Define carefully objects and morphisms in Example 3.7, and draw the diagram corresponding to composition. \(\left[\S 3.2\right]\)
****
**3.8.** \(\triangleright\) A *subcategory* \(\mathsf{C}'\) of a category \(\mathsf{C}\) consists of a collection of objects of \(\mathsf{C}\) with sets of morphisms \(\text{Hom}_{\mathsf{C}'}(A, B) \subseteq \text{Hom}_{\mathsf{C}}(A, B)\) for all objects \(A, B\) in \(\text{Obj}(\mathsf{C}')\), such that identities and compositions in \(\mathsf{C}\) make \(\mathsf{C'}\) into a category. A subcategory \(\mathsf{C'}\) is *full* if \(\text{Hom}_{\mathsf{C'}}(A,B) = \text{Hom}_{\mathsf{C}}(A,B)\) for all \(A, B\) in \(\text{Obj}(\mathsf{C'})\). Construct a category of *infinite sets* and explain how it may be viewed as a full subcategory of \(\mathsf{Set}\). \(\left[4.4, \S \mathrm{VI}.1.1, \S \mathrm{VIII}.1.3\right]\)
****
**3.9.** \(\triangleright\) An alternative to the notion of *multiset* introduced in \(\S 2.2\) is obtained by considering sets endowed with equivalence relations; equivalent elements are taken to be multiple instances of elements 'of the same kind'. Define a notion of morphism between such enhanced sets, obtaining a category \(\mathsf{MSet}\) containing (a 'copy' of) \(\mathsf{Set}\) as a full subcategory. (There may be more than one reasonable way to do this! This is intentionally an open-ended exercise.) Which objects in \(\mathsf{MSet}\) determine the ordinary multisets as defined in \(\S2.2\) and how? Spell out what a morphism of multisets would be from this point of view. (There are several natural notions of morphisms of multisets. Try to define morphisms in \(\mathsf{MSet}\) so that the notion you obtain for ordinary multisets captures your intuitive understanding of these objects.) \(\left[\S2.2, \S3.2, 4.5\right]\)
****
**3.11.** \(\triangleright\) Draw the relevant diagrams and define composition and identities for the category \(\mathsf{C}^{A, B}\) mentioned in Example 3.9. Do the same for the category \(\mathsf{C}^{\alpha, \beta}\) mentioned in Example 3.10. \(\left[\S5.5, 5.12\right]\)