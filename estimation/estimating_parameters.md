# Estimating Parameters

## Model

### Discrete 

| Distribution | Support |Parameters | Formulas |
|:-------------|:--------|:----------|:---------|
| $X \sim Geometric(p)$ | $X$ : Number of trials required to get first success | • $p$ : Success probability of each trial | • $f_X(X=k;p) = (1-p)^{k-1} \cdot p$ <br> • $E(X) = \frac{1}{p}$ <br> • $Var(X) = \frac{1-p}{p^2} := \frac{q}{p^2}$|
| $X \sim Binomial(p)$ | $X$ : Number of successful trials of `n` trials | • $p$ : Success probability of each trial | • $f_X(X=k) = {n \choose k} \cdot p^k \cdot (1-p)^{n-k}$<br> • $E(X) = n \cdot p$ <br> • $Var(X) = n \cdot p \cdot (1-p) := n \cdot p \cdot q$ |
| $X \sim Poisson(\lambda)$ | $X$ : Number of times an event occurs | • $\lambda$ : Avg. rate of occurrence of an event | • $f_X(X=k; \lambda) = \frac{exp(- \lambda) \cdot \lambda^k}{k!}$ <br> • $E(X) = Var(X) = \lambda$ |
| $X \sim NegativeBinomial(r,p)$ | $X$ : Number of trials required to get $r^{th}$ success | • $r$ : Number of success out of `k` trials <br> • $p$ : Success probability of each trial | • $f_X(X=k) = {k-1 \choose r-1}\cdot p^r \cdot (1-p)^{k-r}$ <br> • $E(X) = \frac{r}{p}$ <br> • $Var(X) = \frac{r(1-p)}{p^2}$ |

### Continuous

1. For a PDF the two conditions are as follows :
	1. $f_X(X) \geq 0, \forall X$
	2. $\int_{-\infty}^{\infty} f_X(X) dX = 1$

| Distribution | Support |Parameters | Formulas |
|:-------------|:--------|:----------|:---------|
| $X \sim Uniform(a,b)$ | | $a$ : Start of interval <br> b : End of interval | • $f_X(X=x;a,b) = \begin{cases}\frac{1}{b-a} & x \in [a,b] \\ 0 & x \in \mathbb{R}\setminus[a,b] \end{cases}$ <br>  • $E(X)=\frac{a+b}{2}$ <br>  • $Var(X)=\frac{(b-a)^2}{12}$ |
| $X \sim Exponential(\lambda)$ | $X$ : How long we must wait for an event to occur | $\lambda$ : Avg. rate of occurrence of an event | • $f_X(X=x; \lambda)=\begin{cases}\lambda \cdot exp(-\lambda \cdot x) & x \geq 0 \\ 0 & \mathbb{R}\setminus[0,\infty) \end{cases}$ <br> • $E(X)= \frac{1}{\lambda}$ <br> • $Var(X)=\frac{1}{\lambda^2}$|    
| $X \sim Normal(\mu, \sigma^2)$ | | • $\mu$ : Mean <br> • $\sigma^2$ : Variance | • $f_X(X=x; \mu, \sigma^2)=\frac{1}{\sqrt{2\pi\sigma^2}} exp(\frac{-(x-\mu)^2}{2\sigma^2})$ <br> • $E(X) = \mu$ <br> • $Var(X) = \sigma^2$ |
| $X \sim Gamma(r, \lambda)$ | $X$ : Time required to see `r` instances of an event | $\lambda$ : Avg. rate of an event | • $\Gamma(r)=\int_{0}^{\infty} y^{r-1} \cdot e^{-y} dy = r \cdot \Gamma(r-1), \forall r > 0$ <br> • $f_X(X=x;r,\lambda)=\frac{\lambda^r}{\Gamma(r)} \cdot x^{r-1} \cdot exp(-\lambda \cdot x), x > 0, r > 0, \lambda > 0$ |

## Method of Moments
1. 

## Method of Maximum Likelihood
1. 