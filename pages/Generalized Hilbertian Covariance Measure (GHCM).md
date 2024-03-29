- a conditional independence **measure**, testing $$X\perp Y\vert Z$$
- regressing $$X$$ and $$Y$$ respectively on $$Z$$, and computing a test statistics formed from inner products of pairs of residuals
- Motivation: Generalized Covariance Measure (GCM)
	- We can always write $$X = f(Z)+\varepsilon$$ and $$Y = g(Z)+\xi$$, then the conditional covariance is $$Cov(X, Y\vert Z) = E(\varepsilon\xi^\top\vert Z)$$
	- Under null hypothesis (conditional independent) $$E(\varepsilon \xi^\top\vert Z) \in \mathbb{R}^{d_X\times d_Y}$$ is a zero matrix
- Preliminaries
	- [[Hilbert-Schimidt operator]]