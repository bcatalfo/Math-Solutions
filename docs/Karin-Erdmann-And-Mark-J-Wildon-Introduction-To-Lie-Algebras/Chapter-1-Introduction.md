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
(ii) Suppose that \( x, y \in L\) satisfy \( [x, y] \neq 0\). Show that \( x \) and \( y \) are linearly independent over \( F \).
**Solution**
The contrapositive of the statement is to assume that \( x \) and \( y \) are linearly dependent over F and prove that \( [x, y] = 0 \). We shall prove the contrapositive. So take \( x = ky \) for some \( k \in F\). Then
$$
[x, y] = [x, kx] = k [x, x] = 0
$$
Since \( [x, x] = 0\) by property (L1). \( \square\)
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