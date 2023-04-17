links:: [Local library](zotero://select/library/items/8IKXXS27), [Web library](https://www.zotero.org/users/9801442/items/8IKXXS27)
authors:: [[Yihe Dong]], [[Jean-Baptiste Cordonnier]], [[Andreas Loukas]]
tags:: [[Computer Science - Machine Learning]]
date:: [[Mar 4th, 2021]]
item-type:: [[preprint]]
title:: @Attention is Not All You Need: Pure Attention Loses Rank Doubly Exponentially with Depth

- [[Abstract]]
	- Attention-based architectures have become ubiquitous in machine learning, yet our understanding of the reasons for their effectiveness remains limited. This work proposes a new way to understand self-attention networks: we show that their output can be decomposed into a sum of smaller terms, each involving the operation of a sequence of attention heads across layers. Using this decomposition, we prove that self-attention possesses a strong inductive bias towards "token uniformity". Specifically, without skip connections or multi-layer perceptrons (MLPs), the output converges doubly exponentially to a rank-1 matrix. On the other hand, skip connections and MLPs stop the output from degeneration. Our experiments verify the identified convergence phenomena on different variants of standard transformer architectures.
- [[Attachments]]