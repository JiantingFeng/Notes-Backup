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
		- This score will be high if the model is likely to be wrong
	- Define $$\hat{q}$$ to be $$(n+1)(1-\alpha)/n$$ empirical quantile of $$s_1, \cdots, s_n$$
	- For a new data point,  create a prediction set $$C(X_\text{test}) = \{y: \hat{f}(X_\text{test})_y\geq 1 - \hat{q}\}$$
	- Code:
		- ```python
		  # 1: get conformal scores. n = calib_Y.shape[0]
		  cal_smx = model(calib_X).softmax(dim=1).numpy()
		  cal_scores = 1-cal_smx[np.arange(n),cal_labels]
		  # 2: get adjusted quantile
		  q_level = np.ceil((n+1)*(1-alpha))/n
		  qhat = np.quantile(cal_scores, q_level, method='higher')
		  val_smx = model(val_X).softmax(dim=1).numpy()
		  prediction_sets = val_smx >= (1-qhat) # 3: form prediction sets
		  ```