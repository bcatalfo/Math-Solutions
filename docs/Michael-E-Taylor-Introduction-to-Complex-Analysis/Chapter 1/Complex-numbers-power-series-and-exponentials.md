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

Let $\varepsilon > 0$. We need to find $N$ large enough such that 

$$
n > N \implies \left| \frac{1}{z_n} - \frac{1}{z} \right| < \varepsilon.
$$

First use the fact that $z_n \to z$ to choose $N'$ such that

$$
n > N' \implies |z_n - z| < \varepsilon.
$$

Then notice that

$$
1 = \frac{z\overline{z}}{|z|^2} \\[.25em]
\frac{1}{z} = \frac{\overline{z}}{|z|^2}
$$

so 

$$
\left| \frac{1}{z_n} - \frac{1}{z} \right|
= \left| \frac{\overline{z_n}}{|z_n|^2} - \frac{\overline{z}}{|z|^2} \right |
$$

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
\tag{1.1.78} \phantom{(1.1.78)} \quad (1+a)^k = (1+a) \cdots (1+a) \geq 1 + ka, \quad \forall a > 0, k \in \N.
$$

Use this to prove $(1.1.77)$, hence $(1.1.76)$, hence $(1.1.75)$.

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
\tag{1.1.81} \phantom{(1.1.81)} \quad \sum_{k=0}^{\infty} z_k = \frac{1}{1-z}, \quad \text{for} \enspace |z| < 1.
$$

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

---

$5. \>$ In the case

$$
\tag{1.1.86} \phantom{(1.1.86)} \quad a_k = \frac{z^k}{k!},
$$

show that for each $z \in \mathbb{C}$, there exists $N < \infty$ such that $(1.1.83)$ holds, with $r = 1/2$. Also show that the ratio test applies to 

$$
\tag{1.1.87} \phantom{(1.1.87)} \quad a_k = kz^k, \quad |z| < 1.
$$

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

$$
\\
$$