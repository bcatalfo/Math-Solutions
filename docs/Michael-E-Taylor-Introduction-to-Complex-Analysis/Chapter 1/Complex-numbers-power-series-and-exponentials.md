---
export_on_save:
  html: true
---

<style>
.katex-display { overflow: auto hidden; padding: 2px }
</style>

# Introduction to Complex Analysis (Graduate Studies in Mathematics 202)
## Michael E. Taylor

## Chapter 1. &nbsp; Basic calculus in the complex domain
### §1.1. &nbsp; Complex numbers, power series, and exponentials

### Exercises

$1. \>$ Supplement $(1.1.20)$ with the following result. Assume there exists $A > 0$ such that $|z_n| \geq A$ for all $n$. Then

$$
z_n \to z \implies \frac{1}{z_n} \to \frac{1}{z}.
$$

**Solution**

Let $z_n \to z$. It remains to show that $\frac{1}{z_n} \to \frac{1}{z}$.

_Lemma_ &nbsp; $|z| > 0$.

_Proof of Lemma_ &nbsp; $|z| = 0 \iff z = 0 \iff z_n \to 0 \implies \left( \exists N \enspace \text{s.t.} \enspace n > N \implies |z_n| < A \right)$, contradicting $|z_n| \geq A$ for all $n$. $\quad \square$

Notice that if $w \in \mathbb{C}, |w| > 0$ then

$$
|w|^2 = w \overline{w} \implies 1 = \frac{w\overline{w}}{|w|^2} \implies
\frac{1}{w} = \frac{\overline{w}}{|w|^2}.
$$

Since $z_n, z > 0$,

$$
\left| \frac{1}{z_n} - \frac{1}{z} \right|
= \left| \frac{\overline{z_n}}{|z_n|^2} - \frac{\overline{z}}{|z|^2} \right | .
$$

Therefore it is sufficient to show that 

$$
\tag{1} \phantom{(1)} \quad\overline{z_n} \to \overline{z} \quad \text{and} \quad \frac{1}{|z_n|^2} \to \frac{1}{|z|^2},
$$

because by Equation $(1.1.20)$ if $(\xi_n)$ is a sequence in $\mathbb{C}$ then

$$
\xi_n \to \xi, w_n \to w \implies \xi_nw_n \to \xi w.
$$

Since 

$$
|\overline{z_n} - \overline{z}| = \left|\overline{z_n} + \overline{-1}\overline{z}\right|
$$

We can use Equation $(1.1.12)$

$$
\tag{1.1.12} \phantom{(1.1.12)} \quad \overline{z + w} = \overline{z} + \overline{w}, \quad \overline{zw} = \overline{z} \overline{w}
$$

to get 

$$
\left|\overline{z_n} + \overline{-1}\overline{z}\right| = \left| \overline{z_n} + \overline{-z} \right| = \left| \overline{z_n - z} \right|,
$$

and since $|\overline{\xi}| = |\xi|, \> \forall \xi \in \mathbb{C}$ we have $\left|\overline{z_n-z}\right| = \left|z_n-z\right|$, so

$$
\tag{2} \phantom{(2)} \quad \left| \overline{z_n} - \overline{z} \right| = \left| z_n - z \right|,
$$

therefore $z_n \to z \implies \overline{z_n} \to \overline{z}$. Note that Equation $(2)$ has a geometric interpretation as well $\text{---}$ reflections preserve distance, and $\xi \to \overline{\xi}$ is geometrically a reflection over the $x$-axis.

Since we have shown that $\overline{z_n} \to \overline{z}$, by Equation $(1)$ it remains to show that $\frac{1}{|z_n|^2} \to \frac{1}{|z|^2}$. This is a sequence of real numbers. Since $z_n \to z$ we must have $|z_n| \to |z|$, a sequence of reals. So what follows is a basic exercise in real analysis.

Calculate that

$$
\left| \frac{1}{|z|} - \frac{1}{|z_n|} \right|
= \left| \frac{|z_n|}{|z||z_n|} - \frac{|z|}{|z||z_n|} \right| \\[.25em]
= \left| \frac{|z_n| - |z|}{|z||z_n|} \right| < \left| \frac{|z_n| - |z|}{A^2} \right| .
$$

Let $\varepsilon > 0$. Since $|z_n| \to |z|$ we can choose $N$ such that $n > N \implies ||z| - |z_n|| < \varepsilon A^2$. Then $\left| \frac{1}{|z|} - \frac{1}{|z_n|} \right| < \varepsilon$. Therefore $\frac{1}{|z_n|} \to \frac{1}{|z|}$. For a sequence of reals $(x_n)$, $x_n \to x \implies x_n^2 \to x^2 $. Therefore $\frac{1}{|z_n|^2} \to \frac{1}{|z|^2}. \quad \square$

---

$2. \>$ Show that 

$$
\tag{1.1.75} \phantom{(1.1.75)} \quad |z| < 1 \implies z^k \to 0, \quad \text{as} \quad k \to \infty.
$$

_Hint._ Deduce $(1.1.75)$ from the assertion

$$
\tag{1.1.76} \phantom{(1.1.76)} \quad 0 < s < 1 \implies ks^k \enspace \text{is bounded, for } k \in \N.
$$

Note that this is equivalent to

$$
\tag{1.1.77} \phantom{(1.1.77)} \quad a > 0 \implies \frac{k}{(1+a)^k} \enspace \text{is bounded, for } k \in \N.
$$

Show that

$$
\tag{1.1.78} \phantom{(1.1.78)} \quad (1+a)^k = (1+a) \cdots (1+a) \geq 1 + ka, \> \forall a > 0, k \in \N.
$$

Use this to prove $(1.1.77)$, hence $(1.1.76)$, hence $(1.1.75)$.

**Solution**

First show $(1.1.78)$. Proceed by induction. Let 

$$
P(k): \> (1+a)^k \geq 1 + ka, \> \forall a > 0.
$$

Then $P(0)$ is the statement $(1+a)^0 \geq 1 + 0 \cdot a \iff 1 \geq 1$ which holds.
Assume $P(k)$, it remains to show $P(k+1)$, that is 

$$
(1+a)^{k+1} \geq 1 + (k+1)a
$$

Calculate that 

$$
(1+a)^{k+1} = (1+a) \cdot (1+a)^k \geq (1+a) \cdot (1+ka) \\
 = 1 + ka + a + ka^2 > 1 + (k+1)a.
$$

This shows $P(k+1)$, completing the proof of $(1.1.78)$.

In light of $(1.1.78)$,

$$
\frac{k}{(1 + a)^k} \leq \frac{k}{1 + ka} < \frac{k}{ka} = \frac{1}{a},
$$

proving $(1.1.77)$, which is equivalent to $(1.1.76)$.

Use $(1.1.76)$ to calculate that there must exist $R > 0$ such that

$$
\left|kz^k\right| = k |z|^k < R \implies \left|z^k\right| < \frac{R}{k},
$$

so as $k \to \infty$ we have $z^k \to 0. \quad \square$

---

$3. \>$ Letting $s_n = \sum_{k=0}^{n}r^k$, write the series for $rs_n$ and show that 

$$
\tag{1.1.79} \phantom{(1.1.79)} \quad (1-r)s_n = 1 - r^{n+1}, \quad \text{hence} \enspace s_n = \frac{1 - r^{n+1}}{1-r}.
$$

Deduce that 

$$
\tag{1.1.80} \phantom{(1.1.80)} \quad 0 < r < 1 \implies s_n \to \frac{1}{1-r}, \quad \text{as} \enspace n \to \infty,
$$

as we stated in $(1.1.34)$. More generally, show that 

$$
\tag{1.1.81} \phantom{(1.1.81)} \quad \sum_{k=0}^{\infty} z^k = \frac{1}{1-z}, \quad \text{for} \enspace |z| < 1.
$$

**Solution**

First calculate that 

$$
rs_n = r \sum_{k=0}^n r^k = \sum_{k=0}^n r^{k+1} = \sum_{k=1}^{n+1} r^k,
$$

so

$$
(1 - r)s_n = s_n - r s_n = \sum_{k=0}^n r^k - \sum_{k=1}^{n+1}r^k = 1 - r^{n+1}.
$$

Dividing by $(1-r)$ we get 

$$
s_n = \frac{1-r^{n+1}}{1-r},
$$

and if $0 < r < 1$ then $\lim_{n \to \infty} r^{n+1} = 0$ so $(1.1.80)$ holds.

More generally we can show $(1.1.81)$ by using Exercise $2$.

Let $S_n = \sum_{k=0}^n z^k$. Then by the same argument as before 

$$
S_n = \frac{1 - z^{n+1}}{1-z}.
$$

By Exercise $2$ if $|z| < 1$ then $\lim_{n\to\infty} z^{n+1} = \lim_{n\to\infty}z^n = 0$ so $(1.1.81)$ holds. $\quad \square$

---

$4. \>$ This exercise discusses the ratio test, mentioned in connection with the infinite series $(1.1.49)$ and $(1.1.62)$. Consider the infinite series

$$
\tag{1.1.82} \phantom{(1.1.82)} \quad \sum_{k=0}^{\infty} a_k, \quad a_k \in \mathbb{C}.
$$

Assume there exists $r < 1$ and $N < \infty$ such that 

$$
\tag{1.1.83} \phantom{(1.1.83)} \quad k \geq N \implies \left| \frac{a_{k+1}}{a_k} \right| \leq r.
$$

Show that

$$
\tag{1.1.84} \phantom{(1.1.84)} \quad \sum_{k=0}^{\infty} |a_k| < \infty.
$$

_Hint_. Show that 

$$
\tag{1.1.85} \phantom{(1.1.85)} \quad \sum_{k=N}^{\infty} |a_k| \leq |a_N| \sum_{\ell=0}^{\infty} r^\ell = \frac{|a_N|}{1-r}.
$$

**Solution**

First we use $(1.1.83)$ to obtain an upper bound on $a_{N+k}$

$$
\begin{aligned}
\left| a_{N+k} \right| &= \left| a_N \frac{a_{N+1}}{a_N} \frac{a_{N+2}}{a_{N+1}} \cdots  \frac{a_{N+k}}{a_{N+(k-1)}} \right| \\[.25em]
&\leq |a_N| \cdot \left| \frac{a_{N+1}}{a_N} \right| \left| \frac{a_{N+2}}{a_{N+1}} \right| \cdots \left| \frac{a_{N+k}}{a_{N+(k-1)}} \right| \\[.25em]
&\leq |a_N| r^k,
\end{aligned}
$$

and immediately put it to use to show $(1.1.85)$

$$
\begin{aligned}
\sum_{k=N}^\infty |a_k| &= \sum_{k=0}^\infty \left| a_{N+k} \right| \leq \sum_{k=0}^\infty |a_N| r^k \\[.25em]
&= |a_N| \sum_{k=0}^\infty r^k = \frac{|a_N|}{1 - r}. 
\end{aligned}
$$

The desired result $(1.1.84)$ follows very easily from this as 

$$
\begin{aligned}
\sum_{k=0}^\infty |a_k| &= \sum_{k=0}^N |a_k| + \sum_{k=N}^\infty |a_k| \\[.25em]
&\leq \sum_{k=0}^N |a_k| + \frac{|a_N|}{1-r} < \infty. \quad \square
\end{aligned}
$$

---

$5. \>$ In the case

$$
\tag{1.1.86} \phantom{(1.1.86)} \quad a_k = \frac{z^k}{k!},
$$

show that for each $z \in \mathbb{C}$, there exists $N < \infty$ such that $(1.1.83)$ holds, with $r = 1/2$. Also show that the ratio test applies to 

$$
\tag{1.1.87} \phantom{(1.1.87)} \quad a_k = kz^k, \quad |z| < 1.
$$

**Solution**

Let's first do the ratio test on $(1.1.86)$

$$
\left|\frac{a_{k+1}}{a_k}\right| = \left|\frac{z^{k+1}}{(k+1)!} \frac{k!}{z^k}\right| = \left|\frac{z}{k+1}\right| = \frac{|z|}{k+1}.
$$

So let $N > 2|z|-1$. Then 

$$
k > N \implies \frac{|z|}{k+1} < \frac{|z|}{2|z|} = \frac{1}{2},
$$

showing that $(1.1.83)$ holds with $r = 1/2$.

Next do the same for $(1.1.87)$

$$
\left|\frac{a_{k+1}}{a_k}\right| = \left| \frac{(k+1)z^{k+1}}{kz^k} \right| = \frac{k+1}{k} \left| z \right| < |z|,
$$

since $|z| < 1$, this passes the ratio test with $r=|z|$ and for any $N$, for example $N=1. \quad \square$

---

$6. \>$ This exercise discusses the integral test for absolute convergence of an infinite series, which goes as follows. Let $f$ be a positive, monotonically decreasing, continuous function on $[0,\infty)$, and suppose $|a_k|=f(k)$. Then

$$
\tag{1.1.88} \phantom{(1.1.88)} \quad \sum_{k=0}^{\infty} |a_k| < \infty \iff \int_{0}^{\infty} f(t) \, dt < \infty.
$$

Prove this.
_Hint_. Use 

$$
\tag{1.1.89} \phantom{(1.1.89)} \quad \sum_{k=1}^N |a_k| \leq \int_0^N f(t) \, dt \leq \sum_{k=0}^{N-1} |a_k|.
$$

**Solution**

$(\implies) \>$ Assume that $\sum_{k=0}^\infty |a_k| < \infty$. Let $N > 0$. Then 

$$
\int_{0}^N f(t)dt\, \leq \sum_{k=0}^{N-1} |a_k| < \sum_{k=0}^\infty |a_k| < \infty.
$$

Let $b_k = \int_{0}^N f(t)dt$. Then $\lim_{k \to \infty} b_k  = \int_{0}^\infty f(t)dt\,$.

*Lemma* $\{b_k\}$ is monotone 

*Lemma* $\{b_k\}$ is bounded

Since $\{b_k\}$ is montone and bounded it is convergent. Therefore $\int_0^\infty f(t)dt\, < \infty$.

---

$7. \>$ Use the integral test to show that, if $a > 0$,

$$
\tag{1.1.90} \phantom{(1.1.90)} \quad \sum_{n=1}^\infty \frac{1}{n^a} < \infty \iff a > 1.
$$

---

$8. \>$ This exercise deals with alternating series. Assume $b_k \searrow 0$. Show that 

$$
\tag{1.1.91} \phantom{(1.1.91)} \quad \sum_{k=0}^\infty  (-1)^k b_k \enspace \text{is convergent,}
$$

by showing that, for $m,n \geq 0$,

$$
\tag{1.1.92} \phantom{(1.1.92)} \left| \sum_{k=n}^{n+m} (-1)^kb_k \right| \leq b_n.
$$

---

$9. \>$ Show that $\sum_{k=1}^\infty (-1)^k/k$ is convergent, but not absolutely convergent.

---

$10. \>$ Show that if $f,g: (a,b) \to \mathbb{C}$ are differentiable, then

$$
\tag{1.1.93} \phantom{(1.1.93)} \quad \frac{d}{dt} (f(t)g(t)) = f'(t)g(t) + f(t)g'(t).
$$

Note the use of this identity in $(1.1.66)$ and $(1.1.70)$.

---

$11. \>$ Use the results of Exercise $10$ to show, by induction on $k$, that

$$
\tag{1.1.94} \phantom{(1.1.94)} \quad \frac{d}{dt} t^k = kt^{k-1}, \enspace k = 1,2,3,\dots,
$$

hence

$$
\tag{1.1.95} \phantom{(1.1.95)} \quad \int_0^t s^k \> ds = \frac{1}{k+1}t^{k+1}, \enspace k = 0,1,2,\dots.
$$

Note the use of these identities in $(1.1.57)$, leading to many of the identities in $(1.1.46)$–$(1.1.64).$

---

$12. \>$ Consider 

$$
\tag{1.1.96} \phantom{(1.1.96)} \quad \varphi(z) = \frac{z-1}{z+1}.
$$

Show that 

$$
\tag{1.1.97} \phantom{(1.1.97)} \quad \varphi: \mathbb{C} \setminus \{-1\} \longrightarrow \mathbb{C} \setminus \{1\}
$$

is continuous, one-to-one, and onto. Show that, if $\Omega = \{z \in \mathbb{C}: \mathfrak{R}z > 0\}$ and $D = \{z \in \mathbb{C}: |z| < 1\}$, then 

$$
\tag{1.1.98} \phantom{(1.1.98)} \quad \varphi: \Omega \to D \enspace \text{and} \enspace \varphi: \partial\Omega \to \partial D \setminus \{1\}
$$

are one-to-one and onto.

$$
\\
$$