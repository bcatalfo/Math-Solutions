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
****
\(\quad \text{(b)}\) Show that if \(|z| = 0\), then \(z = 0\).
**Solution**
If \(|z| = 0\) then by definition \(0 = (x^2 + y^2)^{1/2} \implies 0 = x^2 + y^2 \implies x = y = 0\). \(\square\)
****
\(\quad \text{(c)}\) Show that if \(\lambda \in \R\), then \(|\lambda z| = |\lambda||z|\), where \(|\lambda|\) denotes the standard absolute value of a real number.
**Solution**
Calculate that \(\lambda z = \lambda x + i \lambda y\), so \(|\lambda z| = ((\lambda x)^2 + (\lambda y)^2 )^{1/2} = |\lambda||z|\). \(\square\)
****
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
****
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
****
\(\quad \text{(b)}\) Show that \(|z|^2 = z\overline{z}\).
**Solution**
$$
z\overline{z} = (x + iy)(x - iy) = x^2 + y^2 = |z|^2 \quad \square
$$
****
\(\quad \text{(c)}\) Prove that if \(z\) belongs to the unit circle, then \(1/z = \overline{z}\).
**Solution**
If \(z\) belongs to the unit circle that means that \(|z| = 1\). Using part \(\text{(b)}\) we get that \(z\overline{z} = |z|^2 = 1\). Diving both sides by \(z\) gives the result. \(\square\)
****
**3.** A sequence of complex numbers \(\{w_n\}_{n=1}^{\infty}\) is said to converge if there exists \(w \in \mathbb{C}\) such that
$$
\lim_{n \to \infty} |w_n - w| = 0,
$$
and we say that \(w\) is a limit of the sequence.
\(\quad \text{(a)}\) Show that a converging sequence of complex numbers has a unique limit.
**Solution**
Let \(x, y\) be limits of \(\{w_n\}_{n=1}^\infty\)
$$
0 = \lim_{n \to \infty}|w_n - x| = \lim_{n \to \infty}|w_n - y| \\
$$
So
$$
\begin{aligned}
|x - y| &= \lim_{n \to \infty} |x - y| = \lim_{n \to \infty} |x - w_n + w_n - y| \\
&\leq \lim_{n \to \infty} |x - w_n| + |w_n - y| \quad \text{(using 1 (d))} \\
&= \lim_{n \to \infty} |w_n - x| + |w_n - y| \\
&=  \lim_{n \to \infty}|w_n - x| + \lim_{n \to \infty}|w_n - y| \\
&= 0 + 0 = 0 \\
\end{aligned}
$$
This shows that \(|x - y| \leq 0\), we also have \(|x - y| \geq 0\) by the definition of \(|\cdot|\) so we have \(|x - y| = 0\). Using \(\text{1 (b)}\) we get \(x - y = 0 \implies x = y\) so any two limits of a converging sequence of complex numbers are equal, hence this limit is unique. \(\square\)
****
The sequence \(\{w_n\}_{n=1}^\infty\) is said to be a **Cauchy sequence** if for every \(\epsilon > 0\) there exists a positive integer \(N\) such that
$$
|w_n - w_m| < \epsilon \quad \text{whenever } n, m > N.
$$
\(\quad \text{(b)}\) Prove that a sequence of complex numbers converges if and only if it is a Cauchy sequence. [Hint: A similar theorem exists for the convergence of a sequence of real numbers. Why does it carry over to sequences of complex numbers?]
**Solution**
$$
\lim_{n \to \infty} |w_n - w| = 0 \iff \lim_{n \to \infty} |x_n + iy_n - (x + iy)| = 0 \\
\iff \lim_{n \to \infty} |x_n  - x + i(y_n + y)| = 0  \\
\iff \lim_{n \to \infty} |x_n - x| = 0 \text{ and } \lim_{n \to \infty} |y_n - y| = 0 \\
\iff |{x_n}_a - {x_n}_b| < \epsilon \quad \text{ whenever } a, b > N_1 \text{ and } \\
|{y_n}_a - {y_n}_b| < \epsilon \quad \text{ whenever } a, b > N_2
$$
$$
|w_n - w_m| < \epsilon \iff |x_n + iy_n - (x_m + iy_m)| < \epsilon \\
\iff |x_n - x_m + i(y_n - y_m)| < \epsilon \\
\iff |x_n - x_m| < \epsilon \text{ and } |y_n - y_m| < \epsilon \\
$$
****
A series \(\sum_{n=1}^\infty z_n\) of complex numbers is said to converge if the sequence formed by the partial sums
$$
S_N = \sum_{n=1}^N z_n
$$
converges. Let \(\{a_n\}_{n=1}^\infty\) be a sequence of non-negative real numbers such that the series \(\sum_{n}a_n\) converges.
\(\quad \text{(c)}\) Show that if \(\{z_n\}_{n=1}^\infty\) is a sequence of complex numbers satisfying \(|z_n| \leq a_n\) for all \(n\), then the series \(\sum_{n} z_n\) converges. [Hint: Use the Cauchy criterion.]
**Solution**
Start with the Cauchy criterion for \(\sum_{n}a_n\). For any \(\epsilon > 0\) there exists \(n\) such that for all \(N, M > K\) we have
$$
\epsilon > |A_N - A_M| = \left|\sum_{n=1}^N a_n - \sum_{m=1}^M a_m \right| = \left|\sum_{j=\text{min}(N, M)}^{\text{max}(N, M)} a_j\right|
$$
Finish with the Cauchy criterion for \(\sum_{n}z_n\)
$$
|S_N - S_M| = \left|\sum_{n=1}^N z_n - \sum_{m=1}^M z_m\right| = \left|\sum_{j=\text{min}(N, M)}^{\text{max}(N, M)} z_j\right| \\
\leq \sum_{j=\text{min}(N, M)}^{\text{max}(N, M)} |z_j| \leq \sum_{j=\text{min}(N, M)}^{\text{max}(N, M)} a_j \leq \left|\sum_{j=\text{min}(N, M)}^{\text{max}(N, M)} a_j\right| < \epsilon  \quad \square
$$
****
**4.** For \(z \in \Complex\), we define the **complex exponential** by
$$
e^z = \sum_{n=0}^{\infty} \frac{z^n}{n!}.
$$
\(\quad \text{(a)}\) Prove that the above definition makes sense, by showing that the series converges for every complex number \(z\). Moreover, show that the convergence is uniform on every bounded subset of \(\Complex\).
**Solution**
First we use **3.** \(\text{(c)}\) to show that the series converges. Let \(z \in \Complex\), then we have a sequence of non-negative real numbers \(\frac{|z|^n}{n!}\) whose sum converges to \(e^{|z|}\). Since \(\left|\frac{z^n}{n!}\right| \leq \frac{|z|^n}{n!}\) we are done.
We go on to show that the convergence is uniform on bounded subsets. Let \(S \subset C\) be bounded with radius \(R>0\), so for each \(z \in S\) we have \(|z| < R\). Let \(\epsilon > 0\). Regardless of what \(z\) we choose from \(S\)
$$
\left| \sum_{n=0}^N \frac{z^n}{n!}-e^z \right| = \left| \sum_{n=N}^\infty \frac{z^n}{n!} \right| \leq \sum_{n=N}^\infty \left|\frac{z^n}{n!}\right| \leq \sum_{n=N}^\infty \frac{|z|^n}{n!} \leq \sum_{n=N}^\infty \frac{R^n}{n!}
$$
So choose \(N\) large enough so that we have
$$
\epsilon > \left|\sum_{n=0}^N \frac{R^n}{n!} - e^R\right| = \left| \sum_{n=N}^\infty \frac{R^n}{n!} \right| = \sum_{n=N}^\infty \frac{R^n}{n!}.
$$
Note that the above is valid because of the convergence for the exponential series of positive reals. Combining inequalities yields the desired result
$$
\left| \sum_{n=0}^N \frac{z^n}{n!}-e^z \right| < \epsilon. \quad \square
$$
****
\(\quad \text{(b)}\) If \(z_1, z_2\) are two complex numbers, prove that \(e^{z_1}e^{z_2} = e^{z_1 + z_2}\). [Hint: Use the binomial theorem to expand \((z_1 + z_2)^n\), as well as the formula for the binomial coefficients.]
**Solution**
This whole thing is trivial using the Cauchy product. TODO: do the damn Cauchy product.
$$
(z_1 + z_2)^n = \sum_{k = 0}^n \frac{n!z_1^{n-k}z_2^k}{k!(n-k)!}
$$
$$
e^{z_1 + z_2} = \sum_{n=0}^\infty \frac{(z_1 + z_2)^n}{n!} = \sum_{n=0}^\infty \sum_{k=0}^n\frac{z_1^{n-k}z_2^k}{k!(n-k)!} = 1 + \sum_{k=0}^1\frac{z_1^{1-k}z_2^k}{k!(1-k)!} + \sum_{k=0}^2\frac{z_1^{2-k}z_2^k}{k!(2-k)!} + \cdots \\
= 1 + (z_1 + z_2) + \left(\frac{z_1^2}{2} + z_1z_2 + \frac{z_2^2}{2} \right) + \cdots
$$

$$
e^{z_1}e^{z_2} = \sum_{n=0}^\infty \frac{z_1^n}{n!} \cdot \sum_{k=0}^\infty \frac{z_2^k}{k!} = \left(1 + z_1 + \frac{z_1^2}{2} + \cdots\right) \cdot \left( 1 + z_2 + \frac{z_2^2}{2} + \cdots\right) \\
= 1\left(1 + z_2 + \frac{z_2^2}{2} + \cdots\right) + z_1\left(1 + z_2 + \frac{z_2^2}{2} + \cdots\right)+ \frac{z_1^2}{2}\left(1 + z_2 + \frac{z_2^2}{2} + \cdots\right) + \cdots \\
= \left(1 + z_2 + \frac{z_2^2}{2} + \cdots\right) + \left(z_1 + z_1z_2 + \frac{z_1z_2^2}{2} + \cdots\right)+ \left(\frac{z_1^2}{2} + \frac{z_2z_1^2}{2} + \frac{z_2^2z_1^2}{4} + \cdots\right) + \cdots \\
= 1 + (z_1 + z_2) + \left(\frac{z_1^2}{2} + z_1z_2 + \frac{z_2^2}{2}\right) + \frac{z_1z_2^2}{2} + \frac{z_2z_1^2}{2} + \frac{z_2^2z_1^2}{4} + \cdots \\
e^{z_1}e^{z_2} = \sum_{n=0}^\infty \frac{z_1^n}{n!} \cdot \sum_{k=0}^\infty \frac{z_2^k}{k!} = \sum_{k=0}^\infty \frac{z_2^k}{k!} + z_1 \sum_{k=0}^\infty \frac{z_2^k}{k!} + \frac{z_1^2}{2}\sum_{k=0}^\infty \frac{z_2^k}{k!} + \cdots \\
= \sum_{k=0}^\infty \frac{z_2^k + z_1z_2^k + \frac{z_1^2z_2^k}{2} + \cdots}{k!} = \sum_{k=0}^\infty \frac{z_2^k(1 + z_1 + \frac{z_1^2}{2} + \cdots)}{k!}
$$
Idea- show that the difference of the series tends to zero
****
\(\quad \text{(c)}\) Show that if \(z\) is purely imaginary, that is, \(z = iy\) with \(y \in \R\), then
$$
e^{iy} = \cos y + i \sin y.
$$
This is Euler's identity. [Hint: Use power series.]
****
\(\quad \text{(d)}\) More generally,
$$
e^{x + iy} = e^x(\cos y + i \sin y)
$$
whenever \(x, y \in \R\), and show that
$$
\left| e^{x + iy}  \right| = e^{x}
$$
****
\(\quad \text{(e)}\) Prove that \(e^z = 1\) if and only if \(z = 2 \pi k i\) for some integer \(k\).
****
\(\quad \text{(f)}\) Show that every complex number \(z = x + iy\) can be written in the form
$$
z = r e^{i \theta},
$$
where \(r\) is unique and in the range \(0 \leq r < \infty\), and \(\theta \in \R\) is unique up to an integer multiple of \(2 \pi\). Check that
$$
r = |z| \quad \text{and} \quad \theta = \arctan(y/x)
$$
whenever these formulas make sense.
****
\(\quad \text{(g)}\) In particular, \(i = e^{i \pi / 2}\). What is the geometric meaning of multiplying a complex number by \(i\)? Or by \(e^{i \theta}\) for any \(\theta \in \R\)
****
\(\quad \text{(h)}\) Given \(\theta \in \R\), show that
$$
\cos \theta = \frac{e^{i\theta} + e^{-i\theta}}{2} \quad \text{and} \quad \sin \theta = \frac{e^{i\theta} - e^{-i\theta}}{2i}.
$$
There are also called Euler's indentities.
****
\(\quad \text{(i)}\) Use the complex exponential to derive trigonometric identities such as
$$
\cos (\theta + \phi) = \cos \theta \cos \phi - \sin \theta \sin \phi,
$$
and then show that
$$
2 \sin \theta \sin \phi  = \cos(\theta - \phi) - \cos(\theta + \phi),
2 \sin \theta \cos \phi = \sin(\theta + \phi) + \sin(\theta - \phi).
$$
This calculation connects the solution given by d'Alember in terms of traveling waves and the solution in terms of superposition of standing waves.
****