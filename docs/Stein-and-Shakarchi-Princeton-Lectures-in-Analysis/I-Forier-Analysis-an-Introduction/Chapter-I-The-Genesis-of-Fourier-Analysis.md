---
export_on_save:
  html: true
---

<style>
.katex-display { overflow: auto hidden }
</style>
**Exercises**
**1.** If \(z = x + iy\) is a complex number with \(x, y \in \mathbb{R}\), we define
$$
|z| = (x^2 + y^2)^{1/2}
$$
and call this quantity the **modulus** or **absolute value** of \(z\).
\(\quad \text{(a)}\) What is the geometric interpretation of \(|z|\)?
**Solution**
The geometric interpretation of \(|z|\) is the length of the vector \(z\).
\(\quad \text{(b)}\) Show that if \(|z| = 0\), then \(z = 0\).
**Solution**
If \(|z| = 0\) then by definition \(0 = (x^2 + y^2)^{1/2} \implies 0 = x^2 + y^2 \implies x = y = 0\). \(\square\)
\(\quad \text{(c)}\) Show that if \(\lambda \in \R\), then \(|\lambda z| = |\lambda||z|\), where \(|\lambda|\) denotes the standard absolute value of a real number.
**Solution**
Calculate that \(\lambda z = \lambda x + i \lambda y\), so \(|\lambda z| = ((\lambda x)^2 + (\lambda y)^2 )^{1/2} = |\lambda||z|\). \(\square\)
\(\quad \text{(d)}\) If \(z_1\) and \(z_2\) are two complex numbers, prove that
$$
|z_1z_2| = |z_1||z_2| \quad \text{and} \quad |z_1 + z_2| \leq |z_1| + |z_2|.
$$
**Solution**
Let \(z_1 = x_1 + iy_1\) and \(z_2 = x_2 + iy_2\). Calculate that \(z_1 \cdot z_2 = (x_1 + iy_1) \cdot (x_2 + iy_2) = x_1x_2 + ix_1y_2 + iy_1x_2 - y_1y_2 = (x_1x_2 - y_1y_2) + i(x_1y_2 + y_1x_2)\). So \(|z_1z_2|^2 = |(x_1x_2 - y_1y_2) + i(x_1y_2 + y_1x_2)|^2 = (x_1x_2-y_1y_2)^2 + (x_1y_2 + y_1x_2)^2 = x_1^2x_2^2 - 2x_1x_2y_1y_2 + y_1^2y_2^2 + x_1^2y_2^2 + 2x_1x_2y_1y_2 + y_1^2x_2^2 = x_1^2x_2^2 + y_1^2y_2^2 + x_1^2y_2^2 + y_1^2x_2^2\).
Calculate separately that \((|z_1||z_2|)^2 = ((x_1^2 + y_1^2)^{1/2} \cdot (x_2^2+y_2^2)^{1/2})^2 = (x_1^2 + y_1^2)(x_2^2+y_2^2) = x_1^2x_2^2 + x_1^2y_2^2 + y_1^2x_2^2 + y_1^2y_2^2\).
Therefore \(|z_1z_2|^2 = (|z_1||z_2|)^2\). Since both \(|z_1z_2|\) and \(|z_1||z_2|\) are non-negative we can conclude that\(|z_1z_2| = |z_1||z_2|\).
For the inequality we need to show that
$$
|z_1 + z_2| \leq |z_1| + |z_2| \\
\iff |(x_1 + x_2) + i(y_1+y_2)| \leq |x_1 + iy_1| + |x_2 + iy_2| \\
\iff \sqrt{(x_1 + x_2)^2 + (y_1 + y_2)^2 } \leq \sqrt{x_1 ^ 2 + y_1^2} + \sqrt{x_2^2 + y_2^2} \\
\iff (x_1 + x_2)^2 + (y_1+y_2)^2 \leq (x_1^2 + y_1^2) + 2\sqrt{(x_1^2+y_1^2)(x_2^2+y_2^2)} + (x_2^2 + y_2^2) \\
\iff 2x_1x_2 + 2y_1y_2 \leq 2\sqrt{(x_1^2+y_1^2)(x_2^2+y_2^2)} \\
\iff x_1x_2 + y_1y_2 \leq \sqrt{(x_1^2+y_1^2)(x_2^2+y_2^2)} \\
\iff x_1^2x_2^2 + 2x_1x_2y_1y_2 +y_1^2y_2^2 \leq (x_1^2+y_1^2)(x_2^2+y_2^2) \\
\iff x_1^2x_2^2 + 2x_1x_2y_1y_2 +y_1^2y_2^2 \leq x_1^2x_2^2 + x_1^2y_2^2 + y_1^2x_2^2 + y_1^2y_2^2 \\
\iff 2x_1x_2y_1y_2 \leq x_1^2y_2^2 + y_1^2x_2^2 \\
\iff 0 \leq x_1^2y_2^2 - 2x_1x_2y_1y_2 + y_1^2x_2^2\\
\iff 0 \leq (x_1y_2 - y_1x_2)^2 \\ \square
$$
\(\quad \text{(e)}\) Show that if \(z \neq 0\), then \(|1/z| = 1/|z|\).
**Solution**
Using the previous result
$$
|1/z||z| = |1/z \cdot z| = |1| = 1
$$
Dividing both sides by \(|z|\) (which we know isn't zero thanks to \(\text{(b)}\) ) gives the result. \(\square\)
****
**2.** If \(z = x + iy\) is a complex number with \(x, y \in \R\), we define the **complex conjugate** of \(z\) by
$$
\overline{z} = x - iy.
$$
\(\quad \text{(a)}\) What is the geometric interpretation of \(\overline{z}\)?
**Solution**
The geometric interpetation of \(\overline{z}\) is a reflection of the vector \(z\) over the \(x\)-axis.
\(\quad \text{(b)}\) Show that \(|z|^2 = z\overline{z}\).
**Solution**
$$
z\overline{z} = (x + iy)(x - iy) = x^2 + y^2 = |z|^2 \quad \square
$$
\(\quad \text{(c)}\) Prove that if \(z\) belongs to the unit circle, then \(1/z = \overline{z}\).
**Solution**
If \(z\) belongs to the unit circle that means that \(|z| = 1\). Using part \(\text{(b)}\) we get that \(z\overline{z} = |z|^2 = 1\). Diving both sides by \(z\) gives the result. \(\square\)
****