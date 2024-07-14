---
export_on_save:
  html: true
---

# Chapter 1 - Euclidean Spaces

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

