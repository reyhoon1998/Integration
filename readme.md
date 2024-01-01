# Monte Carlo Integration
### Simple Sampling and Importance Sampling
I can help you with writing a readme file that explains simple sampling and importance sampling for integration. Here is a possible outline of the file:

# Simple Sampling and Importance Sampling for Integration

This file provides a brief introduction to two Monte Carlo methods for approximating integrals: simple sampling and importance sampling.

## Simple Sampling

Simple sampling is a basic technique that uses random samples from a given distribution to estimate the expected value of a function. For example, suppose we want to compute the integral

$$
I = \int_a^b f(x) dx
$$

where $f(x)$ is a continuous function and $a$ and $b$ are finite constants. We can rewrite this integral as

$$
I = (b-a) \int_a^b \frac{f(x)}{b-a} dx = (b-a) E[f(X)]
$$

where $X$ is a uniform random variable on $[a,b]$. To approximate $I$, we can generate $n$ independent samples $X_1, X_2, ..., X_n$ from the uniform distribution and use the sample mean as an estimator:

$$
\hat{I}_n = (b-a) \frac{1}{n} \sum_{i=1}^n f(X_i)
$$

The law of large numbers guarantees that $\hat{I}_n$ converges to $I$ as $n$ increases. The variance of the approximation error is given by

$$
\text{Var}(\hat{I}_n) = \frac{(b-a)^2}{n} \text{Var}(f(X))
$$

which decreases as $n$ increases.

## Importance Sampling

Importance sampling is a variance reduction technique that uses random samples from a different distribution to estimate the expected value of a function. The idea is to choose a distribution that is more similar to the function and gives more weight to the regions where the function is large. For example, suppose we want to compute the integral

$$
I = \int_a^b f(x) dx
$$

where $f(x)$ is a continuous function and $a$ and $b$ are finite constants. We can rewrite this integral as

$$
I = \int_a^b \frac{f(x)}{g(x)} g(x) dx = E[f(X) w(X)]
$$

where $X$ is a random variable with density $g(x)$ and $w(x) = 1/g(x)$ is the importance function. To approximate $I$, we can generate $n$ independent samples $X_1, X_2, ..., X_n$ from the density $g(x)$ and use the weighted sample mean as an estimator:

$$
\hat{I}_n = \frac{1}{n} \sum_{i=1}^n f(X_i) w(X_i)
$$

The law of large numbers guarantees that $\hat{I}_n$ converges to $I$ as $n$ increases. The variance of the approximation error is given by

$$
\text{Var}(\hat{I}_n) = \frac{1}{n} \text{Var}(f(X) w(X))
$$

which can be much smaller than the variance of simple sampling if $g(x)$ is close to $f(x)$.

For more details and examples of simple sampling and importance sampling, you can refer to the following web pages:

- [Importance sampling | Explanation, formulae, example - Statlect](^1^)
- [Importance Sampling - University of Michigan](^2^)
- [Evaluate an integral using importance sampling - Cross Validated](^3^)
- [Monte-Carlo simple integration with importance sampling](^4^)
- [Importance Sampling: Simple Definition - Statistics How To](^5^)

Source: Conversation with Bing, 1/1/2024
(1) Importance sampling | Explanation, formulae, example - Statlect. https://www.statlect.com/asymptotic-theory/importance-sampling.
(2) Importance Sampling - University of Michigan. https://dept.stat.lsa.umich.edu/~jasoneg/Stat406/lab7.pdf.
(3) Evaluate an integral using importance sampling - Cross Validated. https://stats.stackexchange.com/questions/437448/evaluate-an-integral-using-importance-sampling.
(4) Monte-Carlo simple integration with importance sampling. https://math.stackexchange.com/questions/3829811/monte-carlo-simple-integration-with-importance-sampling.
(5) Importance Sampling: Simple Definition - Statistics How To. https://www.statisticshowto.com/importance-sampling/.