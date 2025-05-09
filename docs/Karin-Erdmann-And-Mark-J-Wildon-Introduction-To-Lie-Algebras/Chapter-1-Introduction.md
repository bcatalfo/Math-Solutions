---
export_on_save:
  html: true
---

<style>
.katex-display { overflow: auto hidden }
</style>

**_Exercise 1.1_**
(i) Show that \( [v, 0] = 0 = [0, v]\) for all \( v \in L \)
**Solution**
Since the Lie bracket is bilinear, we have

$$
[v, 0] = [v, 0 + 0] = [v, 0] + [v, 0]　
$$

and

$$
[0, v] = [0 + 0, v] = [0, v] + [0, v]　
$$

Subtracting \( [v, 0]\) from the first equation and \( [0, v] \) from the second gives the desired result. \( \square\)

---

(ii) Suppose that \( x, y \in L\) satisfy \( [x, y] \neq 0\). Show that \( x \) and \( y \) are linearly independent over \( F \).
**Solution**
The contrapositive of the statement is to assume that \( x \) and \( y \) are linearly dependent over F and prove that \( [x, y] = 0 \). We shall prove the contrapositive. So take \( y=kx \) for some \( k \in F\). Then

$$
[x, y] = [x, kx] = k [x, x] = 0
$$

Since \( [x, x] = 0\) by property (L1). \( \square\)

---

**_Exercise 1.2_**
Let \( F = \mathbf{R} \). The vector product \( (x, y) \mapsto x \wedge y\) defines the structure of a Lie algebra on \(\mathbf{R}^3\). We denote this Lie algebra by \( \mathbf{R}^3\_\wedge\). Explicitly, if \( x=(x_1, x_2, x_3)\) and \( y=(y_1, y_2, y_3)\) then

$$
x \wedge y = (x_2y_3 - x_3y_2, x_3y_1 - x_1y_3, x_1y_2 - x_2y_1)
$$

Convince yourself that \( \wedge \) is bilinear. Then check that the Jacobi identity holds. _Hint_: If \( x \cdot y \) denotes the dot product of the vectors \( x, y \in \mathbb{R}^3 \), then

$$
x \wedge (y \wedge z) = (x \cdot z)y - (x \cdot y)z \quad \text{for all } x,y, z \in \mathbb{R^3}
$$

**Solution**
Let \( a, b \in \mathbb{R} \) and \(x, y, z \in \mathbb{R^3}\). To show that \( \wedge \) is bilinear we must show that

$$
(a x + b y) \wedge z = a (x \wedge z) + b (y \wedge z), \\
z \wedge (a x + b y) = a ( z \wedge x) + b(z \wedge y),
$$

So

$$
\begin{aligned}
(a x + b y) \wedge z &= (ax_1 + by_1, ax_2 + by_2, ax_3 + by_3) \wedge (z_1, z_2, z_3) \\
&= \big((ax_2 + by_2)z_3 - (ax_3 + by_3)z_2, \\
&\quad (ax_3 + by_3)z_1 - (ax_1 + by_1)z_3, \\
&\quad (ax_1 + by_1)z_2 - (ax_2 + by_2)z_1\big) \\
&= \big(a(x_2z_3 - x_3z_2) + b(y_2z_3 - y_3z_2), \\
&\quad a(x_3z_1 - x_1z_3) + b(y_3z_1 - y_1z_3), \\
&\quad a(x_1z_2 - x_2z_1) + b(y_1z_2 - y_2z_1)\big) \\
&= a(x_2z_3 - x_3z_2, x_3z_1 - x_1z_3, x_1z_2 - x_2z_1) \\
&\quad + b(y_2z_3 - y_3z_2, y_3z_1 - y_1z_3, y_1z_2 - y_2z_1) \\
&= a (x \wedge z) + b (y \wedge z)
\end{aligned}
$$

To show that \( z \wedge (a x + b y) = a ( z \wedge x) + b(z \wedge y) \) we could repeat the above but reversed, but there is a shortcut. Calculate that

$$
\begin{aligned}
y \wedge x &= (y_2x_3 - y_3x_2, y_3x_1 - y_1x_3, y_1x_2 - y_2x_1) \\
&= - (y_3x_2 - y_2x_3, y_1x_3 - y_3x_1, y_2x_1 - y_1x_2) \\
&= - (x_2y_3 - x_3y_2, x_3y_1 - x_1y_3, x_1y_2 - x_2y_1) \\
&= - x \wedge y
\end{aligned}
$$

So

$$
z \wedge (a x + b y) = - ((a x + b y) \wedge z) = -(a (x \wedge z) + b (y \wedge z)) = a(z \wedge x) + b(z \wedge y)
$$

Finally we must show that the Jacobi identity holds for \( \wedge \). This is easy using the given identity

$$
x \wedge (y \wedge z) + y \wedge (z \wedge x) + z \wedge (x \wedge y) = ((x \cdot z)y - (x \cdot y)z) + ((y \cdot x)z - (y \cdot z)x) + ((z \cdot y)x - (z \cdot x)y) = 0
$$

\( \square \)

---

**_Exercise 1.3_**
Suppose that \( V \) is a finite-dimensional vector space over \( F \). Write \( \mathrm{gl}(V) \) for the set of all linear maps from \( V \) to \( V \). This is again a vector space over \( F \), and it becomes a Lie algebra, known as the _general linear algebra_, if we define the Lie bracket \( [-, -]\) by

$$
[x, y] \coloneqq x \circ y- y \circ x \quad \text{for } x, y \in \mathrm{gl}(V),
$$

where \( \circ \) denotes the composition of maps. Check that the Jacobi identity holds.
**Solution**
Calculate that

$$
\begin{aligned}
[x, [y, z]] + [y, [z, x]] + [z,[x,y]] &= x \circ [y, z] - [y, z ]\circ x \\
&\quad + y \circ [z, x] - [z, x ] \circ y \\
&\quad + z \circ [x, y] - [x, y] \circ z \\
&= x \circ (y \circ z - z \circ y) - (y \circ z - z \circ y) \circ x \\
&\quad + y \circ (z \circ x - x \circ z) - (z \circ x - x \circ z) \circ y \\
&\quad + z \circ (x \circ y - y \circ x) - (x \circ y - y \circ x) \circ z
\end{aligned}
$$

Of course, the set of all linear maps is... linear!

$$
\begin{aligned}
[x, [y, z]] + [y, [z, x]] + [z,[x,y]] &= x \circ y \circ z - x \circ z \circ y - y \circ z \circ x + z \circ y \circ x \\
&\quad + y \circ z \circ x - y \circ x \circ z - z \circ x \circ y + x \circ z \circ y \\
&\quad + z \circ x \circ y - z \circ y \circ x - x \circ y \circ z + y \circ x \circ z \\
&= 0
\end{aligned}
$$

It seems that all the terms cancelled out nicely! I see why this exercise is famous as one that every mathematician should do at least once in their life :) \( \square \)

---

**_Unnamed Exercise_**
Write \( \mathrm{gl}(n, F)\) for the vector space of all \( n \times n \) matrices over \( F \) with the Lie bracket defined by

$$
[x, y] \coloneqq xy - yx
$$

Where \( xy \) is the usual product of the matrices \( x \) and \( y \).
As a vector space, \( \mathrm{gl}(n, F)\) has a basis consisting of the _matrix units_ \( e*{ij} \) for \( 1 \leq i, j \leq n \). Here \( e*{ij} \) is the \( n \times n \) matrix which has 1 in the \(ij\)-th position and all other entries are 0. We leave it as an exercise to check that

$$
[e_{ij}, e_{kl}] = \delta_{jk}e_{il} - \delta_{il}e_{kj}
$$

where \( \delta \) is the Kronecker delta, defined by \( \delta*{ij} = 1\) if \( i = j \) and \( \delta*{ij} = 0\) otherwise.
**Solution**

$$
[e_{ij}, e_{kl}] = e_{ij}e_{kl} - e_{kl}e_{ij}
$$

Using the formula for matrix multiplication at some index \( 1 \leq a, b \leq n \) we get

$$
(e_{ij}e_{kl})_{ab} = \sum_{x = 0}^{n} (e_{ij})_{ax}\cdot(e_{kl})_{xb}
$$

Whenever \( x \neq j\) by definition we have \( (e*{ij})*{ax} = 0\) so this reduces to

$$
(e_{ij}e_{kl})_{ab} = (e_{ij})_{aj}\cdot(e_{kl})_{jb} = \delta_{ai} \cdot \delta_{kj} \cdot \delta_{lb}
$$

Hence we have

$$
e_{ij}e_{kl} = \delta_{jk} \cdot e_{il}
$$

As by definition \( (e*{il})*{ab} = \delta*{ai} \cdot \delta*{lb}\). Rearranging symbols gives \( e*{kl}e*{ij} = \delta*{li}e*{kj}\), combining the results finishes the proof. \( \square \)

---

**Exercise 1.4**
Check the following assertions:
Let $\mathrm{b}(n,F)$ be the upper triangular matrices in $\mathrm{gl}(n,F)$. (A matrix $x$ is said to be upper triangular if $x_{ij}=0$ whenever $i > j$.) This is a Lie algebra with the same Lie bracket as $\mathrm{gl}(n,F)$.

Similarly, let $\mathrm{n}(n,F)$ be the strictly upper triangular matrices in $\mathrm{gl}(n,F)$. (a matrix $x$ is said to be strictly upper triangular if $x_{ij}=0$ whenever $i \geq j$) Again this is a Lie algebra with the same Lie bracket as $\mathrm{gl}(n,F)$.
**Solution**
Let $x, y$ be upper-triangular matrices. Recall from linear algebra that upper triangular matrices and strictly upper triangular matrices are subspaces of the vector space formed by all square matrices. Therefore, $(xy - yx)$ forms a Lie Algebra over $\mathrm{b}(n,F)$ and $\mathrm{n}(n,F)$, because the required properties of being a bilinear map $[:]:L \to L$ satisfying the properties

$$
\begin{aligned}
[x,x]=0 \quad\text{for all } x \in L, \qquad &(L1) \\
[x,[y,z]] + [y,[z,x]] + [z,[x,y]]=0 \quad \text{for all } x,y,z \in L \qquad &(L2)
\end{aligned}
$$

are inherited from $\mathrm{gl}(n,F)$. $\quad \square$

---

**Exercise 1.5**
Find $Z(L)$ when $L = \mathrm{sl}(2,F)$. You should find that the answer depends on the characteristic of $F$.
**Solution**
First let's just plug in

$$
Z(\mathrm{sl}(2,F)) = \{ x \in \mathrm{sl}(2,F): xy - yx = 0 \text{ for all } y \in \mathrm{sl}(2,F) \}
$$

Now since $x,y \in \mathrm{sl}(2,F)$ we know that their trace is zero

$$
x = \begin{pmatrix}
  x_{11} & x_{12} \\
  x_{21} & -x_{11}
\end{pmatrix}, y = \begin{pmatrix}
  y_{11} & y_{12} \\
  y_{21} & -y_{11}
\end{pmatrix} \\[4pt]
xy = \begin{pmatrix}
  x_{11} & x_{12} \\
  x_{21} & -x_{11}
\end{pmatrix} \cdot \begin{pmatrix}
  y_{11} & y_{12} \\
  y_{21} & -y_{11}
\end{pmatrix} = \begin{pmatrix}
  x_{11}y_{11} + x_{12}y_{21} & x_{11}y_{12} - x_{12}y_{11} \\
  x_{21}y_{11} - x_{11}y_{21} & x_{21}y_{12} + x_{11}y_{11}
\end{pmatrix} \\[4pt]
yx = \begin{pmatrix}
  y_{11} & y_{12} \\
  y_{21} & -y_{11}
\end{pmatrix} \cdot \begin{pmatrix}
  x_{11} & x_{12} \\
  x_{21} & -x_{11}
\end{pmatrix} = \begin{pmatrix}
  y_{11}x_{11} + y_{12}x_{21} & y_{11}x_{12} - y_{12}x_{11} \\
  y_{21}x_{11} - y_{11}x_{21} & y_{21}x_{12} + y_{11}x_{11}
\end{pmatrix} \\[4pt]
xy - yx = \begin{pmatrix}
  x_{12}y_{21} - y_{12}x_{21} & 2x_{11}y_{12} - 2x_{12}y_{11} \\
  2x_{21}y_{11} - 2x_{11}y_{21} & x_{21}y_{12} - y_{21}x_{12}
\end{pmatrix}
$$

So when is $xy - yx = 0$? Can we come up with some generators for this set? Keep in mind we are only picking for $x$, $y$ can be anything.

$$
x_{12}y_{21} = y_{12}x_{21} \\
2x_{11}y_{12} = 2x_{12}y_{11} \\
2x_{21}y_{21} = 2x_{11}y_{21} \\
x_{21}y_{12} = y_{21}x_{12}
$$

Let's look at some examples. Let _F_ be the field of two elements. Then the only requirements for the center become

$$
x_{12}y_{21} = y_{12}x_{21} \\
x_{21}y_{12} = y_{21}x_{12}
$$

So consider the matrix

$$
x = \begin{pmatrix}
  1 & 0 \\
  0 & -1
\end{pmatrix}
$$

This matrix solves the equations above, to show it is in the center explicitly we can show

$$
\begin{pmatrix}
  1 & 0 \\
  0 & -1
\end{pmatrix} \cdot \begin{pmatrix}
  y_{11} & y_{12} \\
  y_{21} & -y_{11}
\end{pmatrix} = \begin{pmatrix}
  y_{11} & y_{12} \\
  -y_{21} & y_{11}
\end{pmatrix} \\[4pt]
\begin{pmatrix}
  y_{11} & y_{12} \\
  y_{21} & -y_{11}
\end{pmatrix} \cdot \begin{pmatrix}
  1 & 0 \\
  0 & -1
\end{pmatrix} = \begin{pmatrix}
  y_{11} & -y_{12} \\
  -y_{21} & y_{11}
\end{pmatrix} \\[4pt]
xy - yx = \begin{pmatrix}
  1 & 0 \\
  0 & -1
\end{pmatrix} \cdot \begin{pmatrix}
  y_{11} & y_{12} \\
  y_{21} & -y_{11}
\end{pmatrix} - \begin{pmatrix}
  y_{11} & y_{12} \\
  y_{21} & -y_{11}
\end{pmatrix} \cdot \begin{pmatrix}
  1 & 0 \\
  0 & -1
\end{pmatrix}\\[4pt]
= \begin{pmatrix}
  y_{11} & y_{12} \\
  -y_{21} & y_{11}
\end{pmatrix} - \begin{pmatrix}
  y_{11} & -y_{12} \\
  -y_{21} & y_{11}
\end{pmatrix} = \begin{pmatrix}
  0 & y_{12} + y_{12} \\
  0 & 0
\end{pmatrix}
$$

Since for all $\lambda \in F_2$ we have $\lambda + \lambda = 0$, in $F_2$ we clearly have $xy - yx = 0$, so $x \in Z(\mathrm{sl}(2, F_2))$. Of course, we always have $0 \in Z(\mathrm{sl}(2,F))$ for all fields $F$, and when the characteristic of $F$ is not 2, this is the only element. $\quad \square$

---

**Exercise 1.6**
Show that if $\varphi : L_1 \to L_2$ is a homomorphism, then the kernel of $\varphi$, $\ker \varphi$, is an ideal of $L_1$, and the image of $\varphi$, $\text{im} \varphi$, is a Lie subalgebra of $L_2$.
**Solution**
First let's show that $\ker \varphi$ is an ideal of $L_1$. The definition of a kernel gives us

$$
\ker \varphi = \{x \in L_1: \varphi(x)=0 \}.
$$

We wish to show that $\ker \varphi$ is an ideal of $L_1$.
First we must show that it is a subspace of $L_1$. This amounts to showing that $\ker \varphi$ contains the zero vector, and is closed under both vector addition and scalar multiplication. $0 \in \ker \varphi \iff \varphi(0) = 0$, the latter following from $\varphi$ being a homomorphism, so $\ker \phi$ contains the zero vector. Let $x, y \in \ker \varphi$ and $c \in F$ (where $F$ is the common field of scalars shared by $L_1$ and $L_2$). Then $\varphi(x + y) = \varphi(x) + \varphi(y) = 0$ and $\varphi(c \cdot x) = c \cdot \varphi(x) = 0$. We conclude that $\ker \varphi$ is a subspace of $L_1$
Let $x \in L_1$ and $y \in \ker \varphi$. To show that $\ker \varphi$ is an ideal of $L_1$, we need to show that $[x, y] \in \ker \varphi$. Calculate that

$$
\varphi ([x,y]) = [\varphi(x), \varphi(y)] = [\varphi(x), 0] = 0 \quad \square
$$

Next we show that $\text{im} \varphi$ is a Lie subalgebra of $L_2$. Recall that

$$
\text{im} \varphi =  \{ y \in L_2: y = \varphi(x), \text{ for some } x \in L_1 \}.
$$

To prove that $\text{im} \varphi$ is a Lie subalgebra of $L_2$, we first need to show that $\text{im} \varphi$ is a vector subspace of $L_2$. Since $\varphi(0)=0$, $0 \in \text{im} \varphi$. If $y_1 = \varphi(x_1), y_2 = \varphi(x_2), c \in F, x_1, x_2 \in L_1$, then $y_1 + y_2 = \varphi(x_1) + \varphi(x_2) = \varphi(x_1 + x_2)$ and $cy_1 = c \varphi(x_1) = \varphi(cx_1)$, so $\text{im} \varphi$ is closed under vector addition and scalar multiplication. We conclude that $\text{im} \varphi$ is a vector subspace of $L_2$.
To show that $\text{im} \varphi$ is a Lie subalgebra of $L_2$, it remains to show that

$$
[y_1, y_2] \in \text{im} \varphi \qquad \text{for all } y_1,y_2 \in \text{im} \varphi
$$

So let $y_1 = \varphi(x_1), y_2 = \varphi(x_2)$. Calculate that

$$
[y_1, y_2] = [\varphi(x_1), \varphi(x_2)] = \varphi([x_1, x_2]) \qquad \square
$$

---

**Exercise 1.7**
Let $L$ be a Lie algebra. Show that the Lie bracket is associative, that is, $[x, [y, z]] = [[x,y],z]$ for all $x, y, z \in L$, if and only if for all $a, b \in L$ the commutator $[a, b]$ lies in $Z(L)$.
**Solution**
First note that

$$
\quad [a,b] \in Z(L) \text{ for all } a,b \in L \iff [[a,b],c] = 0 \text{ for all } a,b,c \in L
$$

Then calculate that

$$
[[a,b],c] = 0 \text{ for all } a,b,c \in L \implies [x,[y,z]] = [[x,y],z] = 0
$$

and that

$$
[x, [y, z]] = [[x,y],z] \text{ for all } x,y,z \in L \\
\implies [[x,y],z] = [x, [y,z]] = -[[y,z],x] = -[y, [z,x]] = [[z,x],y] = [z,[x,y]] = -[[x,y],z] \\
\implies [[x,y],z] = -[[x,y],z] \\
\implies 1 + 1 = 0 \text{ or } [[x,y],z] = 0 \quad \square
$$

---

**Exercise 1.8**
Let $D$ and $E$ be derivations of an algebra $A$.
(i) Show that $[D,E] = D \circ E - E \circ D$ is also a derivation.
**Solution**
Let $a,b \in A$, by the definition of a derivation we have

$$
D(ab) = aD(b) + D(a)b \\
E(ab) = aE(b) + E(a)b
$$

so

$$
[D, E](ab) = D(E(ab)) - E(D(ab)) = D(aE(b)+E(a)b) - E(aD(b) + D(a)b) \\
= D(aE(b)) + D(E(a)b) - E(aD(b)) - E(D(a)b)
$$

We need to show that

$$
[D,E](ab) = a[D,E](b) + [D,E](a)b = a(D(E(b)) - E(D(b))) + (D(E(a))-E(D(a)))b
$$

The result follows from rearranging terms. $\quad \square$

---

(ii) Show that $D \circ E$ need not be a derivation.
**Solution**
By definition $D \circ E$ being a derivation means that for all $a, b \in A$ we have

$$
(D \circ E) (ab) = a(D \circ E)(b) + (D \circ E)(a)b \\
\iff D(E(ab)) = aD(E(b)) + D(E(a))b \\
\iff D(aE(b) + E(a)b) = aD(E(b)) + D(E(a))b \\
\iff D(aE(b)) + D(E(a)b) = aD(E(b)) + D(E(a))b \\
\iff aD(E(b)) + D(a)E(b) + E(a)D(b) + D(E(a))b = aD(E(b)) + D(E(a))b \\
\iff D(a)E(b) + E(a)D(b)  = 0
$$

Let $D$ be ordinary differentiation in the associative algebra $A=C^{\infty}\R$ of infinitely differentiable functions $f,g: \R \to \R$, where the product $fg$ is given by pointwise multiplication: $(fg)(x) = f(x)g(x)$. Then $D \circ D$ being a derivation if and only if for every $a, b \in A$

$$
D(a)D(b) + D(a)D(b) = 0
$$

Take $a,b$ to be the identity functions that is $a(x) = x$, $b(x) = x$ for all $x \in \R$. Then

$$
D(a)D(b) + D(a)D(b) = 1 \cdot 1 + 1 \cdot 1 = 2 \neq 0.
$$

Indeed, we can check explicitly that

$$
(D \circ D)(a^2) = D(D(a^2)) = D(2a) = 2.
$$

If $D \circ D$ was a derivation we would have

$$
(D \circ D)(aa) = a (D \circ D)(a) + (D \circ D)(a) a = 0,
$$

and of course in $\R$ we have $0 \neq 2$ and this counterexample shows that the composition of two derivations is not necessarily a derivation. $\quad \square$

---

**Exercise 1.9**
Let $L_1$ and $L_2$ be Lie algebras. Show that $L_1$ is isomorphic to $L_2$ if and only if there is a basis $B_1$ of $L_1$ and a basis $B_2$ of $L_2$ such that the structure constants of $L_1$ with respect to $B_1$ is equal to the structure constants of $L_2$ with respect to $B_2$.
**Solution**
$\left( \implies \right)$ Let $f: L_1 \to L_2$ be an isomorphism, and let $x_{1}, x_{2}, \ldots, x_{n}$ be a basis of $L_1$ (_hold up- do we know that $L_1$ is finite dimensional?_). (_Check that you can do this_) Then $f(x_1), \ldots, f(x_n)$ is a basis of $L_2$. $L_1$ has structure constants $a_{ij}^k$ such that

$$
[x_i, x_j] = \sum_{n=0}^k a_{ij}^k x_{k} \\[4px]
f([x_i, x_j]) = f\left(\sum_{n=0}^k a_{ij}^k x_{k}\right) \\[4px]
[f(x_i), f(x_j)] = \sum_{n=0}^k f(a_{ij}^k x_k) = \sum_{n=0}^k a_{ij}^k f(x_k) \quad \square \\[4px]
$$

$\left( \impliedby \right)$ Let $B_1 = (x_1, \ldots, x_n)$ be a basis of $L_1$ and let $B_2 = (y_1, \ldots, y_n)$ be a basis of $L_2$, with a shared set of structure constants $a_{ij}^k$. Let $f$ be the unique linear function satisfying

$$
f(x_i) = y_i
$$

Of course $f$ is an isomorphism of vector spaces, what we need to show is that $f$ is also an isomorphism of Lie algebras, that is that $f$ commutes with $[-,-]$, meaning that for all $a, b \in L_1$

$$
f([a,b]) = [f(a), f(b)]
$$

Use our basis to get

$$
a = \lambda_1 x_1 + \cdots + \lambda_n x_n \\
b =\mu_1 x_1 + \cdots \mu_n x_n
$$

Calculate that

$$
f([a,b]) = f([\lambda_1x_1 + \cdots + \lambda_n x_n, \mu_1 x_1 + \cdots \mu_n x_n]) \\[4px]
= f\left(\left[\lambda_1x_1, \sum_{i=1}^n \mu_i x_i \right] + \cdots + \left[\lambda_nx_n, \sum_{i=1}^n \mu_i x_i \right] \right) \\[8px]
= f\left(\sum_{i=1}^n \left[ \lambda_i x_i, \sum_{j=1}^n \mu_j x_j  \right]  \right)
= f\left(\sum_{i=1}^n \sum_{j=1}^n [\lambda_i x_i, \mu_jx_j]\right) \\[8px]
= f\left(\sum_{i=1}^n \sum_{j=1}^n \lambda_i \mu_j [x_i, x_j]\right)
= \sum_{i=1}^n \sum_{j=1}^n \lambda_i \mu_j f([x_i,x_j]) \\[8px]
$$

Recall that by the definition of a structure constant

$$
[x_i, x_j] = \sum_{k=1}^n a_{ij}^k x_k
$$

So we get

$$
f([a,b]) = \sum_{i=1}^n \sum_{j=1}^n \lambda_i \mu_j \sum_{k=1}^n a_{ij}^k x_k
$$

Separately calculate that

$$
[f(a),f(b)] = \left[f\left(\sum_{i=1}^n \lambda_i x_i \right),f\left(\sum_{j=1}^n \mu_j y_j\right)\right]
= \left[ \sum_{i=1}^n \lambda_i f(x_i), \sum_{j=1}^n \mu_j f(x_j) \right] \\[8px]
= \sum_{i=1}^n \sum_{j=1}^n [\lambda_i f(x_i), \mu_j f(x_j)]
= \sum_{i=1}^n \sum_{j=1}^n \lambda_i \mu_j [f(x_i), f(x_j)]
$$

By the definition of $f$ we get

$$
[f(a), f(b)] = \sum_{i=1}^n \sum_{j=1}^n  \lambda_i \mu_j [y_i, y_j]
$$

By the hypothesis $B_1 = (x_1, \dots, x_n)$ and $B_2 = (y_1, \dots, y_n)$ share the same structure constants $a_{ij}^k$ so

$$
[f(a), f(b)] = \sum_{i=1}^n \sum_{j=1}^n \lambda_i \mu_j \sum_{k=1}^n a_{ij}^k x_k
$$

We conclude that for each $a, b \in L_1$ we have

$$
f([a,b]) = [f(a), f(b)] \quad \square
$$

---

**Exercise 1.10**
Let $L$ be a Lie algebra with a basis $(x_1, \dots, x_n)$. What conditions does the Jacobi identity impose on the structure constants $a_{ij}^k$?
**Solution**
Recall that the Jacobi identity states that for all $x, y, z \in L$ we have

$$
[x, [y, z]] + [y, [z, x]] + [z, [x, y]] = 0
$$

and that, for each $i, j \in {1, \dots, n}$, the structure constants satisfy the equation

$$
[x_i, x_j] = \sum_{k=1}^n a_{ij}^k x_k
$$

Take $x = x_i$, $y = x_j$, $z = x_k$. Then

$$
0 = [x,[y,z]] + [y,[z,x]] + [z, [x, y]] = [x_i, [x_j, x_k]] + [x_j, [x_k, x_i]] + [x_k, [x_i, x_j]] \\[8px]
= \left[x_i, \sum_{l=1}^n a_{jk}^l x_l \right] +
\left[x_j, \sum_{l=1}^n a_{ki}^l x_l \right] +
\left[x_k, \sum_{l=1}^n a_{ij}^l x_l \right] \\
= \sum_{l=1}^n a_{jk}^l [x_i, x_l] +
\sum_{l=1}^n a_{ki}^l [x_j,  x_l ] +
\sum_{l=1}^n a_{ij}^l[x_k,  x_l ] \\
= \sum_{l=1}^n a_{ij}^l [x_i, x_l] + a_{ki}^l [x_j,  x_l ] + a_{ij}^l[x_k, x_l] \\
= \sum_{l=1}^n a_{ij}^l \sum_{m=1}^n a_{il}^m x_m + a_{ki}^l \sum_{m=1}^n a_{jl}^mx_m + a_{ij}^l \sum_{m=1}^n a_{ik}^m x_m \\
= \sum_{l=1}^n \sum_{m=1}^n a_{ij}^l  a_{il}^m x_m + a_{ki}^l a_{jl}^mx_m + a_{ij}^l a_{ik}^m x_m \\
= \sum_{m=1}^n \sum_{l=1}^n a_{ij}^l  a_{il}^m x_m + a_{ki}^l a_{jl}^mx_m + a_{ij}^l a_{ik}^m x_m \\
= \sum_{m=1}^n \sum_{l=1}^n (a_{ij}^l  a_{il}^m + a_{ki}^l a_{jl}^m + a_{ij}^l a_{ik}^m)x_m \\
$$

Since $(x_1, \dots, x_n)$ forms a basis they are linearly independent, so for each $m \in 1, \dots, n$ we must have

$$
\sum_{l=1}^n  a_{ij}^l a_{il}^m + a_{ki}^l a_{jl}^m + a_{ij}^l a_{ik}^m = 0
$$

---

**Exercise 1.11**
Let $L_1$ and $L_2$ be two abelian Lie algebras. Show that $L_1$ and $L_2$ are isomorphic if and only if they have the same dimension.
**Solution**
$(\implies)$ If $L_1$ and $L_2$ are isomorphic as Lie algebras than they must be isomorphic as vector spaces $\iff$ they have the same dimension
$(\impliedby)$ If $L_1$ and $L_2$ are the same dimension then we get a vector space isomorphism $f: L_1 \to L_2$. To show that this is a Lie algebra isomorphism, we need to show that for each $a, b \in L_1$ we have

$$
f([a,b]) = [f(a),f(b)]
$$

Since $L_1$ is abelian we have

$$
f([a,b]) = f(0) = 0,
$$

with the last equality coming from the fact that $f$ is a vector space isomorphism. $L_2$ is abelian as well, so

$$
[f(a), f(b)] = 0.
$$

We conclude that $f([a,b]) = [f(a),f(b)]$ for each $a, b \in L_1$, as desired. $\quad \square$

---
