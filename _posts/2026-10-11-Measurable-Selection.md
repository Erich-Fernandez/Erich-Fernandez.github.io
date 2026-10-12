---
layout: post
title: Measurable Selection
subtitle: A measurable axiom of choice
topic: set theory
subtopic: Descriptive Set Theory
date: 2026-10-11
mathjax: true
---

### 1. Some Motivation


Suppose we have a trading strategy that can be continuously changed at any time and is specified by parameters. Suppose we also have a function 
$$f(\text{time} = t, \text{strategy} = (\text{parameter}_i)_{i=1}^n)$$ 
that tells us our expected profit if we utilize strategy $(\text{parameter}_i)_{i=1}^n$ at time $t$. 

Of course, we will be interested in the function $F(t)$ such that 

\[ F(t) = \underset{x\in\{\text{valid strategies}\}}{\text{max}} f(t, x) \]

We might be interested in doing things with this function $F(t)$, like say integrating it in order to get our total expected profit across a time period. However, we run into a huge problem. How do we know that this function $F(t)$ is even measurable? This is the motivation for the succeeding theorem, which I will state and (roughly) prove. 



