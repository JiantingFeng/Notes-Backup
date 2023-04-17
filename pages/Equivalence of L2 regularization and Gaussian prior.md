---
title: Equivalence of L2 regularization and Gaussian prior
---

- Normally we assume $$L2$$ regularization as a technique to prevent overfitting.

- Here, we give a **Bayesian** perspective to explain it, follows https://bjlkeng.github.io/posts/probabilistic-interpretation-of-regularization/

- Consider ordinary linear regression, which minimize the square difference between the predictions and ground truth.

- $$\hat{\beta}_\text{MLE} = \displaystyle\arg\min_{\beta}\sum_{i=1}^n\left(y_i-(\beta_0+\beta_1x_{i, 1} + \cdots + \beta_px_{i, p})\right)^2$$

- Regularization:
	 - L1: $$\hat{\beta}_\text{L1} = \displaystyle\arg\min_{\beta}\left(\sum_{i=1}^n\left(y_i-(\beta_0+\beta_1x_{i, 1} + \cdots + \beta_px_{i, p})\right)^2+\lambda\sum_{j=0}^p\vert \beta_j\vert \right)$$

	 - L2:  $$\hat{\beta}_\text{L2} = \displaystyle\arg\min_{\beta}\left(\sum_{i=1}^n\left(y_i-(\beta_0+\beta_1x_{i, 1} + \cdots + \beta_px_{i, p})\right)^2+\lambda\sum_{j=0}^p\vert \beta_j\vert^2 \right)$$

- The Likelihood: $$L(\beta\vert y) = P(y\vert \beta) = \prod_{i=1}^n P_Y(y_i\vert \beta, \sigma^2)=\prod_{i=1}^n\frac{1}{\sigma\sqrt{2\pi}}\exp\left\{-\frac{(y_i-(\beta_0 + \beta_1x_{i, 1} +\cdots + \beta_px_{i, p}))}{2\sigma^2}\right\}$$

- Bayesian Inference: 
	 - $$P(\theta\vert y) = \frac{P(y\vert \theta) P(\theta)}{P(y)}$$

	 - $$\text{posterior} = \frac{\text{likelihood}\cdot\text{prior}}{\text{evidence}}$$

- Finding a MAP (maximum a posterior) solution
	 - $$\hat{\theta}_{MAP} = \displaystyle\arg\max_{\theta} P(\theta\vert y)= \displaystyle\arg\max_{\theta} \frac{P(y\vert \theta) P(\theta)}{P(y)} = \displaystyle \arg\max_{\theta}\left(\log P(y\vert \theta) + \log P(\theta)\right)$$

- Conclusion
	 - **For $$L1$$ regularization, the prior follows [[Laplace distribution]]**

	 - **For $$L2$$ regularization, the prior follows Normal distribution**

	 - Different regularization methods represent different prior ([[Laplace distribution]] or gaussian) of parameters $$\theta$$, the predictions always follow $$\mathcal{N}(\hat{y}, \sigma^2)$$
