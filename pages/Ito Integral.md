- Stochastic Process: $$X_t: [0, T]\times \Omega\to \mathbb{R}$$
- We have SDE $$\mathrm{d}X_t = \mu \mathrm{d}t + \sigma \mathrm{d}W_t$$, where $$W_t$$ is Wiener process, drift $$\mu = \mu(t, X_t)$$ and variance $$\sigma = \sigma(t, X_t)$$
- Compared to ODE, the solution can be written in the form $$X_t = X_0 + \int_{0}^t \mu \mathrm{d}s+ \int_{0}^t\sigma \mathrm{d}W_s$$ called Ito integral
	- The first term (drift term) $$\int_0^t\mu \mathrm{d}s$$ is just a Riemann integral
	- The second term (diffusion term) $$\int_0^t\sigma \mathrm{d} W_s$$ is Ito integral w.r.t. Wiener process.
- Example, Geometry Brownian Motion
	- $$\mathrm{d}S_t = \mu S_tdt + \sigma S_t \mathrm{d}W_t$$
	- where $$\mu$$ and $$\sigma$$ are constant term
- Ito Lemma
	- Suppose $$f(x, t)$$ is twice differentiable, $$X_t$$ is a stochastic process satisfying $$\mathrm{d}X_t = \mu_t\mathrm{d} t+\sigma_t \mathrm{d} W_t$$
	- Take derivative $$\mathrm{d} f = \dfrac{\partial f}{\partial t} \mathrm{d} t + \dfrac{\partial f}{\partial x} \mathrm{d}x + \dfrac{1}{2}\dfrac{\partial^2 f}{\partial x^2}\mathrm{d}x^2 $$
	- Substituting $$x$$ with $$X_t$$, we get $$\mathrm{d} f = \dfrac{\partial f}{\partial t} \mathrm{d} t + \dfrac{\partial f}{\partial x} \left(\mu_t\mathrm{d} t+\sigma_t \mathrm{d} W_t\right) + \dfrac{1}{2}\dfrac{\partial^2 f}{\partial x^2}\left(\mu_t\mathrm{d} t+\sigma_t \mathrm{d} W_t\right)^2 $$
		- Note $$(\mathrm{d} W_t)^2 = \mathrm{d}t$$, we get Ito lemma
		- $$\mathrm{d} f = \left(\dfrac{\partial f}{\partial t} + \mu_t\dfrac{\partial f}{\partial x} + \dfrac{\sigma_t^2}{2}\dfrac{\partial^2 f}{\partial x^2}\right)\mathrm{d} t + \sigma_t \dfrac{\partial f}{\partial x}\mathrm{d} W_t$$
	-