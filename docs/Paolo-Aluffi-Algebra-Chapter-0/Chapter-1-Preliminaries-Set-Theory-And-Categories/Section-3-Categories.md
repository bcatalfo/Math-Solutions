---
export_on_save:
  html: true
---
<style>
.katex-display { overflow: auto hidden }
img {display: block; margin: 0 auto;}
p.dot { display: flex; justify-content: center; }
.tikz { display: flex; justify-content: center; align-items: center}
</style>
**3.1.** \(\triangleright\) Let \(\mathsf{C}\) be a category. Consider a structure \(\mathsf{C}^{op}\) with
* \(\text{Obj}(\mathsf{C}^{op}) \coloneqq \text{Obj}(\mathsf{C})\);
* for \(A, B\) objects of \(\mathsf{C}^{op}\) (hence objects of \(\mathsf{C}\)), \(\text{Hom}_{\mathsf{C}^{op}}(A, B) \coloneqq \text{Hom}_{\mathsf{C}}(B, A)\).

Show how to make this into a category (that is, define composition of morphisms in \(\mathsf{C}^{op}\) and verify the properties listed in \(\S3.1\) ).
Intuitively, the 'opposite' category \(\mathsf{C}^{op}\) is simply obtained by 'reversing all the arrows' in \(\mathsf{C}\). \(\left[5.1, \S \mathrm{VIII}.1.1, \S \mathrm{IX}.1.2, \mathrm{IX.1.10} \right]\)

**Solution**
First we'll define an identity morphism. Since \(\mathsf{C}\) is a category, for every object \(A\) of \(\mathsf{C}\), there exists an identity morphism \(1_A \in \text{Hom}_\mathsf{C}(A, A)\). By our definition of \(\mathsf{C}^{op}\) we have \(\text{Obj}(\mathsf{C}^{op}) = \text{Obj}(\mathsf{C})\) and \(\text{Hom}_{\mathsf{C}^{op}}(A, A) = \text{Hom}_\mathsf{C}(A, A)\), so we can just use \(1_A\) as is for \(C^{op}\).
Now for the heart of the matter, defining the composition of morphisms in \(\mathsf{C}^{op}\) and verifying the properties of \(\S 3.1\). Let \(A, B\) be objects of \(\mathsf{C}^{op}\) (which is the same as being an object of \(\mathsf{C}\)), and let \(f \in \text{Hom}_{\mathsf{C}^{op}}(A, B)\) and \(g \in \text{Hom}_{\mathsf{C}^{op}}(B, C)\). By definition, we have \(f \in \text{Hom}_{\mathsf{C}}(B, A)\) and \(g \in \text{Hom}_{\mathsf{C}}(C, B)\). This gives us \(fg \in \text{Hom}_{\mathsf{C}}(C, A) = \text{Hom}_{\mathsf{C}^{op}}(A, C)\) by composition. Define \(gf = fg\). This notation is a bit confusing because the LHS is composition in \(\mathsf{C}^{op}\) and the RHS is composition in \(\mathsf{C}\). We proceed by verifying that this composition is associative and respects the identity.
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
**Solution**
Let \(\mathsf{C}\) be a category and \(A \in \text{Obj}(\mathsf{C})\). We define the co-slice category \(\mathsf{C}_A\) as follows:
* \(\text{Obj}(\mathsf{C}_A) = \{f \in \text{Hom}_{\mathsf{C}}(A, Z): Z \in \text{Obj}(\mathsf{C})\} \). Diagrammatically,
```dot 
digraph {
  {
    node [shape=none fontsize=18]
    A [label=<<i>A</i>>]
    Z [label=<<i>Z</i>>]
  }
  A -> Z [label=<  <i><b>f</b></i>>]
}
```

* If \(f_1, f_2 \in \text{Obj}(\mathsf{C}_A)\), diagrammatically
```dot
digraph { 
  {
    node [shape=none fontsize=18]
    A [label=<<i>A</i>>]
    Z_1 [label=<<i>Z</i><sub>1</sub>>]
    Z_2 [label=<<i>Z</i><sub>2</sub>>]
  }
  A -> Z_1 [xlabel=<<I><b>f</b></I><SUB>1</SUB>  >]
  A -> Z_2 [label=<  <I><b>f</b></I><SUB>2</SUB> >]
}
```


Then elements of \(\text{Hom}_{\mathsf{C}_A}(f_1, f_2)\) are commutative diagrams like
```dot
digraph {
  {
    node [shape=none fontsize=18]
    A [label=<<i>A</i>>];
    Z_1 [label=<<i>Z</i><sub>1</sub>>];
    Z_2 [label=<<i>Z</i><sub>2</sub>>];
  }
  A -> Z_1 [xlabel=<<i><b>f</b></i><sub>1</sub> >];
  A -> Z_2 [label=< <i><b>f</b></i><sub>2</sub>>];
  {Z_1 -> Z_2 [xlabel=< <i><b> &sigma;    </b></i>>]; rank=same;}
}
```

And if we were to take two morphisms, \(\sigma: f_1 \to f_2\) and \(\tau: f_2 \to f_3\) pictured below
```dot
digraph {
  label="(1)"
  {
    node [shape=none fontsize=18]
    A [label=<<i>A</i>>];
    Z_1 [label=<<i>Z</i><sub>1</sub>>];
    Z_2 [label=<<i>Z</i><sub>2</sub>>];
    _A [label=<<i>A</i>>];
    _Z_2 [label=<<i>Z</i><sub>2</sub>>];
    _Z_3 [label=<<i>Z</i><sub>3</sub>>]
  }
  subgraph {
    A -> Z_1 [xlabel=<<i><b>f</b></i><sub>1</sub> >];
    A -> Z_2 [label=< <i><b>f</b></i><sub>2</sub>>];
    {Z_1 -> Z_2 [xlabel=<  <i><b>&sigma;     </b></i>>]; rank=same;}
  }
  subgraph {
    _A -> _Z_2 [xlabel=<<i><b>f</b></i><sub>2</sub> >];
    _A -> _Z_3 [label=< <i><b>f</b></i><sub>3</sub>>];
    {_Z_2 -> _Z_3 [xlabel=<  <i><b>&tau;    </b></i>>]; rank=same;}
  }
}
```

we can define their composition by first putting the diagrams side-by-side
```dot
digraph {
  {
    node [shape=none fontsize=18]
    A [label=<<i>A</i>>];
    Z_1 [label=<<i>Z</i><sub>1</sub>>];
    Z_2 [label=<<i>Z</i><sub>2</sub>>];
    Z_3 [label=<<i>Z</i><sub>3</sub>>]
  }
    A -> Z_1 [xlabel=<<i><b>f</b></i><sub>1</sub> >];
    A -> Z_2 [label=< <i><b>f</b></i><sub>2</sub>>];
    {Z_1 -> Z_2 [xlabel=<  <i><b>&sigma;    </b></i>>]; rank=same;}
    A -> Z_3 [label=< <i><b>f</b></i><sub>3</sub>>];
    {Z_2 -> Z_3 [xlabel=<  <i><b>&tau;    </b></i>>]; rank=same;}
}
```

And then removing the middle and composing \(\sigma\) and \(\tau\)
```dot
digraph {
  {
    node [shape=none fontsize=18]
    A [label=<<i>A</i>>];
    Z_1 [label=<<i>Z</i><sub>1</sub>>];
    Z_3 [label=<<i>Z</i><sub>3</sub>>]
  }
    A -> Z_1 [xlabel=<<i><b>f</b></i><sub>1</sub> >];
    A -> Z_3 [label=< <i><b>f</b></i><sub>3</sub>>];
    {Z_1 -> Z_3 [xlabel=<<i><b>&tau;&sigma;    </b></i>>] rank=same}
}
```

The above diagram commutes because 
$$
\tau \sigma f_1 = \tau (\sigma f_1)
$$ 
because composition in categories is associative, and
$$
\tau (\sigma f_1) = \tau f_2 = f_3
$$
due to the commutative diagrams in (1). 
Composition in \(\mathsf{C}_A\) is associative because (**TODO: FIX THIS ARGUMENT**) the following diagram commutes 
```dot
digraph {
  {
    node [shape=none fontsize=18]
    A [label=<<i>A</i>>];
    Z_1 [label=<<i>Z</i><sub>1</sub>>];
    Z_2 [label=<<i>Z</i><sub>2</sub>>];
    Z_3 [label=<<i>Z</i><sub>3</sub>>]
    Z_4 [label=<<i>Z</i><sub>4</sub>>];
  }
  A -> Z_1 [label=<<i><b>f</b></i><sub>1</sub>>]
  A -> Z_2 [label=<<i><b>f</b></i><sub>2</sub>>]
  A -> Z_3 [label=< <i><b>f</b></i><sub>3</sub>>]
  A -> Z_4 [label=< <i><b>f</b></i><sub>4</sub>>]
  {
    Z_1 -> Z_2 [xlabel=< <i><b> &sigma;   </b></i>>]
    Z_2 -> Z_3 [xlabel=< <i><b> &tau;    </b></i>>]
    Z_3 -> Z_4 [xlabel=< <i><b> &nu;    </b></i>>]
    rank=same
  }
}
```
so \((\sigma \tau) \upsilon = \sigma (\tau \upsilon)\). 
For every \(f: A \to Z\) in \(\mathsf{C}_A\), the identity \(1_f\) is the following commutative diagram
```dot
digraph {
  node [shape=none fontsize=18]

  A [label=<<i>A</i>>]
  Z [label=<<i>Z</i>>]

  A -> Z [label=<<i>  <b>f</b></i>>]
  Z -> Z [label=<  <b>1</b><sub><i>Z</i></sub>>]
}
```
which commutes because \(\mathsf{C}\) is a category. 
Finally, the identity is an identity with respect to our composition. To show this first take the diagram earlier for \(\sigma\), representing an arbitrary morphism in \(\mathsf{C}_A\), and put the identity diagram with it side-by-side
```dot
digraph {
  node [shape=none fontsize=18]

  A [label=<<i>A</i>>]
  Z_1 [label=<<table border="0">
  <tr><td port="start"></td><td rowspan="2" colspan="3"><i>Z</i><sub>1</sub></td></tr>
  <tr><td port="end"></td></tr>
  </table>>]
  Z_2 [label=<<i>Z</i><sub>2</sub>>]

  A -> Z_1 [xlabel=<<i><b>f</b></i><sub>1</sub> >]
  A -> Z_2 [label=< <i><b>f</b></i><sub>2</sub> >]
  Z_1:start -> Z_1:end [label=<
  <table border="0" cellspacing="0" cellpadding="0">
    <tr><td rowspan="2">  <font point-size="20"><b>1</b></font></td><td> </td></tr>
    <tr><td><i>Z</i><sub>1</sub></td></tr>
  </table>
  > ]
  { Z_1 -> Z_2 [xlabel=<<table border="0"><tr><td><b><i><font point-size="18">    &sigma;    </font></i></b></td></tr></table>> ] rank=same  }
}
```
then, as per the definition of composition in \(\mathsf{C}_A\), we remove the middle and compose \(\sigma\) and \(1_{Z_1}\)
```dot
digraph {
  node [shape=none fontsize=18]

  A [label=<<i>A</i>>]
  Z_1 [label=<<i>Z</i><sub>1</sub>>]
  Z_2 [label=<<i>Z</i><sub>2</sub>>]

  A -> Z_1 [xlabel=<<i><b>f</b></i><sub>1</sub> >]
  A -> Z_2 [label=< <i><b>f</b></i><sub>2</sub> >]
  { Z_1 -> Z_2 [xlabel=<
  <table border="0" cellspacing="0" cellpadding="0">
    <tr>
      <td rowspan="2"><b><i><font point-size="18">&sigma;</font></i></b></td>
      <td rowspan="2"><b> <font point-size="18">1</font></b> </td>
      <td> </td>
    </tr>
    <tr>
      <td><i>Z</i><sub>1</sub></td>
    </tr>
  </table>
  > ] rank=same  }
}
```
The diagram above is by definition \(\sigma 1_{f_1}\). Because \(\mathsf{C}\) is a category \(\sigma 1_{Z_1} = \sigma\) so \(\sigma 1_{f_1}\) is equal to the below diagram
```dot
digraph {
  node [shape=none fontsize=18]

  A [label=<<i>A</i>>]
  Z_1 [label=<<i>Z</i><sub>1</sub>>]
  Z_2 [label=<<i>Z</i><sub>2</sub>>]

  A -> Z_1 [xlabel=<<i><b>f</b></i><sub>1</sub> >]
  A -> Z_2 [label=< <i><b>f</b></i><sub>2</sub> >]
  { Z_1 -> Z_2 [xlabel=<
      <b><i><font point-size="18">&sigma;     </font></i></b>
  > ] rank=same  }
}
```
which is the original diagram for \(\sigma\), so we can conclude that \(\sigma 1_{f_1} = \sigma\). The argument that \(1_{f_2}\sigma = \sigma\) is similar. \(\square\)
****
**3.8.** \(\triangleright\) A *subcategory* \(\mathsf{C}'\) of a category \(\mathsf{C}\) consists of a collection of objects of \(\mathsf{C}\) with sets of morphisms \(\text{Hom}_{\mathsf{C}'}(A, B) \subseteq \text{Hom}_{\mathsf{C}}(A, B)\) for all objects \(A, B\) in \(\text{Obj}(\mathsf{C}')\), such that identities and compositions in \(\mathsf{C}\) make \(\mathsf{C'}\) into a category. A subcategory \(\mathsf{C'}\) is *full* if \(\text{Hom}_{\mathsf{C'}}(A,B) = \text{Hom}_{\mathsf{C}}(A,B)\) for all \(A, B\) in \(\text{Obj}(\mathsf{C'})\). Construct a category of *infinite sets* and explain how it may be viewed as a full subcategory of \(\mathsf{Set}\). \(\left[4.4, \S \mathrm{VI}.1.1, \S \mathrm{VIII}.1.3\right]\)

**Solution**

Let $\mathsf{C} = \mathsf{Set}$. Then by the definition of $\mathsf{Set}$,
- $\text{Obj}(\mathsf{\mathsf{C}}) = \text{the class of all sets}$
- For $A,B \in \text{Obj}(\mathsf{C}), \text{Hom}_{\textsf{C}}(A,B) = B^A$

Let $\text{Obj}(\mathsf{C'}) = \text{the class of all infinite sets}$. For $A,B \in \text{Obj}(\mathsf{C'})$, let $\text{Hom}_{\mathsf{C'}}(A,B) = \text{Hom}_{\mathsf{C'}}(A,B) = B^A$. We must show that identities and compositions in $\mathsf{C}$ make $\mathsf{C'}$ into a category. This is obvious as all of the properties are inherited from $\mathsf{C}$. $\quad \square$

****

**3.9.** \(\triangleright\) An alternative to the notion of *multiset* introduced in \(\S 2.2\) is obtained by considering sets endowed with equivalence relations; equivalent elements are taken to be multiple instances of elements 'of the same kind'. Define a notion of morphism between such enhanced sets, obtaining a category \(\mathsf{MSet}\) containing (a 'copy' of) \(\mathsf{Set}\) as a full subcategory. (There may be more than one reasonable way to do this! This is intentionally an open-ended exercise.) Which objects in \(\mathsf{MSet}\) determine the ordinary multisets as defined in \(\S2.2\) and how? Spell out what a morphism of multisets would be from this point of view. (There are several natural notions of morphisms of multisets. Try to define morphisms in \(\mathsf{MSet}\) so that the notion you obtain for ordinary multisets captures your intuitive understanding of these objects.) \(\left[\S2.2, \S3.2, 4.5\right]\)

**Solution**

In $\mathsf{MSet}$ our objects are surjective projections that send $a \in A$ to its equivalence class $[a]_\sim$,

```latex {cmd=true, hide=true, latex_zoom=200%}
\documentclass[tikz]{standalone}
\usetikzlibrary{cd}
\begin{document}
\begin{tikzcd}
  A \arrow[r, twoheadrightarrow] & A / \sim
\end{tikzcd}
\end{document}
```

and our morphisms are diagrams like

```latex {cmd=true, hide=true, latex_zoom=200%}
\documentclass[tikz]{standalone}
\usetikzlibrary{cd}
\begin{document}
\begin{tikzcd}
  A \arrow[r, twoheadrightarrow] & A / \sim \arrow[d, "f"] \\
  B \arrow[r, twoheadrightarrow] & B / \sim' 
\end{tikzcd} 
\end{document}
```

where $f$ takes an equivalence class $[a]_\sim$ where $a \in A$ as input and outputs an equivalence class $[b]_{\sim'}$ where $b\in B$.

Given two morphisms $f: A / \sim \, \to B  /\sim'$ and $g: B / \sim' \, \to C / \sim''$, to combine them we stack them,

```latex {cmd=true, hide=true, latex_zoom=200%}
\documentclass[tikz]{standalone}
\usetikzlibrary{cd}
\begin{document}
\begin{tikzcd}
  A \arrow[r, twoheadrightarrow] & A / \sim \arrow[d, "f"] \\
  B \arrow[r, twoheadrightarrow] & B / \sim' \arrow[d,"g"] \\
  C \arrow[r, twoheadrightarrow] & C / \sim'' 
\end{tikzcd} 
\end{document}
```

compose $f$ and $g$ to get $g \circ f$ and remove the middle, as shown below.

```latex {cmd=true, hide=true, latex_zoom=200%}
\documentclass[tikz]{standalone}
\usetikzlibrary{cd}
\begin{document}
\begin{tikzcd}
  A \arrow[r, twoheadrightarrow] & A / \sim \arrow[d, "g \circ f"] \\
  C \arrow[r, twoheadrightarrow] & C / \sim'' 
\end{tikzcd} 
\end{document}
```

the identity morphism is the diagram below,


```latex {cmd=true, hide=true, latex_zoom=200%}
\documentclass[tikz]{standalone}
\usetikzlibrary{cd}
\begin{document}
\begin{tikzcd}
  A \arrow[r, twoheadrightarrow] & A / \sim \arrow[d, "1"] \\
  A \arrow[r, twoheadrightarrow] & A / \sim 
\end{tikzcd} 
\end{document}
```

where $1$ is of course the identity on $A / \sim$. Since $f \circ 1 = f$ this identity morphism is an identity with respect to composition, following the steps we first stack the diagrams for $1$ and for $f$,

```latex {cmd=true, hide=true, latex_zoom=200%}
\documentclass[tikz]{standalone}
\usetikzlibrary{cd}
\begin{document}
\begin{tikzcd}
  A \arrow[r, twoheadrightarrow] & A / \sim \arrow[d, "1"] \\
  A \arrow[r, twoheadrightarrow] & A / \sim \arrow[d,"f"] \\
  B \arrow[r, twoheadrightarrow] & B / \sim' 
\end{tikzcd} 
\end{document}
```

compose $f \circ 1 = f$ and remove the middle to get 

```latex {cmd=true, hide=true, latex_zoom=200%}
\documentclass[tikz]{standalone}
\usetikzlibrary{cd}
\begin{document}
\begin{tikzcd}
  A \arrow[r, twoheadrightarrow] & A / \sim \arrow[d, "f"] \\
  B \arrow[r, twoheadrightarrow] & B / \sim' 
\end{tikzcd} 
\end{document}
```

which is the original morphism. This also works in the other direction: consider the right-sided identity morphism,

```latex {cmd=true, hide=true, latex_zoom=200%}
\documentclass[tikz]{standalone}
\usetikzlibrary{cd}
\begin{document}
\begin{tikzcd}
  B \arrow[r, twoheadrightarrow] & B / \sim' \arrow[d, "1"] \\
  B \arrow[r, twoheadrightarrow] & B / \sim' 
\end{tikzcd} 
\end{document}
```

stack the morphism for $f$ on top of it,

```latex {cmd=true, hide=true, latex_zoom=200%}
\documentclass[tikz]{standalone}
\usetikzlibrary{cd}
\begin{document}
\begin{tikzcd}
  A \arrow[r, twoheadrightarrow] & A / \sim \arrow[d, "f"] \\
  B \arrow[r, twoheadrightarrow] & B / \sim' \arrow[d,"1"] \\
  B \arrow[r, twoheadrightarrow] & B / \sim' 
\end{tikzcd} 
\end{document}
```

remove the middle and compose $1 \circ f = f$ to get the original diagram for $f$,

```latex {cmd=true, hide=true, latex_zoom=200%}
\documentclass[tikz]{standalone}
\usetikzlibrary{cd}
\begin{document}
\begin{tikzcd}
  A \arrow[r, twoheadrightarrow] & A / \sim \arrow[d, "f"] \\
  B \arrow[r, twoheadrightarrow] & B / \sim' 
\end{tikzcd} 
\end{document}
```

showing that indeed *both* indentity morphisms do function as identities with respect to composing morphisms.

Finally we need to show that with respect to morphisms we have associativity, for this we need a new morphism $h: C / \sim'' \to D / \sim'''$ and to show that

$$
(hg)f = h(gf).
$$

First we find $hg$, which by definition involves first stacking $g$ and $h$,

```latex {cmd=true, hide=true, latex_zoom=200%}
\documentclass[tikz]{standalone}
\usetikzlibrary{cd}
\begin{document}
\begin{tikzcd}
  B \arrow[r,twoheadrightarrow] & B / \sim' \arrow[d,"g"] \\
  C \arrow[r,twoheadrightarrow] & C / \sim'' \arrow[d,"h"] \\
  D \arrow[r,twoheadrightarrow] & D / \sim''' 
\end{tikzcd}
\end{document}
```

then removing the middle and composing $g$ and $h$ to get $h \circ g$

```latex {cmd=true, hide=true, latex_zoom=200%}
\documentclass[tikz]{standalone}
\usetikzlibrary{cd}
\begin{document}
\begin{tikzcd}
  B \arrow[r, twoheadrightarrow] & B / \sim' \arrow[d, "h \circ g"] \\
  D \arrow[r,twoheadrightarrow] & D / \sim'''
\end{tikzcd}
\end{document}
```

so to find the morphism $(hg)f$ we have to first stack the morphism for $f$ onto the above morphism for $hg$,

```latex {cmd=true, hide=true, latex_zoom=200%}
\documentclass[tikz]{standalone}
\usetikzlibrary{cd}
\begin{document}
\begin{tikzcd}
  A \arrow[r, twoheadrightarrow] & A / \sim \arrow[d, "f"] \\
  B \arrow[r, twoheadrightarrow] & B / \sim' \arrow[d, "h \circ g"] \\
  D \arrow[r,twoheadrightarrow] & D / \sim'''
\end{tikzcd}
\end{document}
```

then composing $f$ with $h \circ g$ to get $(h \circ g) \circ f = h \circ g \circ f$, and removing the middle to get the below diagram.

```latex {cmd=true, hide=true, latex_zoom=200%}
\documentclass[tikz]{standalone}
\usetikzlibrary{cd}
\begin{document}
\begin{tikzcd}
  A \arrow[r, twoheadrightarrow] & A / \sim \arrow[d, "h \circ g \circ f"] \\
  D \arrow[r,twoheadrightarrow] & D / \sim'''
\end{tikzcd}
\end{document}
```

Now we need to show that the morphism $h(gf)$ is the above diagram. We start by taking the diagram for $gf$, which is by definition the below diagram,

```latex {cmd=true, hide=true, latex_zoom=200%}
\documentclass[tikz]{standalone}
\usetikzlibrary{cd}
\begin{document}
\begin{tikzcd}
  A \arrow[r, twoheadrightarrow] & A / \sim \arrow[d, "g \circ f"] \\
  C \arrow[r,twoheadrightarrow] & C / \sim''
\end{tikzcd}
\end{document}
```

and stack on the diagram for $h$,

```latex {cmd=true, hide=true, latex_zoom=200%}
\documentclass[tikz]{standalone}
\usetikzlibrary{cd}
\begin{document}
\begin{tikzcd}
  C \arrow[r, twoheadrightarrow] & C / \sim'' \arrow[d, "h"] \\
  D \arrow[r,twoheadrightarrow] & D / \sim'''
\end{tikzcd}
\end{document}
```

to get the following

```latex {cmd=true, hide=true, latex_zoom=200%}
\documentclass[tikz]{standalone}
\usetikzlibrary{cd}
\begin{document}
\begin{tikzcd}
  A \arrow[r, twoheadrightarrow] & A / \sim \arrow[d, "g \circ f"] \\
  C \arrow[r, twoheadrightarrow] & C / \sim'' \arrow[d, "h"] \\
  D \arrow[r,twoheadrightarrow] & D / \sim'''
\end{tikzcd}
\end{document}
```

and then remove the middle and compose $g \circ f$ with $h$ to get $h \circ (g \circ f) = h \circ g \circ f$,

```latex {cmd=true, hide=true, latex_zoom=200%}
\documentclass[tikz]{standalone}
\usetikzlibrary{cd}
\begin{document}
\begin{tikzcd}
  A \arrow[r, twoheadrightarrow] & A / \sim \arrow[d, "h \circ g \circ f"] \\
  D \arrow[r,twoheadrightarrow] & D / \sim'''
\end{tikzcd}
\end{document}
```

and we have the desired diagram, so we have shown that the composition of our morphisms is associative.

We conclude that as defined $\mathsf{MSet}$ is indeed a category. It has $\mathsf{Set}$ as a full subcategory by only considering objects of the type


```latex {cmd=true, hide=true, latex_zoom=200%}
\documentclass[tikz]{standalone}
\usetikzlibrary{cd}
\begin{document}
\begin{tikzcd}
  A \arrow[r, twoheadrightarrow] & A / = 
\end{tikzcd}
\end{document}
```

Where $=$ is the standard equivalence relation, that only elements of a set that are normally considered equal are considered equal. $\quad \square$

****

**3.11.** \(\triangleright\) Draw the relevant diagrams and define composition and identities for the category \(\mathsf{C}^{A, B}\) mentioned in Example 3.9. Do the same for the category \(\mathsf{C}^{\alpha, \beta}\) mentioned in Example 3.10. \(\left[\S5.5, 5.12\right]\)

We define the category $\mathsf{C}^{A,B}$ to have the following objects and morphisms
- $\text{Obj}(\mathsf{C}^{A,B})$ = diagrams

```latex {cmd=true, hide=true, latex_zoom=200%}
\documentclass[tikz]{standalone}
\usetikzlibrary{cd}
\begin{document}
\begin{tikzcd}
A \arrow[rd,"f"] \\
& Z \\
B \arrow[ur,"g", swap]
\end{tikzcd}
\end{document}
```
in $\mathsf{C}$; and
- morphisms are commutative diagrams
```latex {cmd=true, hide=true, latex_zoom=200%}
\documentclass[tikz]{standalone}
\usetikzlibrary{cd}
\begin{document}
\begin{tikzcd}
A \arrow[rd,"f_1",swap] \arrow[rrd,"f_2", bend left] \\
& Z_1 \arrow[r,"\sigma"] & Z_2 \\
B \arrow[ur,"g_1"] \arrow[urr,"g_2",swap, bend right]
\end{tikzcd}
\end{document}
```

Now let's look at another morphism.

```latex {cmd=true, hide=true, latex_zoom=200%}
\documentclass[tikz]{standalone}
\usetikzlibrary{cd}
\begin{document}
\begin{tikzcd}
A \arrow[rd,"f_2",swap] \arrow[rrd,"f_3", bend left] \\
& Z_2 \arrow[r,"\tau"] & Z_3 \\
B \arrow[ur,"g_2"] \arrow[urr,"g_3",swap, bend right]
\end{tikzcd}
\end{document}
```

To compose these two let's first put them side by side,

```latex {cmd=true, hide=true, latex_zoom=200%}
\documentclass[tikz]{standalone}
\usetikzlibrary{cd}
\begin{document}
\begin{tikzcd}
A \arrow[rd,"f_1",swap] \arrow[rrd,"f_2"] \arrow[rrrd,"f_3", bend left] \\
& Z_1 \arrow[r,"\sigma"] & Z_2 \arrow[r,"\tau"] & Z_3 \\
B \arrow[ur,"g_1"] \arrow[urr,"g_2",swap] \arrow[urrr,"g_3", swap, bend right]
\end{tikzcd}
\end{document}
```

then remove the middle and compose $\sigma$ and $\tau$.

```latex {cmd=true, hide=true, latex_zoom=200%}
\documentclass[tikz]{standalone}
\usetikzlibrary{cd}
\begin{document}
\begin{tikzcd}
A \arrow[rd,"f_1",swap] \arrow[rrd,"f_3", bend left] \\
& Z_1 \arrow[r,"\tau \circ \sigma"]  & Z_3 \\
B \arrow[ur,"g_1"] \arrow[urr,"g_3", swap, bend right]
\end{tikzcd}
\end{document}
```

Here's what an identity looks like

```latex {cmd=true, hide=true, latex_zoom=200%}
\documentclass[tikz]{standalone}
\usetikzlibrary{cd}
\begin{document}
\begin{tikzcd}
A \arrow[rd,"f",swap] \arrow[rrd,"f", bend left] \\
& Z_1 \arrow[r,"1"] & Z_1 \\
B \arrow[ur,"g"] \arrow[urr,"g",swap, bend right]
\end{tikzcd}
\end{document}
```

we can compose it with the following morphism

```latex {cmd=true, hide=true, latex_zoom=200%}
\documentclass[tikz]{standalone}
\usetikzlibrary{cd}
\begin{document}
\begin{tikzcd}
A \arrow[rd,"f",swap] \arrow[rrd,"f'", bend left] \\
& Z_1 \arrow[r,"\sigma"] & Z_2 \\
B \arrow[ur,"g"] \arrow[urr,"g'",swap, bend right]
\end{tikzcd}
\end{document}
```

by first putting them side by side,

```latex {cmd=true, hide=true, latex_zoom=200%}
\documentclass[tikz]{standalone}
\usetikzlibrary{cd}
\begin{document}
\begin{tikzcd}
A \arrow[rd,"f",swap] \arrow[rrd,"f"] \arrow[rrrd,"f'", bend left] \\
& Z_1 \arrow[r,"1"] & Z_1 \arrow[r,"\sigma"] & Z_2 \\
B \arrow[ur,"g"] \arrow[urr,"g",swap] \arrow[urrr,"g'", swap, bend right]
\end{tikzcd}
\end{document}
```

and then removing the middle part and composing $1$ and $\sigma$ to get $\sigma \circ 1 = \sigma$

```latex {cmd=true, hide=true, latex_zoom=200%}
\documentclass[tikz]{standalone}
\usetikzlibrary{cd}
\begin{document}
\begin{tikzcd}
A \arrow[rd,"f",swap] \arrow[rrd,"f'", bend left] \\
& Z_1 \arrow[r,"\sigma"] & Z_2 \\
B \arrow[ur,"g"] \arrow[urr,"g'", swap, bend right]
\end{tikzcd}
\end{document}
```

we have another identity

```latex {cmd=true, hide=true, latex_zoom=200%}
\documentclass[tikz]{standalone}
\usetikzlibrary{cd}
\begin{document}
\begin{tikzcd}
A \arrow[rd,"f'",swap] \arrow[rrd,"f'", bend left] \\
& Z_2 \arrow[r,"1"] & Z_2 \\
B \arrow[ur,"g'"] \arrow[urr,"g'",swap, bend right]
\end{tikzcd}
\end{document}
```

we can compose it with the one above by first putting them side by side,

```latex {cmd=true, hide=true, latex_zoom=200%}
\documentclass[tikz]{standalone}
\usetikzlibrary{cd}
\begin{document}
\begin{tikzcd}
A \arrow[rd,"f",swap] \arrow[rrd,"f'"] \arrow[rrrd,"f'", bend left] \\
& Z_1 \arrow[r,"\sigma"] & Z_2 \arrow[r,"1"] & Z_2 \\
B \arrow[ur,"g"] \arrow[urr,"g'",swap] \arrow[urrr,"g'", swap, bend right]
\end{tikzcd}
\end{document}
```

and then removing the middle and composing $\sigma$ and $1$ to get $1 \circ \sigma = \sigma$,

```latex {cmd=true, hide=true, latex_zoom=200%}
\documentclass[tikz]{standalone}
\usetikzlibrary{cd}
\begin{document}
\begin{tikzcd}
A \arrow[rd,"f",swap] \arrow[rrd,"f'", bend left] \\
& Z_1 \arrow[r,"\sigma"] & Z_2 \\
B \arrow[ur,"g"] \arrow[urr,"g'", swap, bend right]
\end{tikzcd}
\end{document}
```

and now we have shown that the identity works on both sides.

We define the category $\mathsf{C}^{\alpha,\beta}$ to have the following objects and morphisms
- $\text{Obj}(\mathsf{C}^{\alpha,\beta}) = $ _commutative diagrams_

```latex {cmd=true, hide=true, latex_zoom=200%}
\documentclass[tikz]{standalone}
\usetikzlibrary{cd}
\begin{document}
\begin{tikzcd}
 & A \arrow[rd,"f"] \\
C \arrow[ur,"\alpha"] \arrow[dr,"\beta",swap] & & Z \\
 & B \arrow[ur,"g", swap]
\end{tikzcd}
\end{document}
```

in $\mathsf{C}$, and

- morphisms are commutative diagrams

```latex {cmd=true, hide=true, latex_zoom=200%}
\documentclass[tikz]{standalone}
\usetikzlibrary{cd}
\begin{document}
\begin{tikzcd}
 & A \arrow[rd,"f_1"] \arrow[rrd, "f_2", bend left] \\
C \arrow[ur,"\alpha"] \arrow[dr,"\beta",swap] & & Z_1 \arrow[r,"\sigma"] & Z_2 \\
 & B \arrow[ur,"g_1", swap] \arrow[rru, bend right, "g_2", swap]
\end{tikzcd}
\end{document}
```

here's another morphism

```latex {cmd=true, hide=true, latex_zoom=200%}
\documentclass[tikz]{standalone}
\usetikzlibrary{cd}
\begin{document}
\begin{tikzcd}
 & A \arrow[rd,"f_2"] \arrow[rrd, "f_3", bend left] \\
C \arrow[ur,"\alpha"] \arrow[dr,"\beta",swap] & & Z_2 \arrow[r,"\tau"] & Z_3 \\
 & B \arrow[ur,"g_2", swap] \arrow[rru, bend right, "g_3", swap]
\end{tikzcd}
\end{document}
```

to compose them we first put them side by side,

```latex {cmd=true, hide=true, latex_zoom=200%}
\documentclass[tikz]{standalone}
\usetikzlibrary{cd}
\begin{document}
\begin{tikzcd}
 & A \arrow[rd,"f_1", swap] \arrow[rrd, "f_2"] \arrow[rrrd, "f_3", bend left] \\
C \arrow[ur,"\alpha"] \arrow[dr,"\beta",swap] & & Z_1 \arrow[r,"\sigma"] & Z_2 \arrow[r,"\tau"] & Z_3 \\
 & B \arrow[ur,"g_1"] \arrow[rru, "g_2", swap] \arrow[rrru, "g_3", bend right, swap]
\end{tikzcd}
\end{document}
```

then compose $\sigma$ and $\tau$ to get $\tau \circ \sigma$ and remove the middle.

```latex {cmd=true, hide=true, latex_zoom=200%}
\documentclass[tikz]{standalone}
\usetikzlibrary{cd}
\begin{document}
\begin{tikzcd}
 & A \arrow[rd,"f_1"] \arrow[rrd, "f_3", bend left] \\
C \arrow[ur,"\alpha"] \arrow[dr,"\beta",swap] & & Z_1 \arrow[r,"\tau \circ \sigma"] & Z_3 \\
 & B \arrow[ur,"g_1", swap] \arrow[rru, bend right, "g_3", swap]
\end{tikzcd}
\end{document}
```

Here's an identity,

```latex {cmd=true, hide=true, latex_zoom=200%}
\documentclass[tikz]{standalone}
\usetikzlibrary{cd}
\begin{document}
\begin{tikzcd}
 & A \arrow[rd,"f_1"] \arrow[rrd, "f_1", bend left] \\
C \arrow[ur,"\alpha"] \arrow[dr,"\beta",swap] & & Z_1 \arrow[r,"1"] & Z_1 \\
 & B \arrow[ur,"g_1", swap] \arrow[rru, bend right, "g_1", swap]
\end{tikzcd}
\end{document}
```

we can compose it with the following morphism

```latex {cmd=true, hide=true, latex_zoom=200%}
\documentclass[tikz]{standalone}
\usetikzlibrary{cd}
\begin{document}
\begin{tikzcd}
 & A \arrow[rd,"f_1"] \arrow[rrd, "f_2", bend left] \\
C \arrow[ur,"\alpha"] \arrow[dr,"\beta",swap] & & Z_1 \arrow[r,"\sigma"] & Z_2 \\
 & B \arrow[ur,"g_1", swap] \arrow[rru, bend right, "g_2", swap]
\end{tikzcd}
\end{document}
```

by first putting the two side by side,

```latex {cmd=true, hide=true, latex_zoom=200%}
\documentclass[tikz]{standalone}
\usetikzlibrary{cd}
\begin{document}
\begin{tikzcd}
 & A \arrow[rd,"f_1", swap] \arrow[rrd, "f_1"] \arrow[rrrd, "f_2", bend left] \\
C \arrow[ur,"\alpha"] \arrow[dr,"\beta",swap] & & Z_1 \arrow[r,"1"] & Z_1 \arrow[r,"\sigma"] & Z_2 \\
 & B \arrow[ur,"g_1"] \arrow[rru, "g_1", swap] \arrow[rrru, "g_2", bend right, swap]
\end{tikzcd}
\end{document}
```

then removing the middle and composing $1$ and $\sigma$ to get $\sigma \circ 1 = \sigma$.

```latex {cmd=true, hide=true, latex_zoom=200%}
\documentclass[tikz]{standalone}
\usetikzlibrary{cd}
\begin{document}
\begin{tikzcd}
 & A \arrow[rd,"f_1"] \arrow[rrd, "f_2", bend left] \\
C \arrow[ur,"\alpha"] \arrow[dr,"\beta",swap] & & Z_1 \arrow[r,"\sigma"] & Z_2 \\
 & B \arrow[ur,"g_1", swap] \arrow[rru, bend right, "g_2", swap]
\end{tikzcd}
\end{document}
```

As you can see we get the original morphism, so the right-sided identy works. Our left-sided identity would be

```latex {cmd=true, hide=true, latex_zoom=200%}
\documentclass[tikz]{standalone}
\usetikzlibrary{cd}
\begin{document}
\begin{tikzcd}
 & A \arrow[rd,"f_2"] \arrow[rrd, "f_2", bend left] \\
C \arrow[ur,"\alpha"] \arrow[dr,"\beta",swap] & & Z_2 \arrow[r,"1"] & Z_2 \\
 & B \arrow[ur,"g_2", swap] \arrow[rru, bend right, "g_2", swap]
\end{tikzcd}
\end{document}
```

we can compose it with the previous morphism by first putting them side by side,

```latex {cmd=true, hide=true, latex_zoom=200%}
\documentclass[tikz]{standalone}
\usetikzlibrary{cd}
\begin{document}
\begin{tikzcd}
 & A \arrow[rd,"f_1", swap] \arrow[rrd, "f_2"] \arrow[rrrd, "f_2", bend left] \\
C \arrow[ur,"\alpha"] \arrow[dr,"\beta",swap] & & Z_1 \arrow[r,"\sigma"] & Z_2 \arrow[r,"1"] & Z_2 \\
 & B \arrow[ur,"g_1"] \arrow[rru, "g_2", swap] \arrow[rrru, "g_2", bend right, swap]
\end{tikzcd}
\end{document}
```

and then removing the middle and composing $\sigma$ and $1$ to get $1 \circ \sigma = \sigma$.

```latex {cmd=true, hide=true, latex_zoom=200%}
\documentclass[tikz]{standalone}
\usetikzlibrary{cd}
\begin{document}
\begin{tikzcd}
 & A \arrow[rd,"f_1"] \arrow[rrd, "f_2", bend left] \\
C \arrow[ur,"\alpha"] \arrow[dr,"\beta",swap] & & Z_1 \arrow[r,"\sigma"] & Z_2 \\
 & B \arrow[ur,"g_1", swap] \arrow[rru, bend right, "g_2", swap]
\end{tikzcd}
\end{document}
```

Clearly this is the original morphism, so the left-sided identity works as well. $\quad \square$

$$
\\
$$