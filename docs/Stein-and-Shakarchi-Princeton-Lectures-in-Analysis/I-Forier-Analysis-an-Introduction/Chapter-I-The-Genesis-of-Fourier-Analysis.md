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
This problem had stumped me for a while. I ended up taking a break from this problem, learning some combinatorics, and coming back to it. Upon doing so I realized that there is a very easy combinatorical solution to this problem using the basic method of "double-counting". Take a look at the following infinite list of terms.
$$
\begin{array}{ccccc}
  1 \\[4pt]
  a & b \\[4pt]
  \frac{a^2}{2} & ab & \frac{b^2}{2} \\[4pt]
  \frac{a^3}{6} & \frac{a^2b}{2} & \frac{ab^2}{2} & \frac{b^3}{6} \\[4pt]
  \vdots & \vdots & \vdots & \vdots & \vdots 
\end{array}
$$
Here the term at the $n + 1$th row and the $k + 1$th column is given by the formula $\frac{a^{n-k}b^{k}}{(n -k)!k!}$, where we always have $k \leq n$, so the sum of all of these terms is $\sum_{n=0}^{\infty}\sum_{k=0}^{n} \frac{a^{n-k}b^k}{(n-k)!k!}$.

The key insight of the double-counting method is that there are two different ways of adding up all of the terms- you can add all the rows or add all of the columns- but the result is the same.

If we add all the rows we get 
$$
\sum_{n=0}^{\infty}\sum_{k=0}^{n} \frac{a^{n-k}b^k}{(n-k)!k!} = 1 + (a + b) + \left(\frac{a^2}{2} + ab + \frac{b^2}{2}\right) + \left( \frac{a^3}{6} + \frac{a^2b}{2} + \frac{ab^2}{2} + \frac{b^3}{6} \right) + \cdots \\
= \frac{(a + b)^0}{0!} + \frac{(a + b)^1}{1!} + \frac{(a + b)^2}{2!} + \frac{(a + b)^3}{3!} + \cdots \\
= \sum_{n=0}^{\infty} \frac{(a + b)^n}{n!} = e^{a + b}
$$

If we add all the columns we get
$$
\begin{aligned}
  \sum_{n=0}^{\infty}\sum_{k=0}^{n} \frac{a^{n-k}b^k}{(n-k)!k!} &= \left(1 + a + \frac{a^2}{2} + \frac{a^3}{6} + \cdots \right) + \left( b + ab + \frac{a^2b}{2} + \cdots \right) \\ 
  &+ \left( \frac{b^2}{2} + \frac{ab^2}{2} + \cdots \right) + \left(\frac{b^3}{6} + \cdots\right) + \cdots \\
  &= \sum_{n=0}^{\infty} \frac{a^n}{n!} + b\sum_{n=0}^{\infty}\frac{a^n}{n!} + \frac{b^2}{2}\sum_{n=0}^{\infty}\frac{a^n}{n!} + \frac{b^3}{6}\sum_{n=0}^{\infty} \frac{a^n}{n!} + \cdots \\
  &= \sum_{n=0}^{\infty}\frac{a^n}{n!} \left( 1 + b + \frac{b^2}{2} + \frac{b^3}{6} + \cdots \right) \\
  &= \sum_{n=0}^{\infty}\frac{a^n}{n!} \cdot \sum_{k=0}^{\infty}\frac{b^k}{k!} = e^a \cdot e^b 
\end{aligned}
$$
This is the heart and soul of the proof, but it is a little bit hand-wavey. I hope that the above gives the reader a clear intuition behind the proof. In order to turn this intuition into more rigorous mathematics, we use the binomial expansion
$$
(a + b)^n = \sum_{k=0}^{n} \frac{n!a^{n-k}b^k}{(n-k)!k!} 
$$
to calculate that 
$$
\sum_{n=0}^{\infty}\sum_{k=0}^{n} \frac{a^{n-k}b^k}{(n-k)!k!} = \sum_{n=0}^{\infty} \frac{(a+b)^n}{n!} = e^{a + b}
$$
and combinatorically rearrange the series to switch from adding the rows to adding the columns via the identity
$$
\sum_{n=0}^{\infty}\sum_{k=0}^{n} f(n,k) = \sum_{k=0}^{\infty}\sum_{n=k}^{\infty} f(n,k)
$$
which holds because both the LHS and RHS are summing over each $k, n \in \N$ such that $k \leq n$. Plugging in $f(n,k)=\frac{a^{n-k}b^{k}}{(n-k)!k!}$ to the identity yields
$$
\sum_{n=0}^{\infty}\sum_{k=0}^{n} \frac{a^{n-k}b^k}{(n-k)!k!} = \sum_{k=0}^{\infty}\sum_{n=k}^{\infty} \frac{a^{n-k}b^k}{(n-k)!k!} = \sum_{k=0}^{\infty} \frac{b^k}{k!} \sum_{n=k}^{\infty} \frac{a^{n-k}}{(n-k)!} = \sum_{k=0}^{\infty} \frac{b^k}{k!} \sum_{n=0}^{\infty} \frac{a^n}{n!} = e^a \cdot e^b \qquad \square
$$
****
\(\quad \text{(c)}\) Show that if \(z\) is purely imaginary, that is, \(z = iy\) with \(y \in \R\), then
$$
e^{iy} = \cos y + i \sin y.
$$
This is Euler's identity. [Hint: Use power series.]
**Solution**
The general idea is
$$
e^{iy} = \sum_{n=0}^{\infty}\frac{(iy)^n}{n!} = 1 + (iy) + \frac{(iy)^2}{2} + \frac{(iy)^3}{6} + \cdots \\
= 1 + iy - \frac{y^2}{2} -\frac{iy^3}{6} + \cdots \\
= (1 - \frac{y^2}{2} + \cdots) + (y - \frac{y^3}{6} + \cdots)i \\
= \cos y + i \sin y
$$
More rigorously,
$$
e^{iy} = \sum_{n=0}^{\infty}\frac{(iy)^n}{n!} = \sum_{n=0 \text{, } n \text { is even}}^{\infty}\frac{(iy)^n}{n!} + \sum_{n=0 \text{, } n \text{ is odd}}^{\infty}\frac{(iy)^n}{n!} \\
= \sum_{n=0}^{\infty} \frac{(iy)^{2n}}{(2n)!} + \sum_{n=0}^{\infty} \frac{(iy)^{2n+1}}{(2n+1)!}  \\
= \sum_{n=0}^{\infty} \frac{i^{2n}(y)^{2n}}{(2n)!} + \sum_{n=0}^{\infty} \frac{i^{2n+1}(y)^{2n+1}}{(2n+1)!} \\
= \sum_{n=0}^{\infty} \frac{i^{2n}(y)^{2n}}{(2n)!} + i\sum_{n=0}^{\infty} \frac{i^{2n}(y)^{2n+1}}{(2n+1)!} \\
= \sum_{n=0}^{\infty} \frac{(-1)^{n}(y)^{2n}}{(2n)!} + i\sum_{n=0}^{\infty} \frac{(-1)^{n}(y)^{2n+1}}{(2n+1)!} \\
= \cos y + i \sin y \quad \square
$$
****
\(\quad \text{(d)}\) More generally,
$$
e^{x + iy} = e^x(\cos y + i \sin y)
$$
whenever \(x, y \in \R\), and show that
$$
\left| e^{x + iy}  \right| = e^{x}
$$
**Solution**
Combining parts $\text{(b)}$ and $\text{(c)}$ gives
$$
e^{x + iy} = e^x \cdot e^{iy} = e^x ( \cos y + i \sin y)
$$
and we can calculate that 
$$
|e^{x + iy}| = |e^x (\cos y + i \sin y)| = |e^x| |\cos y + \sin y| = e^x \quad \square
$$
****
\(\quad \text{(e)}\) Prove that \(e^z = 1\) if and only if \(z = 2 \pi k i\) for some integer \(k\).
**Solution**
Let $z = x + iy$ with $x, y \in \R$
$$
1 = e^z = e^{x+iy} = e^x(\cos y + i \sin y) \\
\iff e^x \cos y = 1 \text{ and } \sin y \cdot e^x = 0 
$$
Remember that $x$ and $y$ are real so 
$$
\sin y \cdot e^x = 0 \iff \sin y = 0 \iff y = 2 \pi k \text{, for some integer } k
$$
We can now plug in $y$ to the other equation to find $x$
$$
e^x \cos y = 1 \iff e^x \cos 2\pi k = 1 \iff e^x = 1 \iff x = 0 
$$
So in conclusion
$$
e^z = 1 \iff y = 2 \pi k \text{ and } x = 0 \iff z = 2\pi ki \quad \square
$$
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
**Solution**
$$
z = x + iy \\
\frac{z}{\sqrt{x^2 + y^2}} = \frac{x}{\sqrt{x^2 + y^2}} + i \frac{y}{\sqrt{x^2+y^2}} \\
z = \sqrt{x^2 + y^2} \left( \frac{x}{\sqrt{x^2+y^2}} + i \frac{y}{\sqrt{x^2+y^2}} \right)
$$
Now by making a right triangle with bases of $x$ and $y$ it is clear that there is $\theta$ such that $\cos \theta = \frac{x}{\sqrt{x^2 + y^2}}$ and $\sin \theta \ = \frac{y}{\sqrt{x^2+y^2}}$, and for such $\theta$ we have $\arctan(\theta) = y/x$. Plugging in,
$$
z = \sqrt{x^2 + y^2} \cdot ( \cos \theta + i \sin \theta) = re^{i\theta} \quad \square
$$
****
\(\quad \text{(g)}\) In particular, \(i = e^{i \pi / 2}\). What is the geometric meaning of multiplying a complex number by \(i\)? Or by \(e^{i \theta}\) for any \(\theta \in \R\)
**Solution**
Multiplying by $i$ is rotating $\pi / 2$ radians, in general multipling by $e^{i \theta}$ is rotating by $\theta$ radians.
****
\(\quad \text{(h)}\) Given \(\theta \in \R\), show that
$$
\cos \theta = \frac{e^{i\theta} + e^{-i\theta}}{2} \quad \text{and} \quad \sin \theta = \frac{e^{i\theta} - e^{-i\theta}}{2i}.
$$
There are also called Euler's indentities.
**Solution**
$$
e^{i \theta} = \cos \theta + i \sin \theta \\
e^{-i \theta} = e^{i \cdot (-\theta)} = \cos (-\theta) + i \sin (-\theta) = \cos \theta - i \sin \theta \\
e^{i \theta} + e^{-i\theta} = (\cos \theta + i \sin \theta) + (\cos \theta - i \sin \theta) = 2 \cos \theta \\
\cos \theta = \frac{e^{i \theta} + e^{-i \theta}}{2} \\
e^{i \theta} - e^{-i \theta} = (\cos \theta + i \sin \theta) - (\cos \theta - i \sin \theta) = 2i \sin \theta \\
\sin \theta = \frac{e^{i \theta} - e^{-i\theta}}{2i} \quad \square
$$
****
\(\quad \text{(i)}\) Use the complex exponential to derive trigonometric identities such as
$$
\cos (\theta + \phi) = \cos \theta \cos \phi - \sin \theta \sin \phi,
$$
and then show that
$$
2 \sin \theta \sin \phi  = \cos(\theta - \phi) - \cos(\theta + \phi), \\
2 \sin \theta \cos \phi = \sin(\theta + \phi) + \sin(\theta - \phi).
$$
This calculation connects the solution given by d'Alember in terms of traveling waves and the solution in terms of superposition of standing waves.
**Solution**
First calculate that 
$$
\begin{aligned}
  2 \cos(\theta + \phi) &= e^{i(\theta + \phi)} + e^{-i(\theta + \phi)} = e^{i\theta}e^{i\phi} + e^{-i\theta}e^{-i\phi} \\
  &= (\cos \theta + i \sin \theta) (\cos \phi + i \sin \phi) + (\cos \theta - i \sin \theta)(\cos \phi - i \sin \phi) \\ 
  &= (\cos\theta \cos\phi + i \cos\theta \sin\phi + i \sin \theta \cos \phi - \sin \theta \sin \phi)  \\ 
  &+ (\cos \theta \cos \phi - i \cos \theta \sin \phi - i \sin \theta \cos \phi - \sin \theta \sin \phi) \\
  &= 2 \cos \theta \cos \phi - 2 \sin \theta \sin \phi \quad \square
\end{aligned}
$$
Using this formula
$$
\begin{aligned}
  \cos(\theta - \phi) - \cos(\theta + \phi) &= \cos(\theta + (-\phi)) - \cos(\theta + \phi) \\
  &= (\cos \theta \cos (- \phi) - \sin \theta \sin (-\phi)) - (\cos \theta \cos \phi - \sin \theta \sin \phi) \\
  &= \cos \theta \cos \phi + \sin \theta \sin \phi - \cos \theta \cos \phi + \sin \theta \sin \phi \\
  &= 2 \sin \theta \sin \phi \quad \square
\end{aligned}
$$
Now let's calculate sine's angle addition formula
$$
\begin{aligned}
  2i \sin(\theta + \phi) &= e^{i (\theta + \phi)} - e^{-i (\theta + \phi)} = e^{i\theta}e^{i\phi} - e^{i(-\theta)}e^{i(-\phi)} \\
  &= (\cos \theta \cos \phi + i \cos \theta \sin \phi + i \sin \theta \cos \phi - \sin \theta \sin \phi) \\
  &- (\cos \theta \cos \phi - i \cos \theta \sin \phi - i \sin \theta \cos \phi - \sin \theta \sin \phi) \\
  &= 2i \cos \theta \sin \phi + 2i\sin \theta \cos \phi \\
\end{aligned} \\
\sin(\theta + \phi) = \cos \theta \sin \phi + \sin \theta \cos \phi
$$
We can now solve the last identity
$$
\begin{aligned}
  \sin(\theta + \phi) + \sin(\theta - \phi) &= (\cos \theta \sin \phi + \sin \theta \cos \phi) + (\cos \theta \sin (-\phi) + \sin \theta \cos (-\phi)) \\
  &= (\cos \theta \sin \phi + \sin \theta \cos \phi) + (-\cos \theta \sin \phi + \sin \theta \cos \phi) \\
  &= 2\sin \theta \cos \phi \quad \square
\end{aligned}
$$
****