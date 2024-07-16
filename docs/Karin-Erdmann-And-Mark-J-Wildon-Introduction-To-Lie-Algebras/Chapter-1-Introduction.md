---
export_on_save:
  html: true
---
*Exercise 1.1*
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
Subtracting \( [v, 0]\) from the first equation and \( [0, v] \) from the second gives the desired result.
(ii) Suppose that \( x, y \in L\) satisfy \( [x, y] \neq 0\). Show that \( x \) and \( y \) are linearly independent over \( F \).
**Solution**
The contrapositive of the statement is to assume that \( x \) and \( y \) are linearly dependent over F and prove that \( [x, y] = 0 \). We shall prove the contrapositive. So take \( x = ky \) for some \( k \in F\). Then
$$
[x, y] = [x, kx] = k [x, x] = 0
$$
Since \( [x, x] = 0\) by property (L1).