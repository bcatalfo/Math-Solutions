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

**Solution**

Let $\alpha = a + bi$. Then

$$
\alpha \times \overline{\alpha} = (a + bi)(a - bi) = a^2 + b^2
$$

Assume for the purpose of contradiction that $a^2 + b^2 = 0$. Then $a = b = 0$. Then by definition $\alpha = 0$. But we are given $\alpha \neq 0$, a contradiction. Therefore $a^2 + b^2 \neq 0$.

Let

$$
\beta = \frac{a - bi}{a^2 + b^2},
$$

which is well-defined because $a^2 + b^2 \neq 0$. Clearly $\alpha \beta = 1$. What remains to be shown is uniqueness.

Let $\beta' = c + di$ satisfy

$$
\alpha \beta' = 1.
$$

Plug in to get

$$
(a + bi)(c + di) = 1 \\
\iff (ac - bd) + (ad + bc)i = 1 \\
\iff ac - bd = 1 \quad \text{and} \quad ad + bc = 0
$$

$$
ac = 1 + bd \\[4px]
c = \frac{1 + bd}{a} \\[4px]
0 = ad + bc = ad + \frac{b + b^2d}{a} \\
0 = a^2d + b + b^2d \\
a^2d + b^2d = -b \\
d = \frac{-b}{a^2+b^2} \\[4px]
c = \frac{1 + bd}{a} = \frac{1 - \frac{b^2}{a^2+b^2}}{a} = \frac{a^2 + b^2 - b^2}{a(a^2 + b^2)} \\
= \frac{a}{a^2 + b^2}. \quad \square
$$

---

**7** &nbsp; Show that

$$
\frac{-1 + \sqrt{3}i}{2}
$$

is a cube root of $1$ (meaning that its cube equals $1$).

**Solution**
Let $x = \frac{-1 + \sqrt{3}i}{2}$. Calculate that

$$
\left(-1 + \sqrt{3}i\right) \left(-1 + \sqrt{3}i\right) = (1 - 3) + (-\sqrt{3}-\sqrt{3})i \\
= -2 - 2\sqrt{3}i.
$$

And so

$$
\\[1px]
\left(-1 + \sqrt{3}i\right)^3 = \left(-2 - 2\sqrt{3}i\right)\left(-1 + \sqrt{3}i\right) \\
= (2 + 2 \times 3) + \left(-2\sqrt{3} + 2\sqrt{3}\right)i = 8.
$$

Therefore $x^3 = 1$. $\quad \square$

---

**8** &nbsp; Find two distinct square roots of $i$.

**Solution**

$$
(a+bi)(a+bi) = i \\
\iff (a^2-b^2) + (ab + ba)i = i \\
\iff a^2 = b^2 \quad \text{and} \quad 2ab = 1
$$

Consider $\frac{1}{\sqrt{2}} + \frac{1}{\sqrt{2}}i$ and $-\frac{1}{\sqrt{2}} - \frac{1}{\sqrt{2}}i$. Verify that indeed

$$
\left( \frac{1}{\sqrt{2}} + \frac{1}{\sqrt{2}}i \right) \left( \frac{1}{\sqrt{2}} + \frac{1}{\sqrt{2}}i \right) \\[4px]
= \left(\frac{1}{2} - \frac{1}{2}\right) + \left(\frac{1}{2} + \frac{1}{2}\right)i = i. \quad \square
$$

---

**9** &nbsp; Find $x \in \mathbf{R}^4$ such that

$$
(4,-3,1,7) + 2x = (5,9,-6,8).
$$

**Solution**

$$
2x = (1, 12, -7, 1) \\
x = (0.5, 6, -3.5, 0.5). \quad \square
$$

---

**10** &nbsp; Explain why there does not exist $\lambda \in \mathbf{C}$ such that

$$
\lambda(2-3i,5+4i,-6+7i)=(12-5i,7+22i,-32   -9i).
$$

**Solution**

Let $\lambda = a + bi$. Then

$$
12 - 5i = (a + bi)(2 - 3i) = (2a + 3b) + (-3a + 2b)i \\
12 = 2a + 3b \\
-5 = -3a + 2b
$$

Multiply the top equation by three and the bottom by two

$$
36 = 6a + 9b \\
-10 = -6a + 4b,
$$

add both equations together to get

$$
13b = 26 \\
b = 2 \\
12 = 2a + 3 \times 2 \\
12 = 2a + 6 \\
2a = 6 \\
a = 3
$$

So we must have $\lambda = 3 + 2i$. To double check our work calculate that

$$
(3 + 2i)(2 - 3i) = (6 + 6) + (-9 + 4)i = 12 - 5i.
$$

We also need to have

$$
\lambda(5 + 4i) = 7 + 22i.
$$

Calculate that

$$
(3 + 2i)(5 + 4i) = (15 - 8) + (12 + 10)i = 7 + 22i.
$$

Okay, so that one works, but we still got one more to go! We still need

$$
\lambda (-6 + 7i) = -32 - 9i.
$$

Calculate that

$$
(3 + 2i) (-6 + 7i) = (-18 - 14) + (21 - 12)i \\
= -32 + 9i \neq -32 - 9i \quad \square
$$

---

**11** &nbsp; Show that $(x+y)+z = x+(y+z)$ for all $x,y,z \in \mathbf{F}^n$.

**Solution**

Let $x = (x_1, \dots, x_n)$, $y = (y_1, \dots, y_n)$, and $z = (z_1, \dots, z_n)$. Calculate that

$$
(x + y) + z = ((x_1, \dots, x_n) + (y_1, \dots, y_n)) + (z_1, \dots, z_n) \\
= (x_1 + y_1, \dots, x_n + y_n) + (z_1, \dots, z_n) \\
= (x_1 + y_1 + z_1, \dots, x_n + y_n + z_n) \\
= (x_1 + (y_1 + z_1), \dots, x_n + (y_n + z_n)) \\
= (x_1, \dots, x_n) + (y_1 + z_1, \dots, y_n + z_n) \\
= x + (y + z). \quad \square
$$

---

**12** &nbsp; Show that $(ab)x = a(bx)$ for all $x \in \mathbf{F}^n$ and all $a,b \in \mathbf{F}$.

**Solution**

Let $x = (x_1, \dots, x_n)$. Then

$$
(ab)x = (ab)(x_1, \dots, x_n) = ((ab)x_1, \dots, (ab)x_n) \\
= (a(bx_1), \dots, a(bx_n)) = a(bx_1, \dots, bx_n) = a(bx). \quad \square
$$

---

**13** &nbsp; Show that $1x = x$ for all $x \in \mathbf{F}^n$.

---

**14** &nbsp; Show that $\lambda(x+y) = \lambda x + \lambda y$ for all $\lambda \in \mathbf{F}$ and all $x,y \in \mathbf{F}^n$.

---

**15** &nbsp; Show that $(a+b)x = ax + bx$ for all $a,b \in \mathbf{F}$ and all $x \in \mathbf{F}^n$.
