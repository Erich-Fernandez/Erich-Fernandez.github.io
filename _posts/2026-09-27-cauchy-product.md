---
layout: post
title: Cauchy Products
subtitle: A Review of Cauchy Products and an Application to Semigroups
topic: analysis
subtopic: series
date: 2026-09-27
mathjax: true
---

In this blog post, my goal is to present the proof of a classical result in semigroup theory. 

### 1. Recalling the Cauchy Product
Remember that one obscure theorem you learned in your undergraduate analysis class, but barely ever really used? I'm talking about the cauchy product of two series. Specifically, remember the following result:

$$ (\sum^\infty_{n=0}a_n)(\sum^\infty_{m=0}b_m) = \sum^\infty_{k=0}\sum^k_{j=0} a_j b_{k-j}. $$

If you don't, no need to worry. All you need to remember are two things: (1) if the LHS series converges and at least one of them converges absolutely, then the equality holds, and (2) if the RHS series converges, then the equality also automatically holds.

{: .box-note}
**Note:** If you're still a bit confused, the key to understanding this result is to envision an invisible $x^n$ next to the series terms and treat these series as the evaluation of a power series at $x=1$. This serves as both a motivation and intuition for the proof to follow.

### 2. Cauchy Products in Operator Spaces
I recently came across the following statement which was the motivation for this post. How do I justify the following claim in the book: If $A$ is some bounded linear operator on some Banach space $X$, then $e^{(t+s)A}=e^{tA}e^{sA}$.

Essentially, this boils down to proving the following result:

$$ \sum^\infty_{n=0} \frac{((t+s)A)^n}{n!} 
= \sum^\infty_{n=0} \sum^n_{k=0} \binom{n}{k}\frac{1}{n!} (tA)^k (sA)^{n-k} = \sum^\infty_{n=0} \frac{(tA)^n}{n!}\sum^\infty_{n=0} \frac{(sA)^n}{n!}$$

The first equality is just a trivial binomial expansion in commutative rings whereas the second one is an operator version of the exact cauchy product we just talked about. I will now present a proof sketch for the real numbers cauchy product result. Then, by simply replacing the symbols with operators, the exact same proof reveals the equality. 

Assuming the $a_n$ series sum absolutely converges, the key to the proof is to note that 
$$\sum^n_{k=0}\sum^k_{j=0} a_j b_{k-j} = a_0(b_0+\dots+b_n) + a_1(b_0+\dots+b_{n-1}) + \dots + a_n(b_0).$$

From here, it is a simple manner of brute forcing the convergence by noticing that the partial sums $b_0+\dots+b_j$ that are close to the value of the full series sum are paired with the low index $a_{k-j}$ terms and that the partial sums that are still far from the true value are paired with the higher $a_n$ values. By performing a Kronecker-like proof, we can easily conclude the result.

### 3. Closing Thoughts
I hope this was helpful to people who needed a quick refresher on cauchy products.

