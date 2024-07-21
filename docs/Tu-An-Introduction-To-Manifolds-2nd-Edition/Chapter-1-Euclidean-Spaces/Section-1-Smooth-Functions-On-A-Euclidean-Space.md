---
export_on_save:
  html: true
---
<style>
.katex-display { overflow: auto hidden }
</style>

# \(\S 1\) - Smooth Functions on a Euclidean Space

## 1.1. A function that is \( C^2 \) but not \( C^3 \)

Let \( g: \mathbb{R} \to \mathbb{R} \) be the function in Example 1.2(iii). Show that the function \( h(x) = \int_0^x g(t) \, dt \) is \( C^2 \) but not \( C^3 \) at \( x = 0 \).

### Solution

First, recall that \( g: \mathbb{R} \to \mathbb{R} \) is defined as 
$$  
g(x) = \frac{3}{4}x^{4/3} 
$$

So
$$  
g'(x) = x^{1/3}
$$

And
$$
g''(x) = 
\begin{cases} 
\frac{1}{3}x^{-2/3} & \text{for } x \ne 0, \\
\text{undefined} & \text{for } x = 0.
\end{cases}
$$
By the fundamental theorem of calculus \( h'(x) = g(x)\), so this shows that \( h \) is \( C^2 \) but not \( C^3 \) at \( x = 0 \) (as \( h''' = g'' \) ). Note that \( h \) is a polynomial and therefore continuous.

## 1.2.* A \( C^\infty \) function very flat at 0

Let \( f(x) \) be the function on \( \mathbb{R} \) defined in Example 1.3.

### (a)
Show by induction that for \( x > 0 \) and \( k \geq 0 \), the \( k \)-th derivative \( f^{(k)}(x) \) is of the form \( p_{2k}(1/x)e^{-1/x} \) for some polynomial \( p_{2k}(y) \) of degree \( 2k \) in \( y \).

#### Solution

First recall that \( f(x) \) is defined on \(\mathbb{R}\) by
$$
f(x) =
\begin{cases}
e^{-1/x} & \text{for } x > 0, \\
0 & \text{for } x \leq 0
\end{cases}
$$
The base case of the induction is for \( k = 0 \). By definition when \( x > 0\) we have \( f(x) = e^{-1/x} = 1 \cdot e^{-1/x} \), proving the hypothesis via the polynomial \( p_0(y) = 1 \) which is of degree \( 2k = 0\).

Now assume that \( f^{(k)}(x) = p_{2k}(1/x)e^{-1/x} \). We need to show that \( f^{(k+1)}(x) = p_{2k+2}(1/x)e^{-1/x} \) for some polynomial \( p_{2k+2}\) of degree \( 2k + 2\). Proceed by differentiating 
$$
\begin{aligned}
f^{(k+1)}(x) &= \frac{d}{dx} \left( p_{2k}\left(\frac{1}{x}\right) e^{-1/x} \right) \\
&= \frac{d}{dx} \left( p_{2k}\left(\frac{1}{x}\right) \right) e^{-1/x} + p_{2k}\left(\frac{1}{x}\right) \frac{d}{dx} e^{-1/x} \\
&= p_{2k}'\left(\frac{1}{x}\right) \cdot \left(-\frac{1}{x^2}\right) e^{-1/x} + p_{2k}\left(\frac{1}{x}\right) \cdot \left(-\frac{1}{x^2}\right) e^{-1/x} \\
&= -\frac{1}{x^2} \left( p_{2k}'\left(\frac{1}{x}\right) + p_{2k}\left(\frac{1}{x}\right) \right) e^{-1/x}
\end{aligned}
$$
Since $p_{2k}$ is of degree \( 2k \), \(p'_{2k}\) is of degree \( 2k - 1 \), so \( \left( p_{2k}'\left(\frac{1}{x}\right) + p_{2k}\left(\frac{1}{x}\right) \right) \) is of degree \( 2k \), and \( p_{2k+2} = -\frac{1}{x^2} \left( p_{2k}'\left(\frac{1}{x}\right) + p_{2k}\left(\frac{1}{x}\right) \right) \) is of degree \( 2k + 2 \).



### (b)
Prove that \( f \) is \( C^\infty \) on \( \mathbb{R} \) and that \( f^{(k)}(0) = 0 \) for all \( k \geq 0 \).

#### Solution
To prove that \( f \) is \( C^{\infty}\) on \( \mathbb{R} \) it is sufficient to show that it is smooth at \( x = 0 \), as we handled that case \( x > 0 \) in part (a) and the case \( x < 0 \) is trivial as we have a whole epsilon ball where \( f = 0 \). Take \( k \geq 0 \), we need to show that the limit
$$
\lim_{h \to 0} \frac{f^{(k)}(h) - f^{(k)}(0)}{h}
$$ 
exists, and for the second part of the question we need to show that it equals to zero. We proceed by induction. For the base case \( k = 0 \) we have that
$$
\lim_{h \to 0} \frac{f^{(k)}(h) - f^{(k)}(0)}{h} = \lim_{h \to 0} \frac{f(h) - f(0)}{h} 
$$ 
This splits into two cases: approaching from the left and from the right. From the left we always have \( h < 0 \) so
$$
\lim_{h \to 0^-} \frac{f(h) - f(0)}{h} = \lim_{h \to 0^-} \frac{0 - 0}{h} = 0
$$
From the right we always have \( h > 0 \) so 
$$
\lim_{h \to 0^+} \frac{f(h) - f(0)}{h} = \lim_{h \to 0^+} \frac{e^{-1/h} - 0}{h}
$$
Let \( y = 1/h \) so as \( h \to 0^+\) we have \( y \to \infty \)
$$
\lim_{h \to 0^+} \frac{e^{-1/h} - 0}{h} = \lim_{y \to \infty} ye^{-y} = \lim_{y \to \infty} \frac{y}{e^y} = 0
$$
The last equality follows from L'Hospital's Rule. Now it's time for the induction. Assume that 
$$
\lim_{h \to 0} \frac{f^{(k)}(h) - f^{(k)}(0)}{h} = 0
$$ 
We need to show that (note that the following limit is not even assumed to exist)
$$
\lim_{h \to 0} \frac{f^{(k+1)}(h) - f^{(k+1)}(0)}{h} = 0
$$ 
From the assumption it is clear that \(f^{(k+1)}(0) = 0 \) so all that remains to show is that
$$
\lim_{h \to 0} \frac{f^{(k+1)}(h)}{h} = 0
$$ 
If \(h\) approaches from the left than this is obvious as the left side of the function is identically zero (since the left side of \(f \) is zero so are all of its derivatives). So without loss of generality approach from the right, and use part (a)
$$
\lim_{h \to 0^+} \frac{f^{(k+1)}(h)}{h} = \lim_{h \to 0^+}\frac{p_{2k+2}(1/h)e^{-1/h}}{h} = \lim_{h \to 0^+} \frac{p_{2k+3}(1/h)}{e^{1/h}}
$$ 
Once again substitute \( y = 1/h\)
$$
\lim_{h \to 0^+} \frac{f^{(k+1)}(h)}{h} = \lim_{y \to \infty} \frac{p_{2k+3}(y)}{e^{y}} = 0
$$
The last equality following from repeated applications of L'Hospital's Rule.