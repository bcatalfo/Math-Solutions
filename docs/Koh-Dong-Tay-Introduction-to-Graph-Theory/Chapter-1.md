---
export_on_save:
  html: true
---

<style>
.katex-display { overflow: auto hidden }
p.dot { display: flex; justify-content: center; }
</style>

**Question 1.2.2** Let $G$ be the multigraph shown below. Find $V(G)$, $E(G)$, $v(G)$, and $e(G)$.

```dot
graph {
    {
        u [label=<<i>u</i>>]
    }
    {
        rank= same
        v [label=<<i>v</i>>]
        w [label=<<i>w</i>>]
    }
    {
        rank= same
        x [label=<<i>x</i>>]
        y [label=<<i>y</i>>]
    }
    u -- v
    u -- w
    v -- w [label=<<i>e</i><sub>1</sub>>]
    v -- w [label=<<i>e</i><sub>2</sub>>]
    v -- x
    w -- y
    x -- y
}
```

**Solution**

$$
V(G) = \{u, v, w, x, y\} \\
E(G) = \{uv, uw, e_1, e_2, vx, wy, xy\} \\
v(G) = 5 \\
e(G) = 7
$$

---

**Question 1.2.3.** Let $H$ be the graph with $V(H) = \{a,b,c,x,y,z\}$ and $E(H) = \{ab, ay, bx, by, cx, cz, xz, yz\}$. Find $v(H)$ and $e(H)$, and draw a diagram of $H$.

**Solution**
$v(H) = 6$
$e(H) = 8$

```dot
graph {
    {
        a [label=<<i>a</i>>]
        b [label=<<i>b</i>>]
        c [label=<<i>c</i>>]
        x [label=<<i>x</i>>]
        y [label=<<i>y</i>>]
        z [label=<<i>z</i>>]
    }
    a -- b
    a -- y
    b -- x
    b -- y
    c -- x
    c -- z
    x -- z
    y -- z
}
```
