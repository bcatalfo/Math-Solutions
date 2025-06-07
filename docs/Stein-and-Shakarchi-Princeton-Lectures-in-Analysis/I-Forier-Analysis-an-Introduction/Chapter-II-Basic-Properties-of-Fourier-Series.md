---
export_on_save:
  html: true
---

<style>
.katex-display { overflow: auto hidden }
.tikz { display: flex; justify-content: center; align-items: center}
</style>

# Princeton Lectures in Analysis I - Fourier Analysis: An Introduction

## Chapter II - Basic Properties of Fourier Series

### Exercises

$\textbf{1.} \>$ Suppose $f$ is $2 \pi$-periodic and integrable on any finite interval. Prove that if $a,b \in \R$, then

$$
\int_{a}^{b} f(x) \, dx = \int_{a+2\pi}^{b+2\pi} f(x) \, dx = \int_{a-2\pi}^{b-2\pi} f(x) \, dx.
$$

Also prove that

$$
\int_{-\pi}^{\pi} f(x+a) \, dx = \int_{-\pi}^{\pi} f(x) \, dx = \int_{-\pi + a}^{\pi + a} f(x) \, dx.
$$

---

$\textbf{2.} \>$ In this exercise we show how the symmetries of a function imply certain properties of its Fourier coefficients. Let $f$ be a $2 \pi$-periodic Riemann integrable function defined on $\R$.

$\quad \text{(a)} \>$ Show that the Fourier series of the function $f$ can be written as 

$$
f(\theta) \sim \hat{f}(0) + \sum_{n \geq 1} [\hat{f}(n) + \hat{f}(-n)] \cos n \theta + i [\hat{f}(n) - \hat{f}(-n)]\sin n\theta.
$$

$\quad \text{(b)} \>$ Prove that if $f$ is even, then $\hat{f}(n) = \hat{f}(-n)$, and we get a cosine series.
$\quad \text{(c)} \>$ Prove that if $f$ is odd, then $\hat{f}(n) = -\hat{f}(-n)$, and we get a sine series.
$\quad \text{(d)} \>$ Prove that $f(\theta + \pi) = f(\theta)$ for all $\theta \in \R$. Show that $\hat{f}(n) = 0$ for all odd $n$.
$\quad \text{(e)} \>$ Show that $f$ is real-valued if and only if $\overline{\hat{f}(n)} = \hat{f}(-n)$ for all $n$.

---


### Problems

$$
\\
$$