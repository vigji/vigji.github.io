---
title: "The World is Smooth Enough"
date: 2025-06-10
draft: true
math: true
description: "Or a microprocessor. Or a brain. Or none?"
---

{{< epigraph author="Huh et al," cite="[The Platonic Representation Hypothesis](https://arxiv.org/html/2405.07987v1/)" >}}
Under mild conditions that the world is smooth enough, a choice of $ f_X $ can exactly represent $ K_{𝖯𝖬𝖨} $...{{< /epigraph >}}

## Math test

Inline math works like this: the mutual information $I(X;Y) = \sum_{x,y} p(x,y) \log \frac{p(x,y)}{p(x)p(y)}$ between two variables measures their statistical dependence.

Display equations go on their own line:

$$
K_{\text{PMI}}(x, y) = \log \frac{P(x, y)}{P(x) P(y)}
$$

And a more complex example with aligned equations:

$$
\begin{aligned}
H(X) &= -\sum_x p(x) \log p(x) \\
H(X|Y) &= -\sum_{x,y} p(x,y) \log p(x|y) \\
I(X;Y) &= H(X) - H(X|Y)
\end{aligned}
$$