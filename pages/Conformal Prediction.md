- Conformal prediction is a method for constructing **prediction sets** like interval estimation) for any model.
- Outline
	- Begin with a trained model
	  logseq.order-list-type:: number
	- Calibration step: Create prediction sets (a set of possible labels)  with a small amount of data (called calibration data)
	  logseq.order-list-type:: number
- Detail steps
	- Get a classifier $$\hat{f}(x)\in[0,1]^K$$
	  logseq.order-list-type:: number
	- Reserve a *moderate* number of i.i.d. pairs of $$(X_1, Y_1), \cdots, (X_n, Y_n)$$ as calibration data.
	  logseq.order-list-type:: number
- Goal: Construct a *prediction set* $$C(X_\text{test})$$ with $$1-\alpha \leq \mathbb{P}(Y_\text{test}\in C(X_\text{test})\leq 1-\alpha +\frac{1}{n+1}$$, $$\alpha$$ is an user-chosen error rate
- Calibration step
	- Set *conformal score* $$s_i = 1 - \hat{f}(X_i)_{Y_i}$$ to be $$1$$ minus the softmax output of true label.
-