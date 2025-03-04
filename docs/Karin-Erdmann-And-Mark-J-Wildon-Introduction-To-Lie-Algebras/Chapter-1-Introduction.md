---
export_on_save:
  html: true
---
<style>
.katex-display { overflow: auto hidden }
</style>
***Exercise 1.1***
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
****
(ii) Suppose that \( x, y \in L\) satisfy \( [x, y] \neq 0\). Show that \( x \) and \( y \) are linearly independent over \( F \).
**Solution**
The contrapositive of the statement is to assume that \( x \) and \( y \) are linearly dependent over F and prove that \( [x, y] = 0 \). We shall prove the contrapositive. So take \( y=kx \) for some \( k \in F\). Then
$$
[x, y] = [x, kx] = k [x, x] = 0
$$
Since \( [x, x] = 0\) by property (L1). \( \square\)
****
***Exercise 1.2***
Let \( F = \mathbf{R} \). The vector product \( (x, y) \mapsto  x \wedge y\) defines the structure of a Lie algebra on \(\mathbf{R}^3\). We denote this Lie algebra by \( \mathbf{R}^3_\wedge\). Explicitly, if \( x=(x_1, x_2, x_3)\) and \( y=(y_1, y_2, y_3)\) then
$$
x \wedge y = (x_2y_3 - x_3y_2, x_3y_1 - x_1y_3, x_1y_2 - x_2y_1)
$$
Convince yourself that \( \wedge \) is bilinear. Then check that the Jacobi identity holds. *Hint*: If \( x \cdot y \) denotes the dot product of the vectors \( x, y \in \mathbb{R}^3 \), then
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
****
***Exercise 1.3***
Suppose that \( V \) is a finite-dimensional vector space over \( F \). Write \( \mathrm{gl}(V) \) for the set of all linear maps from \( V \) to \( V \). This is again a vector space over \( F \), and it becomes a Lie algebra, known as the *general linear algebra*, if we define the Lie bracket \( [-, -]\) by
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
****
***Unnamed Exercise***
Write \( \mathrm{gl}(n, F)\) for the vector space of all \( n \times n \) matrices over \( F \) with the Lie bracket defined by
$$
[x, y] \coloneqq xy - yx
$$
Where \( xy \) is the usual product of the matrices \( x \) and \( y \).
As a vector space, \( \mathrm{gl}(n, F)\) has a basis consisting of the *matrix units* \( e_{ij} \) for \( 1 \leq i, j \leq n \). Here \( e_{ij} \) is the \( n \times n \) matrix which has 1 in the \(ij\)-th position and all other entries are 0. We leave it as an exercise to check that
$$
[e_{ij}, e_{kl}] = \delta_{jk}e_{il} - \delta_{il}e_{kj}
$$
where \( \delta \) is the Kronecker delta, defined by \( \delta_{ij} = 1\) if \( i = j \) and \( \delta_{ij} = 0\) otherwise.
**Solution**
$$
[e_{ij}, e_{kl}] = e_{ij}e_{kl} - e_{kl}e_{ij}
$$
Using the formula for matrix multiplication at some index \( 1 \leq a, b \leq n \) we get
$$
(e_{ij}e_{kl})_{ab} = \sum_{x = 0}^{n} (e_{ij})_{ax}\cdot(e_{kl})_{xb} 
$$
Whenever \( x \neq j\) by definition we have \( (e_{ij})_{ax} = 0\) so this reduces to
$$
(e_{ij}e_{kl})_{ab} = (e_{ij})_{aj}\cdot(e_{kl})_{jb} = \delta_{ai} \cdot \delta_{kj} \cdot \delta_{lb}
$$
Hence we have
$$
e_{ij}e_{kl} = \delta_{jk} \cdot e_{il}
$$
As by definition \( (e_{il})_{ab} = \delta_{ai} \cdot \delta_{lb}\). Rearranging symbols gives \( e_{kl}e_{ij} = \delta_{li}e_{kj}\), combining the results finishes the proof. \( \square \)
****
**Exercise 1.4**
Check the following assertions:
Let $\mathrm{b}(n,F)$ be the upper triangular matrices in $\mathrm{gl}(n,F)$. (A matrix $x$ is said to be upper triangular if $x_{ij}=0$ whenever $i > j$.) This is a Lie algebra with the same Lie bracket as $\mathrm{gl}(n,F)$. 

Similarly, let $\mathrm{n}(n,F)$ be the strictly upper triangular matrices in $\mathrm{gl}(n,F)$. (a matrix $x$ is said to be strictly upper triangular if $x_{ij}=0$ whenever $i \geq j$) Again this is a Lie algebra with the same Lie bracket as $\mathrm{gl}(n,F)$.
**Solution**
Let $x, y$ be upper-triangular matrices. Recall from linear algebra that upper triangular matrices and strictly upper triangular matrices are subspaces of the vector space formed by all square matricies. Therefore $(xy - yx)$ forms a Lie Algebra over $\mathrm{b}(n,F)$ and $\mathrm{n}(n,F)$, because the required properties of being a bilinear map $[:]:L \to L$ satisfying the properties
$$
\begin{aligned}
[x,x]=0 \quad\text{for all } x \in L, \qquad &(L1) \\
[x,[y,z]] + [y,[z,x]] + [z,[x,y]]=0 \quad \text{for all } x,y,z \in L \qquad &(L2)
\end{aligned}
$$
are inherited from $\mathrm{gl}(n,F)$. $\quad \square$
****
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
Let's look at some examples. Let *F* be the field of two elements. Then the only requirements for the center become
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
Since for all $\lambda \in F_2$ we have $\lambda + \lambda = 0$, in $F_2$ we clearly have $xy - yx = 0$, so $x \in Z(\mathrm{sl}(2, F_2))$. Of course we always have $0 \in Z(\mathrm{sl}(2,F))$ for all fields $F$, and when the characteristic of $F$ is not 2, this is the only element. $\quad \square$
****
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
****
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
****
**Exercise 1.8**
Let $D$ and $E$ be derviations of an algebra $A$.
(i) Show that $[D,E] = D \circ E - E \circ D$ is also a derivation.
(ii) Show that $D \circ E$ need not be a derivation.