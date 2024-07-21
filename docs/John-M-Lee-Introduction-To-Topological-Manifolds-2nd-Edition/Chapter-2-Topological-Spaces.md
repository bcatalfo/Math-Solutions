---
export_on_save:
  html: true
---
<style>
.katex-display { overflow: auto hidden }
</style>
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
From Example B.3(c) we have the definition of the discrete metric: \(d(x,y) = 1\) unless \(x = y\), in which case \(d(x,y)=0\). Next from Example 2.1 the discrete topology is defined by letting \(\mathcal{T} = \mathcal{P}(X)\). Let \(U \subseteq X\) and let \(x \in U\). We need to show that \(U\) is open under the discrete metric, which is equivalent to showing that for some \(r > 0\) we have \(B_{r}^{(d)}(x) \subseteq U\). Let \( r = \frac{1}{2}\). Then
$$
B_{r}^{(d)}(x) = \{y \in X: d(y,x) < r\} = \left\{y \in X: d(y,x) < \frac{1}{2}\right\}.
$$
Since \(y \neq x \Rightarrow d(y,x) = 1 > \frac{1}{2}\) and \(y = x \Rightarrow d(y,x) = 0 < \frac{1}{2}\), we get 
$$
B_{r}^{(d)}(x) = \{x\} \subseteq U. 
$$
Therefore each \(U \subseteq X\) is open in \(d\) so \(\mathcal{T} = \mathcal{P}(X)\), the set of all subsets of \(X\), a.k.a the discrete topology. \(\square\)
**(e)** Show that the discrete metric and the Euclidean metric generate the same topology on the set \(\mathbb{Z}\) of integers.
**Solution**
By part (d) the discrete metric generates the discrete topology, so it suffices to show that the Euclidean metric does the same. We can actually solve this the same way we did (d), that is by taking \(U \subseteq \mathbb{Z}\), \(x \in U\), and \(r = \frac{1}{2}\). We then have (letting \(d\) denote the Euclidean metric)
$$
B_{r}^{(d)}(x) = \{y \in \mathbb{Z} : d(y,x)<r\} = \left\{y \in \mathbb{Z} : d(y,x)<\frac{1}{2}\right\}
$$
Of course since we are in \(\mathbb{Z}\) the nearest integers to \(y\) other than \(y\) itself are \(y + 1\) and \(y - 1\), and of course \(d(y+1,y) = d(y-1,y) = 1 > \frac{1}{2}\). So
$$
B_{r}^{(d)}(x) = \{x\} \subseteq U,
$$
meaning that each \(U \subseteq Z\) is open in the Euclidean metric, generating the discrete topology \(\mathcal{T} = \mathcal{P}(\mathbb{Z})\). \(\square\)
****
**Exercise 2.5.** Suppose \(X\) is a topological space and \(Y\) is an open subset of \(X\). Show that the collection of all open subsets of \(X\) that are contained in \(Y\) is a topology on \(Y\).
**Solution**
Let \(\mathcal{T}\) denote the open subsets of \(X\) and let 
$$
\mathcal{T}_Y \coloneqq \{U \in \mathcal{T} : U \subseteq Y\}.
$$
We need to use the fact that \(\mathcal{T}\) is a topology on \(X\) and that \(Y \in \mathcal{T}\) to show that \(\mathcal{T}_Y\) is a topology on \(Y\). There are three properties that we need to show:
(i) \(Y\) and \(\emptyset\) are elements of \(\mathcal{T}_Y\).
It is obvious that \(Y \in \mathcal{T}_Y\) as it is given that \(Y \in \mathcal{T}\) and clearly \(Y \subseteq Y\). Since \(\mathcal{T}\) is a topology we must have \(\emptyset \in \mathcal{T}\), combining this with the fact that \(\emptyset \subseteq Y\) as the empty set is a subset of all sets we get \(\emptyset \in \mathcal{T}_Y\).
(ii) \(\mathcal{T}_Y\) is closed under finite intersections.
Let \(U_1,\ldots,U_n \in \mathcal{T}_Y\). By the definition of \(\mathcal{T}_Y\) we have \(U_1,\ldots,U_n \in \mathcal{T}\). Since \(\mathcal{T}\) is a topology we have \(U_1 \cap\ldots\cap U_n \in \mathcal{T}\). The definition of \(\mathcal{T}_Y\) tells us that \(U_1,\ldots,U_n \subseteq Y\) so \(U_1 \cap \ldots \cap U_n \subseteq Y\). So by the definition of \(\mathcal{T}_Y\) we have \(U_1 \cap \cdots \cap U_n \in \mathcal{T}_Y\).   
(iii) \(\mathcal{T}_Y\) is closed under arbitrary unions.
Let \((U_\alpha)_{\alpha \in A}\) be any (finite or infinite) family of elements of \(\mathcal{T}_Y\). Since this is also a family of elements in \(\mathcal{T}\) which is a topology we have \(\bigcup_{\alpha \in A}U_\alpha \in \mathcal{T}\). Let \(x \in \bigcup_{\alpha \in A}U_\alpha\), then for some \(\alpha \in A\) we have \(x \in U_\alpha \subseteq Y\), so \(\bigcup_{\alpha \in A}U_\alpha \subseteq Y\). We conclude that \(\bigcup_{\alpha \in A}U_\alpha \in \mathcal{T}_Y\). \(\square\)
****
**Exercise 2.6** Let \(X\) be a set, and suppose \(\{\mathcal{T}_\alpha\}_{\alpha \in A}\) is a collection of topologies on \(X\). Show that the intersection \(\mathcal{T} = \bigcap_{\alpha \in A}\mathcal{T}_\alpha\) is a topology on \(X\). (The open subsets in this topology are exactly those subsets of \(X\) that are open in each of the topologies \(\mathcal{T}_\alpha\).)
**Solution**
To show that \(\mathcal{T}\) is a topology we need to show the following properties:
(i) \(X\) and \(\emptyset\) are elements of \(\mathcal{T}\).
Let \(\alpha \in A\), since \(\mathcal{T}_\alpha\) is a topology on \(X\) we have \(X, \emptyset \in \mathcal{T}_\alpha\). Since this holds for all \(\alpha \in A\) we have \(X, \emptyset \in \bigcap_{\alpha \in A}\mathcal{T}_\alpha = \mathcal{T}\).
(ii) \(\mathcal{T}\) is closed under finite intersections.
Let \(U_1, \ldots, U_n \in \mathcal{T} = \bigcap_{\alpha \in A}\mathcal{T}_\alpha\). Let \(\alpha \in A\). By the definition of intersection we have \(U_1, \ldots, U_n \in \mathcal{T}_\alpha\). Since \(\mathcal{T}_\alpha\) is a topology we have \(U_1 \cap \cdots \cap U_n \in \mathcal{T}_\alpha\). Since this holds for all \(\alpha \in A\) we have \(U_1 \cap \cdots \cap U_n \in \bigcap_{\alpha \in A}\mathcal{T}_\alpha = \mathcal{T}\).
(iii) \(\mathcal{T}\) is closed under arbitrary unions.
Let \((U_\beta)_{\beta \in B}\) be any (finite or infinite) family of elements of \(\mathcal{T} = \bigcap_{\alpha \in A}\mathcal{T_\alpha}\). Let \(\alpha \in A\) and \( \beta \in B\), we have \(U_\beta \in \mathcal{T_\alpha}\). Since \(\mathcal{T_\alpha}\) is a topology we have \(\bigcup_{\beta \in B}U_\beta \in \mathcal{T}_\alpha\). Since this holds for all \(\alpha \in A\) we have \(\bigcup_{\beta \in B}U_\beta \in \bigcap_{\alpha \in A}\mathcal{T}_\alpha = \mathcal{T}\). \(\square\) 
****
**Exercise 2.9.** Let \(X\) be a topological space and let \(A \subseteq X\) be any subset. Prove the following:
**(a)** A point is in \(\text{Int} A\) if and only if it has a neighborhood contained in \(A\).
By definition
$$
\text{Int} A = \bigcup \{C \subseteq X : C \subseteq A \text{ and } C \text{ is open in } X\}.
$$
\(\Rightarrow\) If \(x \in \text{Int} A\) then \(x \in C \) for some open \(C \subseteq A\) and \(C\) is open in \(X\). This is our desired neighborhood (in this book a neighborhood of a point is by definition an open subset containing it). 
\(\Leftarrow\) If \(x'\) has a neighborhood contained in \(A\) that means that \(x \in C'\) for some \(C' \subseteq A\) where \(C'\) is open in \(X\). Since \(A \subseteq X\) we have \(C' \subseteq X\) so by definition \(x' \in \text{Int} A\). \(\square\)
**(b)** A point is in \(\text{Ext} A\) if and only if it has a neighborhood contained in \(X \setminus A\).
By definition the exterior of \(A\) is
$$
\text{Ext} A = X \setminus \overline{A}
$$
and the closure of \(A\) is
$$
\overline{A} = \bigcap \{B \subseteq X : B \supseteq A \text{ and } B \text{ is closed in } X \}.
$$
\(\Rightarrow\) Take \(x \in \text{Ext} A\), then by definition of the exterior \(x \notin \overline{A}\). Then by the definition of the closure there must be some \(B \supseteq A\) that is closed in \(A\) and \(x \notin B\). Now consider the set \(X \setminus B\). Since \(B\) is closed by definition \(X \setminus B\) is open. Additionally, since \(x \in X\) and \(x \notin B\) we have \(x \in X \setminus B\). Finally, note that since \(B \supseteq A\) we have \(X \setminus B \subseteq X \setminus A\). Therefore, \(X \setminus B\) is our desired neighborhood.
\(\Leftarrow\) Take \(x \in C \subseteq X \setminus A\) with \(C\) open. Then \(X \setminus C\) is closed and \(X \setminus C \supseteq A\). However, \(x \notin X \setminus C\) so \(x \notin \overline{A}\) so \(x \in \text{Ext} A\). \(\square\)
**(c)** A point is in \(\partial A\) if and only if every neighborhood of it contains both a point of \(A\) and a point of \(X \setminus A\).
Recall that the boundary of \(A\) is defined as
$$
\partial A = X \setminus (\text{Int} A \cup \text{Ext} A)
$$
\(\Rightarrow\) Let \(x \in \partial A\). It follows immediately from this definition that \(x \notin \text{Int} A\) and \(x \notin \text{Ext} A\). Let \(C\) be an open set in \(X\) such that \(x \in C\). Since \(x \notin \text{Int} A\) we must have \(C \nsubseteq A\), so there exists \(y \in C\) such that \(y \notin A\), or equivalently \(y \in X \setminus A\). Since \(x \notin \text{Ext} A\) and \(\text{Ext} A = X \setminus \overline{A}\), we have \(x \in \overline{A}\). \(C\) is open so \(X \setminus C\) is closed. Assume that there is no \(z \in C\) such that \(z \in A\). Then \(X \setminus C \supseteq A \), so since \(x \in \overline{A}\) we have \(x \in X \setminus C\), contradicting \(x \in C\). Therefore, our assumption was wrong and there does exist some \(z \in C\) such that \(z \in A\).
\(\Leftarrow\) Let \(x \in X\) such that for each open \(C \subseteq X\) we have \(y, z \in C\) such that \(y \in A\) and \(z \in X \setminus A\). Therefore, \(x\) has no neighborhood contained in \(A\) and no neighborhood contained in \(X \setminus A\). Part (a) tells us that \(x \notin \text{Int}A\) and part (b) tells us that \(x \notin \text{Ext} A\). Therefore, \(x \in X \setminus (\text{Int}A \cup \text{Ext} A) = \partial A\).
**(d)** A point is in \(\overline{A}\) if and only if every neighborhood of it contains a point of \(A\).
**(e)** \(\overline{A} = A \cup \partial A = \text{Int} A \cup \partial A\).
**(f)** \(\text{Int} A\) and \(\text{Ext} A\) are open in \(X\), while \(\overline{A}\) and \(\partial A\) are closed in \(X\).
**(g)** The following are equivalent:
* \(A\) is open in \(X\).
* \(A = \text{Int} A\).
* \(A\) contains none of its boundary points.
* Every point of \(A\) has a neighborhood contained in \(A\).

**(h)** The following are equivalent:
* \(A\) is closed in \(X\).
* \(A = \overline{A}\).
* \(A\) contains all of its boundary points.
* Every point of \(X \setminus A\) has a neighborhood contained in \(X \setminus A\).
****