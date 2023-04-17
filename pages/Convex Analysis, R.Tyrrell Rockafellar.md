---
title: Convex Analysis, R.Tyrrell Rockafellar
---

- PART 1. BASIC CONCEPTS
	 - Affine Sets
		 - Def: A subset set $$M\subset \mathbb{R}^n$$ is called an **affine set** if $$(1-\lambda)x+\lambda y\in M$$ for every $$x\in M, \lambda\in\mathbb{R}$$. Affine set is also referred as **affine manifold**, **affine variety**, **linear variety** or **flat**.

		 - E.g.: $$\emptyset$$ and $$\mathbb{R}^n$$ itself are affine sets.

		 - Thm 1.1: the subspaces of $$\mathbb{R}^n$$ are the affine sets which contain the origin. (Closed under addition and scaler multiplication)

		 - Define **translate** of $$M$$: $$M+a = \{x+a\vert x\in M\}$$, it's also an affine set.

	 - Convex Sets and Cones
		 - Def: A subset $$C\subset \mathbb{R}^n$$ is **convex** if $$(1-\lambda)x+\lambda y\in C$$ whenever $$x, y\in C$$ and $$\lambda \in (0, 1)$$

		 - Convex sets are affine, however affine sets are not convex (e.g. non-convex affine set)

		 - The intersection of arbitrary convex sets is convex. (verifying the definition of convexity and intersection)

		 - Vector sum $$\sum_{i=1}^n\lambda_ix_i$$ is called a **convex combination** if $$\lambda_i\geq 0$$ and $$\sum_{i=1}^n\lambda_i=1$$

		 - Def: A subset $$K\subset \mathbb{R}^n$$ is called a **cone** if $$\lambda x\in K$$ for any $$x\in K$$ and $$\lambda > 0$$, i.e. closded under positive multiplication. If the cone is convex then it is called **convex cone**.

	 - Algebra of Convex sets
