---
layout: post
title: Geometric Series for Operators
subtitle: Obtaining the Inverse by Indirect Meeans
topic: analysis
subtopic: series
date: 2026-09-29
mathjax: true
---

### 1. Introduction
The goal in this section is to use the geometric series in order to obtain another way to prove invertibility of operators. In the end, some ideas are provided.

### 2. Recall

If we recall from complex analysis, a common trick performed in order to find Laurent series expansion of meromorphic functions.

$$ \frac1a = \frac{1}{1-(1-a)} = \sum^\infty_{n=0} (1-a)^n $$

This equality is valid whenever the series converges, which is whenever $\|1-a\|<1$. 

### 3. The Big Idea
Now, what if we used this same idea on operators, namely what if we use the identity operator $I$ and some linear operator $A$ on a Banach space $X$. The Banach space assumption is necessary in order to conclude that $\mathscr{L}(X)$ is a Banach space, which is necessary in order to use the Cauchy criterion to get series convergence (identically to how it is done in basic analysis).

We now assume $\|I-A\|<1$ and consider the operator

$$ B := \sum^\infty_{n=0} (I-A)^n. $$

This series converges because of our assumption and by Cauchy criterion (the upper bound is by $\|I-A\|^n$).

Now, notice that

$$ (I-A)B = \sum^\infty_{n=1} (I-A)^n = B - (I-A)^0 = B - I. $$

Therefore, $I = (I-(I-A))B = AB$.

Note that $A$ and $B$ are commutative by virtue of being polynomials of the same elements. Thus, we have proven the following:

{: .box-warning} 
**Theorem:** $\|I-A\|<1$ implies $A$ is invertible.

### 4. Closing Remarks

An interesting thing to note is that we can approximate the inverse by truncating the series. So for example, we have

$$ A^{-1} \approx \sum^N_{n=0} (I-A)^n $$
, though I don't recall ever seeing this result used in practice. The invertibility of $A$ here is mainly used inside of bigger theorem proofs to extract invertibility.
