---
title: Policy Gradient Method
---

- Setting
	 - Policy gradient methods target at modeling and optimizing the policy directly.

	 - Policy is parameterized by $$\theta$$, $$\pi_\theta(s\vert a)$$

	 - The goal is to maximize reward, $$J(\theta) = \displaystyle\sum_{s\in\mathcal{S}}d^{\pi}(s)V^{\pi}(s)=\displaystyle\sum_{s\in\mathcal{S}}d^{\pi}(s)\sum_{a\in\mathcal{A}}\pi(a\vert s)Q^{\pi}(s, a)$$

	 - $$d^{\pi}(s)$$ is the stationary distribution of Markov chain, i.e. $$d^{\pi}(s)=\displaystyle\lim_{t\to\infty}P(s_t=s\vert s_0, \pi_0)$$

- Policy Gradient Theorem
	 - $$\nabla_\theta J(\theta) = \nabla_\theta\left(\displaystyle\sum_{s\in\mathcal{S}}d^{\pi}(s)\sum_{a\in\mathcal{A}}\pi(a\vert s)Q^{\pi}(s, a)\right)$$

	 - Under certain regularity condition, $$\nabla_\theta$$ can put before $$\pi_\theta(a\vert s)$$
