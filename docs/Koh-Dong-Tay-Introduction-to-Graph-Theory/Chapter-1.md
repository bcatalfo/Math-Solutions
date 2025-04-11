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

---

**Question 1.2.4** Let $G$ be the multigraph shown below.

```dot
graph {
    {
        v1 [label=<<i>v</i><sub>1</sub>>]
    }
    {
        rank = same
        v2 [label=<<i>v</i><sub>2</sub>>]
        v5 [label=<<i>v</i><sub>5</sub>>]
    }
    {
        rank = same
        v3 [label=<<i>v</i><sub>3</sub>>]
        v4 [label=<<i>v</i><sub>4</sub>>]
    }
    v1 -- v2
    v1 -- v3
    v1 -- v3
    v1 -- v3
    v1 -- v5
    v2 -- v3
    v3 -- v5
    v3 -- v4
    v4 -- v5
}
```

$(i)\>$ Find $A(G)$
$(ii)\>$ Is $A(G)$ symmetric (i.e., $(i,j)$-entry = $(j,i)$=entry)?
$(iii)\>$ What is the sum of the values of the entries in each row (respectively, column)?
$(iv)\>$ What is your interpretation of the 'sum' obtained in $(iii)$?

**Solution**

$(i)$

$$
A(G) = \begin{pmatrix}
0 & 1 & 3 & 0 & 1 \\
1 & 0 & 1 & 0 & 0 \\
3 & 1 & 0 & 1 & 1 \\
0 & 0 & 1 & 0 & 1 \\
1 & 0 & 1 & 1 & 0
\end{pmatrix}
$$

$(ii)\>$ Yes, $A(G)$ is symmetric.
$(iii)\>$ $5, 2, 6, 2, 3$
$(iv)\>$ The sum of the values of the entries in each row corresponds to the total number of edges that vertex is incident with.

---

**Question 1.2.5** The adjacency matrix of a multigraph $G$ is given below:

$$
A = \begin{pmatrix}
    0 & 2 & 1 & 0 & 1 \\
    2 & 0 & 1 & 0 & 0 \\
    1 & 1 & 0 & 3 & 2 \\
    0 & 0 & 3 & 0 & 0 \\
    1 & 0 & 2 & 0 & 0 \\
\end{pmatrix}
$$

Draw a diagram of $G$
**Solution**

```dot
graph {
    {
        v1 [label=<<i>v</i><sub>1</sub>>]
        v2 [label=<<i>v</i><sub>2</sub>>]
        v3 [label=<<i>v</i><sub>3</sub>>]
        v4 [label=<<i>v</i><sub>4</sub>>]
        v5 [label=<<i>v</i><sub>5</sub>>]
    }
    v1 -- v2
    v1 -- v2
    v1 -- v3
    v1 -- v5

    v2 -- v3

    v3 -- v4
    v3 -- v4
    v3 -- v4
    v3 -- v5
    v3 -- v5
}
```

---

## **Exercise 1.2**

(1) Let $G$ be the multigraph representing the following diagram. Determine $V(G)$, $E(G)$, $v(G)$, and $e(G)$. Is $G$ a simple graph?

```dot
graph {
    {
        rank = same
        w [label=<<i>w</i>>]
        m [label=<<i>m</i>>]
    }
    {
        rank = same
        x [label=<<i>x</i>>]
        y [label=<<i>y</i>>]
    }
    {
        rank = same
        n [label=<<i>n</i>>]
    }
    {
        rank = same
        ordering = "in"
        u [label=<<i>u</i>>]
        v [label=<<i>v</i>>]
        z [label=<<i>z</i>>]
        edge [style=invis]
        v -- z
    }
    w -- u
    w -- x

    m -- y

    x -- u
    x -- v
    x -- z

    y -- v
    y -- z

    u -- v
}
```

**Solution**

$$
V(G) = \{w, m, n, x, y, u, v, z\} \\
E(G) = \{ wu, wx, my, xu, xv, xz, yv, yz, uv \} \\
v(G) = 8\\
e(G) = 9
$$

$G$ is a simple graph.

---

(2) Draw the graph $G$ modeling the flight connectivity between twelve capital cities with the following vertex set $V(G)$ and edge set $E(G)$.

$$
\begin{aligned}
V(G) = &\{ \text{Asuncion}, \text{Beijing}, \text{Canberra},  \text{Dili}, \text{Havana}, \text{Kuala Lumpur}, \\
&\text{London}, \text{Nairobi}, \text{Phnom Penh}, \text{Singapore}, \text{Wellington}, \text{Zagreb} \}. \\
E(G) = &\{\text{Asuncion-London}, \text{Asuncion-Havana}, \text{Beijing-Canberra} \\
    &\text{Beijing-Kuala Lumpur}, \text{Beiijng-London}, \text{Beijing-Singapore} \\
    &\text{Beijing-Phnom Penh}, \text{Dili-Kuala Lumpur}, \text{Dili-Singapore} \\
    &\text{Dili-Canberra}, \text{Havana-London}, \text{London-Wellington} \\
    &\text{Kuala Lumpur-London}, \text{Kuala Lumpur-Phnom Penh} \\
    &\text{Kuala Lumpur-Singapore}, \text{Kuala Lumpur-Wellington} \\
    &\text{London-Nairobi}, \text{Phnom Penh-Singapore}, \text{London-Singapore} \\
    &\text{London-Zagreb}, \text{Singapore-Wellington}, \text{Havana-Nairobi}
 \}.
\end{aligned}
$$

(Note that you may use A to represent Asuncion, B to represent Beijing, C to represent Canberra, etc. )

**Solution**

```dot
graph {
    A -- L
    A -- H
    B -- C

    B -- K
    B -- L
    B -- S

    B -- P
    D -- K
    D -- S

    D -- C
    H -- L
    L -- W

    K -- L
    K -- P

    K -- S
    K -- W

    L -- N
    P -- S
    L -- S

    L -- Z
    S -- W
    H -- N
}
```

---

(3) Define a graph $G$ such that $V(G) = \{ 2, 3, 4, 5, 11, 12, 13, 14 \}$ and two vertices $s$ and $t$ are adjacent if and only if $\text{gcd}\{s, t\} = 1$. Draw a diagram of $G$ and find its size $e(G)$.

**Solution**
First we draw the graph $G$

```dot
graph {
    2 -- 3
    2 -- 5
    2 -- 11
    2 -- 13

    3 -- 4
    3 -- 5
    3 -- 11
    3 -- 13
    3 -- 14

    4 -- 5
    4 -- 11
    4 -- 13

    5 -- 11
    5 -- 12
    5 -- 13
    5 -- 14

    11 -- 12
    11 -- 13
    11 -- 14

    12 -- 13
}
```

To find $e(G)$ we simply count all the edges.

```dot
graph {
    2 -- 3  [label=1]
    2 -- 5 [label=2]
    2 -- 11 [label=3]
    2 -- 13 [label=4]

    3 -- 4 [label=5]
    3 -- 5 [label=6]
    3 -- 11 [label=7]
    3 -- 13 [label=8]
    3 -- 14 [label=9]

    4 -- 5 [label=10]
    4 -- 11 [label=11]
    4 -- 13 [label=12]

    5 -- 11 [label=13]
    5 -- 12 [label=14]
    5 -- 13 [label=15]
    5 -- 14 [label=16]

    11 -- 12 [label=17]
    11 -- 13 [label=18]
    11 -- 14 [label=19]

    12 -- 13 [label=20]
}
```

We conclude that $e(G) = 20$.

---

(4) The following diagram is a map of the road system in a town. Draw a multigraph to model the road system, using a vertex to represent a junction and an edge to represent a road joining two junctions.
![Road Map Diagram](image.png)

---
