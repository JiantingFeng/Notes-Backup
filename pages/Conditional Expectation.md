- Definition:
	- $$\mathbb{E}X = \sum_{X\in\Omega}X(\omega)P(\omega)$$
	- If $$A\subset \Omega$$, then
		- $$\mathbb{E}(1_AX) = \int_AXdP=\sum_{\omega\in A} X(\omega)P(\omega)$$
- Partial Averaging Property
	- Given probability space $$(\Omega, \mathcal{F}, P)$$
	- Let $$\mathcal{G}$$ be a subfield of $$\mathcal{F}$$ and $$A\in \mathcal{G}$$, then $$\int_{A}\mathbb{E}[X\vert \mathcal{G}]dP = \mathbb{E}[1_A\mathbb{E}[X\vert \mathcal{G}]] = \mathbb{E}[\mathbb{E}[1_A X\vert \mathcal{G}]] = \mathbb{E}[1_A X] = \int_{A} XdP$$
	- When $$A = \Omega$$, above equation becomes double-expectation law.
- Notion
	- For random variables $$X, Y$$, the standard notation is
		- $$\mathbb{E}(X\vert Y) = \mathbb{E}(X\vert \sigma(Y))$$
		- Where $$\sigma(Y)$$ is the sigma field generated by $Y$