---
export_on_save:
  html: true
---

<style>
.katex-display { overflow: auto hidden }
</style>

**1** &nbsp; Prove that $-(-v) = v$ for every $v \in V$.

**Solution**

Let $v \in V$. By the definition of an additive inverse $-v$ is the unique solution to the equation

$$
\tag{1} v + (-v) = 0.
$$

Similarly, $-(-v)$ is the unique solution to the equation

$$
\tag{2}(-v) + -(-v) = 0.
$$

Using the commutative property on $(1)$ we get

$$
(-v) + v = 0.
$$

Plugging into $(2)$ yields

$$
-(-v) = v. \quad \square
$$

---

**2** &nbsp; Suppose $a \in \mathbf{F}$, $v \in V$, and $av = 0$. Prove that $a = 0$ or $v = 0$.

**Solution**

Assume that $a \neq 0$. Then we divide the equation $av = 0$ by $a$ to get $v = 0$.

Alternatively, assume that $v \neq 0$. We know that $av = 0$. Assume for the purpose of contradiction that $a \neq 0$. Then divide by $a$ to get $v = 0$, a contradiction. Therefore $a = 0$.

We have shown that $a \neq 0 \implies v = 0$ and $v \neq 0 \implies a = 0$. Therefore either $a = 0$ or $v = 0$. $\quad \square$

---

**3** &nbsp; Suppose $v,w \in V$. Explain why there exists a unique $x \in V$ such that $v + 3x = w$.

**Solution**

Of course $x = \frac{1}{3}(w-v)$ is a solution to $v + 3x = w$. Suppose there exists $x' \in V$ such that

$$
v + 3x' = w.
$$

Subtracting $v$ and dividing by $3$ yields

$$
x' = \frac{1}{3}(w-v). \quad \square
$$

---

**4** &nbsp; The empty set is not a vector space. The empty set fails to satisfy only one of the reqirements listed in the definition of a vector space (1.20). Which one?

**Solution**

The additive identity requires an element $0 \in V$, contradicting $V = \emptyset$. $\quad \square$

---

**5** &nbsp; Show that in the definition of a vector space (1.20), the additive inverse condition can be replaced with the condition that

$$
0v = 0 \text{ for all } v \in V.
$$

Here the $0$ on the left side is the number $0$, and the $0$ on the right side is the additive identity of $V$.

_The phrase a "condition can be replaced" in a definition means that the collection of objects satisfying the definition is unchanged if the original condition is replaced with the new condition._

**Solution**

Let $V$ be a vector space. By 1.30 we know that $0v = 0$ for all $v \in V$.
Alternatively, let $V$ satisfy all the requirements of a vector space, with the replacement of the additive inverse condition by the condition that $0v = 0$ for all $v \in V$. We need to show that $V$ satisfies the additive inverse condition.
Let $v \in V$. Calculate that

$$
v + (-1)v = 1v + (-1)v = (1-1)v = 0v = 0. \quad \square
$$

---

**6** &nbsp; Let $\infty$ and $-\infty$ denote two distinct objects, neither of which is in $\mathbf{R}$. Define an addition and scalar multiplication on $\mathbf{R} \cup \{\infty, -\infty\}$ as you could guess from the notation. Specifically, the sum and product of two real numbers is as usual, and for $t \in \mathbf{R}$ define

$$
t \infty =
\begin{cases}
    -\infty &\text{if } t < 0, \\
    0 &\text{if } t = 0, \\
    \infty &\text{if } t > 0, \\
\end{cases}
\quad
t(-\infty) =
\begin{cases}
    \infty &\text{if } t < 0, \\
    0 &\text{if } t = 0, \\
    -\infty &\text{if } t > 0,
\end{cases}
$$

and

$$
t + \infty = \infty + t = \infty + \infty = \infty, \\
t + (-\infty) = (\infty) + t = (-\infty) + (-\infty) = -\infty, \\
\infty + (-\infty) = (-\infty) + \infty = 0.
$$

With these operations of addition and scalar multiplication, is $\mathbf{R} \cup \{\infty, -\infty\}$ a vector space over $\mathbf{R}$? Explain.

**Solution**

As defined above $\mathbf{R} \cup \{\infty, -\infty\}$ does not form a vector space.
Assume for the purpose of contradiction that $\mathbf{R} \cup \{\infty, -\infty\}$ is a vector space over $\mathbf{R}$.
By the above definition we have

$$
\infty + \infty = \infty
$$

Add $-\infty$ to both sides

$$
(\infty + \infty) + (-\infty) = \infty + (-\infty)
$$

Since $\infty$ and $-\infty$ are vectors and vector addition is by definition associative,

$$
\infty + (\infty + (-\infty)) = \infty + (-\infty)
$$

it is defined above that $\infty + -\infty = 0$ so we can plug this in to get

$$
\infty + 0 = 0,
$$

however by the definition of an additive identity in a vector space this becomes

$$
\infty = 0,
$$

contradicting the above assertion that $\infty$ is a distinct object. $\quad \square$

---

**7** &nbsp; Suppose $S$ is a nonempty set. Let $V^S$ denote the set of functions from $S$ to $V$. Define a natural addition and scalar multiplication on $V^S$, and show that $V^S$ is a vector space with these definitions.

**Solution**

Let $f,g,h \in V^S$, so $f,g,h: S \to V$ are vectors. Let $\lambda, \mu$ be scalars. Define vector addition and scalar multiplication as follows

$$
(f+g)(x) = f(x) + g(x), \\
(\lambda f)(x) = \lambda f(x).
$$

We proceed to verify the vector space axioms. Let $x \in S$.

_commutativity_

$$
(f + g)(x) = f(x) + g(x) = g(x) + f(x) = (g + f)(x) \\
f + g = g + f
$$

_associativity_

$$
((f + g) + h)(x) = (f+g)(x) + h(x) = f(x) + g(x) + h(x) \\
= f(x) + (g(x) + h(x)) = f(x) + (g + h)(x) = (f + (g+h))(x) \\
(f + g) + h = f + (g+h)\\[4px]
((\lambda \mu) f)(x) = (\lambda \mu)f(x) = \lambda(\mu f(x)) = \lambda (\mu f)(x) \\
(\lambda \mu)f = \lambda (\mu f)
$$

_additive identity_

Define $0 \in V^S$ as the function $0(x) = 0$. Then

$$
(f + 0)(x) = f(x) + 0 = f(x) \\
f + 0 = f
$$

_additive inverse_

Define $-f$ by $(-f)(x) = -f(x)$. Then 

$$
(f + -f)(x) = f(x) + -f(x) = 0 \\
f + -f = 0
$$

_multiplicative identity_

$$
(1f)(x) = 1 f(x) = f(x) \\
1f = f
$$

_distributive properties_

$$
(\lambda (f + g))(x) = \lambda (f+g)(x) = \lambda (f(x) + g(x)) = \lambda f(x) + \lambda g(x) \\
\lambda (f + g) = \lambda f + \lambda g \\[4px]
((\lambda + \mu)f)(x) = (\lambda + \mu)f(x) = \lambda f(x) + \mu f(x) \\
(\lambda + \mu)f = \lambda f + \mu f \quad \square
$$


---

**8** &nbsp; Suppose $V$ is a real vector space.

- The _complexification_ of $V$, denoted by $V_{\mathbf{C}}$, equals $V \times V$. An element of $V_{\mathbf{C}}$ is an ordered pair $(u,v)$, where $u,v \in V$, but we write this as $u+iv$.
- Addition on $V_{\mathbf{C}}$ is defined by
  $$
  (u_1 + iv_1) + (u_2 + iv_2) = (u_1 + u_2) + i (v_1+v_2)
  $$
  for all $u_1, v_1, u_2, v_2 \in V$.
- Complex scalar multiplication on $V_{\mathbf{C}}$ is defined by
  $$
  (a+bi)(u+iv) = (au - bv) + i(av+bu)
  $$
  for all $a,b\in \mathbf{R}$ and all $u,v \in V$.

Prove that with the definitions of addition and scalar multiplication as above, $V_{\mathbf{C}}$ is a complex vector space.

**Solution**

Again, we go one by one through the axioms.

_commutativity_

$$
(u_1 + iv_1) + (u_2 + iv_2) = (u_1 + u_2) + i(v_1 + v_2) \\
 = (u_2 + u_1) + i(v_2 + v_1) = (u_2 + iv_2) + (u_1 + iv_1)
$$

_associativity_

$$
((u_1 + iv_1) + (u_2 + iv_2)) + (u_3 + iv_3) \\
 = ((u_1 + u_2) + i(v_1 + v_2)) + (u_3 + iv_3) \\
 = (u_1 + u_2 + u_3) + i(v_1 + v_2 + v_3) \\
 = (u_1 + (u_2 + u_3)) + i(v_1 + (v_2 + v_3)) \\
 = (u_1 + iv_1) + ((u_2 + u_3) + i(v_2 + v_3)) \\
 = (u_1 + iv_1) + ((u_2 + iv_2) + (u_3 + iv_3))
$$

_additive identity_

$$
(u + iv)+ (0 + 0i) = (u + 0) + i(v + 0) = u + iv
$$

_additive inverse_

$$
(u + iv) + (-u + i(-v)) = (u + -u) + i(v + -v) = 0 + 0i = 0
$$

_multiplicative identity_

$$
1(u+iv) = (1 + 0i)(u+iv) = (1u - 0v) + i(1v + 0u) = u + iv 
$$

_distributive properties_

$$
(a + bi)((u_1 + iv_1) + (u_2 + iv_2)) = (a+bi)((u_1+u_2)+i(v_1+v_2)) \\
= (a(u_1+u_2) - b(v_1+v_2)) + i(a(v_1+v_2) + b(u_1+u_2)) \\
= ((au_1 - bv_1) + (au_2 - bv_2)) + i((av_1+bu_1)+(av_2+bu_2)) \\
= ((au_1 - bv_1) + i(av_1 + bu_1)) + ((au_2 - bv_2) + i(av_2+bu_2)) \\
= (a+bi)(u_1 + iv_1) + (a+bi)(u_2+iv_2)
$$

$$
((a + bi) + (c+di))(u + iv) = ((a+c)+i(b+d))(u+iv) \\
((a+c)u - (b+d)v) + i((a+c)v + (b+d)u) \\
= ((au - bv) + (cu-dv)) + i((av + bu) + (cv + du)) \\
= ((au-bv) + i(av+bu)) + ((cu - dv) + i(cv + du)) \\
= (a+bi)(u + iv) + (c+di)(u+iv) \quad \square
$$

$$
\\
$$