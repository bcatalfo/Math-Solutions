---
export_on_save:
  html: true
---
**Exercise 2.2**
Verify that each of the following examples is in fact a topology.
**(a)** Let \( X \) be any set whatsoever, and let \( \mathcal{T} = \mathcal{P}(X)\) (the ***power set of X***, which is the set of all subsets of \(X \)), so every subset of \(X\) is open. 
**Solution**
Let's verify each axiom one by one.
(i) \( X \) and \( \emptyset \) are elements of \( \mathcal{T}\).
This is obvious as \( X \) and \( \emptyset \) are both subsets of \( X \).
(ii) \( \mathcal{T} \) is closed under finite intersections.
Let \( U_1, \ldots, U_n \) be elements of \( \mathcal{T}\), then  \( U_1 \cap \cdots \cap U_n \subset U_1 \subset X\) so \( U_1 \cap \cdots \cap U_n \in \mathcal{P}(X) = \mathcal{T}\).
(iii) \( \mathcal{T}\) is closed under arbitrary unions.
Let \( (U_\alpha)_{\alpha \in A} \) be a family of elements of \( \mathcal{T}\), and let \( x \in \bigcup_{\alpha \in A} U_\alpha\). Then there must exist \( \alpha \in A\) such that \( x \in U_\alpha \subset X\), so \( x \in X\), hence \( \bigcup_{\alpha \in A} U_\alpha \in \mathcal{T}\). \( \square\)
**(b)** Let \( Y \) be any set, and let \( \mathcal{T} = \{Y, \emptyset \}\).
**Solution**
(i) \( Y \) and \( \emptyset \) are elements of \( \mathcal{T}\).
This is obvious by our definition of \( \mathcal{T}\).
(ii) \( \mathcal{T} \) is closed under finite intersections.
The only intersection we can construct is \( Y \cap \emptyset = \emptyset \in \mathcal{T}\).
(iii) \( \mathcal{T}\) is closed under arbitrary unions.
The only union we can construct is \( Y \cup \emptyset = Y \in \mathcal{T}\). \( \square\)
**(c)** Let \( Z \) be the set \( \{1, 2, 3\}\) and declare the open subsets to be \( \{1\}, \{ 1, 2\}, \{ 1, 2, 3\}\), and the empty set.
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
****
**Exercise 2.4**
**(a)** Suppose that \( M \) is a set and \( d, d'\) are two different metrics on \( M \). Prove that \( d \) and \( d' \) generate the same topology on \( M \) if and only if the following condition is satisfied: for every \( x \in M\) and every \( r > 0\), there exist positive numbers \( r_1 \) and \( r_2\) such that \( B_{r_1}^{(d')}(x) \subseteq B_{r}^{(d)}(x)\) and \(B_{r_2}^{(d)}(x) \subseteq B_{r}^{(d')}(x)\).
**Solution**
Let us denote the metric topologies induced by \( d \) and \( d' \) as \(\mathcal{T}\), \(\mathcal{T'}\), respectively. 
\(\Rightarrow\) Assume that \( \mathcal{T} = \mathcal{T'}\), and take \( x \in M\) and \( r > 0\). Clearly \(B_{r}^{(d)}(x) \in \mathcal{T}\), so by the assumption \(B_{r}^{(d)}(x) \in \mathcal{T'}\). This means that \(B_{r}^{(d)}(x)\) is an open set in the \(d'\) metric topology, so for each \(x' \in B_{r}^{(d)}(x)\) we have an open ball \(B_{r_1}^{(d')}(x') \subseteq B_{r}^{(d)}(x)\) for some \(r_1 > 0\). Since \( x \in B_{r}^{(d)}(x)\) we can take \( x' = x\) giving the desired \(B_{r_1}^{(d')}(x) \subseteq B_{r}^{(d)}(x)\). Using the same logic, the set \(B_{r}^{(d')}(x) \in \mathcal{T'} = \mathcal{T}\) is open in the \(d\) metric giving some \(r_2 > 0\) such that \(B_{r_2}^{(d)}(x) \subseteq B_{r}^{(d')}(x)\).
\(\Leftarrow\) Assume that for every \( x \in M\) and every \( r > 0\), there exist positive numbers \( r_1 \) and \( r_2\) such that \( B_{r_1}^{(d')}(x) \subseteq B_{r}^{(d)}(x)\) and \(B_{r_2}^{(d)}(x) \subseteq B_{r}^{(d')}(x)\). Let \( U \in \mathcal{T}\), so \(U\) is an open set in \(d\)'s metric topology, so for each \(x \in U \) there exists some \( r > 0\) such that \(B_{r}^{(d)}(x) \subseteq U\). By the assumption we have some \(r_1 > 0\) such that \(B_{r_1}^{(d')}(x) \subseteq B_{r}^{(d)}(x) \subseteq U\), so \(U\) is open in the \(d'\) metric, giving \(U \in \mathcal{T'}\). Since this is true for all \(U \in \mathcal{T}\) we have \(\mathcal{T} \subseteq \mathcal{T'}\). Similarly, let \(U' \in \mathcal{T'}\), so for each \(x' \in U'\) we have \(r' > 0\) such that \(B_{r'}^{(d')}(x') \subseteq U'\). By the assumption there exists \(r_2 > 0\) such that \(B_{r_2}^{(d)}(x) \subseteq B_{r'}^{(d')}(x) \subseteq U'\), so \(U'\) is open in the \(d\) metric, yielding \(U' \in \mathcal{T}\). Since this is true for all \(U' \in \mathcal{T'}\) we have \(\mathcal{T'} \subseteq \mathcal{T}\). Combining this with \(\mathcal{T} \subseteq \mathcal{T'}\) gives the desired \(\mathcal{T} = \mathcal{T'}\). \(\square\)
**(b)** Let \((M,d)\) be a metric space, let \(c\) be a positive real number, and define a new metric \(d'\) on \(M\) by \(d'(x,y) = c \cdot d(x,y)\). Prove that \(d\) and \(d'\) generate the same topology on \(M\).
**Solution**
First note that \(d'\) is a metric, because for all \(x, y, z \in M\) we have
*Symmetry*: \(d'(x,y) = c \cdot d(x,y) = c \cdot d(y,x) = d'(y,x)\),
*Positivity*: \(d'(x,y) = c \cdot d(x,y) \geq 0\) as \(d(x,y) \geq 0\) and \(c\) is positive, and \(d'(x,y) = 0 \iff c \cdot d(x,y) = 0 \iff d(x,y) = 0 \iff x = y\), and
*Triangle Inequality*: \(d'(x,y) = c \cdot d(x,y) \leq c \cdot (d(x,y) + d(y,z)) = c \cdot d(x,y) + c \cdot d(y,z) = d'(x,y) + d'(y,z)\). 
We can now continue to the actual problem of showing that \(d\) and \(d'\) generate the same topology on \(M\). To do this we will use the result from part (a). Let \(x \in M\) and \(r > 0\), and let \(r_1 = c \cdot r > 0\) as \(r, c > 0\) and \(r_2 = \frac{r}{c} > 0\). Then 
$$
B_{r_1}^{(d')}(x) = \{y \in M : d'(y, x) < r_1\} = \{y \in M : c \cdot d(y, x) < c \cdot r\} = \{y \in M : d(y, x) < r\} = B_{r}^{(d)}(x)
$$
and
$$
\begin{aligned}
B_{r_2}^{(d)}(x) &= \{y \in M : d(y,x) < r_2\} = \left\{y \in M : d(y,x) < \frac{r}{c}\right\} \\
&= \{y \in M : c \cdot d(y,x) < r\} = \{y \in M : d'(y,x) < r\} = B_{r}^{(d')}(x).
\end{aligned}
$$
So by part (a) \(d\) and \(d'\) generate the same topology on \(M\). \(\square\)
**(c)** Define a metric \(d'\) on \(\mathbb{R^n}\) by \(d'(x,y) = \text{max}\{|x_1 - y_1|, \ldots, |x_n - y_n|\}\). Show that the Euclidean metric and \(d'\) generate the same topology on \(\mathbb{R^n}\). [Hint: see Exercise B.1.]
**Solution**
We begin by showing that \(d'\) is in fact a metric. Take \(x, y, z \in \mathbb{R^n}\), check the following properties of \(d'\):
*Symmetry*: \(d'(x,y) = \text{max}\{|x_1 - y_1|, \ldots, |x_n - y_n|\} = \text{max}\{|y_1 - x_1|, \ldots, |y_n - x_n|\} = d(y,x)\),
*Positivity*: \(d'(x,y) = \text{max}\{|x_1 - y_1|, \ldots, |x_n - y_n|\}\) so for some \(i \in 1, \ldots, n\) we have \(d'(x,y) = |x_i - y_i| \geq 0\) with equality if and only if \( x = y\), and
*Triangle Inequality*: \(d'(x,y) = \text{max}\{|x_1 - y_1|,\ldots,|x_n - y_n|\} \leq \text{max}\{|x_1 - y_1| + |y_1 - z_1|,\ldots,|x_n - y_n| + |y_n - z_n|\}\)
\(\leq \text{max}\{|x_1 - y_1|,\ldots,|x_n - y_n|\} + \text{max}\{|y_1 - z_1|,\ldots,|y_n - z_n|\} = d'(x,y) + d'(y,z)\).
Then note Exercise B.1. says that for any \(x = (x_1, \ldots, x_n) \in \mathbb{R^n}\):
$$
\text{max}\{|x_1|,\ldots,|x_n|\} \leq |x| \leq \sqrt{n} \text{max}\{|x_1|,\ldots,|x_n|\}.
$$
So in particular
$$
\text{max}\{|x_1 - y_1|,\ldots,|x_n - y_n|\} \leq |x - y| \leq \sqrt{n} \text{max}\{|x_1 - y_1|,\ldots,|x_n - y_n|\}.
$$
Using the definition of \(d'\) and notating the usual Euclidean metric as \(d\)
$$
d'(x,y) \leq d(x,y) \leq \sqrt{n} \cdot d'(x,y).
$$
By symmetry,
$$
d'(y,x) \leq d(y,x) \leq \sqrt{n} \cdot d'(y,x).
$$
Now we can finally prove that \(d\) and \(d'\) generate the same topology on \(\mathbb{R^n}\) by utilizing part (a). Let \(x \in \mathbb{R^n}\) and \(r > 0\), pick \(r_1 = \frac{r}{\sqrt{n}}> 0\) and \(r_2 = r > 0\). Then
$$
B_{r_1}^{(d')}(x) = \{y \in \mathbb{R^n} : d'(y,x) < r_1\} = \left\{y \in \mathbb{R^n} : d'(y,x) < \frac{r}{\sqrt{n}}\right\} = \{y \in \mathbb{R^n} : \sqrt{n} \cdot d'(y,x) < r\}.
$$ 
Let \(y' \in B_{r_1}^{(d')}(x)\), then \(d(y',x) \leq \sqrt{n} \cdot d'(y',x) < r\), so \(y' \in B_{r}^{(d)}(x)\), yielding \(B_{r_1}^{(d')}(x) \subseteq B_{r}^{(d)}(x)\). We also have
$$
B_{r_2}^{(d)}(x) = \{y \in \mathbb{R^n} : d(y,x)<r_2\} = \{y \in \mathbb{R^n} : d(y,x)<r\}.
$$
Let \(y \in B_{r_2}^{(d)}(x)\), then \(d'(y,x) \leq d(y,x) < r \), so \(y \in B_{r}^{(d')}(x)\), yielding \(B_{r_2}^{(d)} \subseteq B_{r}^{(d')}(x)\). So by part (a) \(d\) and \(d'\) generate the same topology on \(\mathbb{R^n}\). \(\square\)
**(d)** Let \(X\) be any set, and let \(d\) be the discrete metric on \(X\) (see Example B.3(c)). Show that \(d\) generates the discrete topology.
**Solution**
From Example B.3(c) we have the definition of the discrete metric: \(d(x,y) = 1\) unless \(x = y\), in which case \(d(x,y)=0\). Next from Example 2.1 the discrete topology is defined by letting \(\mathcal{T} = \mathcal{P}(X)\).