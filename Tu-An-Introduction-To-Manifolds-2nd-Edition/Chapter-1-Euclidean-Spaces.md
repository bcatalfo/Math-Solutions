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

So
$$
g'''(x) = 
\begin{cases} 
-\frac{2}{9}x^{-5/3} & \text{for } x \ne 0, \\
\text{undefined} & \text{for } x = 0.
\end{cases}
$$

Thus, \( g \) is \( C^2 \) but not \( C^3 \) at \( x = 0 \).