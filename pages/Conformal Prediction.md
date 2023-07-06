- Conformal prediction is a method for constructing **prediction sets** like interval estimation) for any model.
- Outline
	- Begin with a trained model
	  logseq.order-list-type:: number
	- Calibration step: Create prediction sets (a set of possible labels)  with a small amount of data (called calibration data)
	  logseq.order-list-type:: number
- Detail steps:
	- Get a classifier $$\hat{f}(x)\in[0,1]^K$$
	  logseq.order-list-type:: number
	- Reserve a *moderate* number of i.i.d. pairs fo
	  logseq.order-list-type:: number
- Goal: Construct a *prediction set* $$C(X_\text{test})$$ with