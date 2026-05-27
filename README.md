# Foundations of Hypothesis Testing

This repository contains self-contained mathematical notes on classical hypothesis testing, with derivations from first principles and an emphasis on probabilistic structure.

## Contents

The notes cover:

- Z-test for known variance  
- One-sample t-test  
- Two-sample t-test (equal and unequal variances)  
- Welch’s t-test and the Welch–Satterthwaite approximation  
- Chi-square tests:
  - Goodness of fit
  - Independence
  - Homogeneity  

## Perspective

Rather than presenting results as formulas, the goal is to derive them from basic probabilistic principles, highlighting:

- Gaussian structure underlying classical tests  
- Geometric interpretation of sample variance  
- Role of chi-square distributions in quadratic forms  
- Asymptotic approximations in large-sample regimes  

## Numerical Experiments

Some of the tests are illustrated using artificially generated data to validate their behaviour in practice.

For example, in the two-sample setting, two datasets are sampled from Gaussian distributions with different means and variances. The Welch t-test is then applied to verify whether it correctly rejects the null hypothesis of equal means under these conditions.

## Aside: Independence as Structure

Motivated by the chi-square test for independence, we discuss what it means mathematically for $n$ discrete random variables to be independent.

In general, a joint discrete distribution

$$
P(x_1,\dots,x_n)
$$

can be viewed as an $n$-way tensor. Under full independence, it factorises as

$$
P(x_1,\dots,x_n) = v_1 \otimes \cdots \otimes v_n,
$$

where each $v_i$ is a probability vector.

From this viewpoint, independence corresponds to a rank-1 tensor structure.

We also describe a simple numerical procedure to test whether a given probability tensor approximately factorises. The method is based on repeated singular value decomposition (SVD), applied to suitable matrix reshaping of the tensor.
