---
export_on_save:
  html: true
---

<style>
.katex-display { overflow: auto hidden }
</style>

**1** &nbsp; Show that \(\alpha + \beta = \beta + \alpha\) for all \(\alpha, \beta \in \mathbf{C}\).
**Solution**
This follows immediately from the definition of \(\mathbf{C}\) and the commutativity of the reals. Let \(\alpha = a + bi\) and \(\beta = c + di\) for \(a, b, c, d \in \R\). Then

$$
\begin{aligned}
\alpha + \beta &= (a + bi) + (c + di) = (a + c) + (b + d)i \\
&= (c + a) + (d + b)i = (c + di) + (a + bi) \\
&= \beta + \alpha. \quad \square
\end{aligned}
$$

---

**2** &nbsp; Show that $(\alpha + \beta) + \lambda = \alpha + (\beta + \lambda)$ for all $\alpha, \beta, \lambda \in \mathbf{C}$.

**Solution**

Let $\alpha = a + bi$, $\beta = c + di$, and $\lambda = e + fi$. Then

$$
(\alpha + \beta) + \lambda = (a + bi + c + di) + e + fi \\
= ((a + c) + (b + d)i) + (e + fi) = (a + c + e) + (b + d + f)i \\
= (a + bi) + ((c + e) + (d + f)i) = \alpha + (\beta + \lambda). \quad \square
$$

---

**3** &nbsp; Show that $(\alpha \beta)\lambda = \alpha(\beta \lambda)$ for all $\alpha, \beta, \lambda \in \mathbf{C}$.

**Solution**

Let $\alpha = a + bi$, $\beta = c + di$, and $\lambda = e + fi$. Then

$$
(\alpha \beta) \lambda = ((a + bi)(c + di)) (e + fi) \\
= ((ac - bd) + (ad + bc)i)(e + fi) \\
= ((ac - bd)e - (ad + bc)f) + ((ac - bd)f + (ad + bc)e)i \\
= (ace - bde - adf - bcf) + (acf - bdf + ade + bce)i.
$$

Calculate separately that

$$
\alpha (\beta \lambda) = (a + bi)((c + di)(e + fi)) \\
= (a + bi)((ce - df) + (cf + de)i) \\
= (a(ce - df) - b(cf + de)) + (a(cf+de) + b(ce-df))i \\
= (ace - adf - bcf - bde) + (acf + ade + bce - bdf)i.
$$

Rearranging terms shows that

$$
(\alpha \beta) \lambda = \alpha (\beta \lambda). \quad \square
$$

---

**4** &nbsp; Show that $\lambda (\alpha + \beta) = \lambda \alpha + \lambda \beta$ for all $\lambda, \alpha, \beta \in \mathbf{C}$.

**Solution**

Let $\alpha = a + bi$, $\beta = c + di$, and $\lambda = e + fi$. Then

$$
\lambda (\alpha + \beta) = (e + fi)((a + bi) + (c + di)) \\
= (e + fi)((a+c) + (b+d)i) \\
= (e(a+c) - f(b+d)) + (e(b+d) + f(a+c))i \\
= (ea + ec -fb - fd) + (eb + ed + fa + fc)i.
$$

Calculate separately that

$$
\lambda \alpha + \lambda \beta = (e + fi)(a + bi) + (e + fi)(c + di) \\
= ((ea - bf) + (eb + fa)i) + ((ec - fd) + (ed + fc)i) \\
= (ea - bf + ec - fd) + (eb + fa + ed + fc)i.
$$

Rearranging terms and the commutative property for reals gives

$$
\lambda(\alpha + \beta) = \lambda \alpha + \lambda \beta. \quad \square
$$

---

**5** &nbsp; Show that for every $\alpha \in \mathbf{C}$, there exists a unique $\beta \in \mathbf{C}$ such that $\alpha + \beta = 0$.

**Solution**

Let $\alpha = a + bi$. Let $\beta = -a - bi$. Clearly $\alpha + \beta = 0$. Let $\beta' = c + di$ satisfy
$$\alpha + \beta' = 0.$$

Plug in,

$$
(a + bi) + (c + di) = 0 \\
(a + c) + (b + d)i = 0 \\
c = -a, \quad d = -b,
$$

so we have

$$
\beta' = \beta
$$

proving uniqueness. $\quad \square$

---

**6** &nbsp; Show that for every $\alpha \in \mathbf{C}$ with $\alpha \neq 0$, there exists a unique $\beta \in \mathbf{C}$ such that $\alpha \beta = 1$.

---

**7** &nbsp; Show that

$$
\frac{-1 + \sqrt{3}i}{2}
$$

is a cube root of $1$ (meaning that its cube equals $1$).

---

**8** &nbsp; Find two distinct square roots of $i$.

---

**9** &nbsp; Find $x \in \mathbf{R}^4$ such that

$$
(4,-3,1,7) + 2x = (5,9,-6,8).
$$

---

**10** &nbsp; Explain why there does not exist $\lambda \in \mathbf{C}$ such that

$$
\lambda(2-3i,5+4i,-6+7i)=(12-5i,7+22i,-32,-9i).
$$

---

**11** &nbsp; Show that $(x+y)+z = x+(y+z)$ for all $x,y,z \in \mathbf{F}^n$.

---

**12** &nbsp; Show that $(ab)x = a(bx)$ for all $x \in \mathbf{F}^n$ and all $a,b \in \mathbf{F}$.

---

**13** &nbsp; Show that $1x = x$ for all $x \in \mathbf{F}^n$.

---

**14** &nbsp; Show that $\lambda(x+y) = \lambda x + \lambda y$ for all $\lambda \in \mathbf{F}$ and all $x,y \in \mathbf{F}^n$.

---

**15** &nbsp; Show that $(a+b)x = ax + bx$ for all $a,b \in \mathbf{F}$ and all $x \in \mathbf{F}^n$.
