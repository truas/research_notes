### How do Decisions Emerge across Layers in Neural Models? Interpretation with Differentiable Masking
---
- [Zotero Select Link](zotero://select/groups/2480461/items/IW3Z3KI4)
- [Zotero URI](https://www.zotero.org/groups/2480461/items/IW3Z3KI4)
- Authors: [[Nicola de Cao]]  [[Ivan Titov]] 
- Topics: [[nlp_explain]] [[nlp_attention]] [[nlp_intepretability]]
- Venue: #arxiv #ACL 
- Year: #2020

---
### Major Contributions
- We propose a new method, Differentiable Masking (DIFFMASK), which overcomes the aforementioned limitations and results in attributions that are more informative and help us understand how the model arrives at the prediction.
	- [[DIFFMASK]] relies on learning sparse stochastic gates (a.k.a., masks), guaranteeing that the information from the maskedout inputs does not get propagated while maintaining end-to-end differentiability without having to resort to [[REINFORCE]] (Williams, 1992).
- we study post hoc interpretability where the goal is to explain the prediction of a trained model and to reveal how the model arrives at the decision. This goal is usually approached with attribution methods (Bach et al., 2015; Shrikumar et al., 2017; Sundararajan et al., 2017), which explain the behavior of a model by assigning relevance to inputs.
	- One way to perform attribution is to use [[erasure]] where a subset of features (e.g., input tokens) is considered irrelevant if it can be removed without affecting the model prediction
---
### Secondary Contribution
- We report hyperparameters in Appendix C, and additional plots, examples and analysis in Appendix D.
---
### Limitations/Future Work
- 
---
### Notes (Try to use backlinks)
- Despite its conceptual simplicity, subset erasure is not commonly used in practice. First, it is generally intractable, and beam search (Feng et al., 2018) or leave-one-out estimates (Zintgraf et al., 2017) are typically used instead.
- Second, the method is susceptible to the hindsight bias: the fact that a feature can be dropped does not mean that the model ‘knows’ that it can be dropped and that the feature is not used by the model when processing the example.
- We then probe the model using a shallow interpreter network which takes hidden states up to a certain layer  and outputs a binary mask z = 〈z1, . . . , zn〉 indicating which input tokens are necessary and which can be disregarded
	- Masking, however, as in multiplication by zero, makes a strong assumption about the geometry of the feature space, in particular, it assumes that the zero vector bears no information
- Clearly, there is no direct supervision to estimate the parameters φ of the probe and the baseline b, thus we borrow erasure’s objective: namely, we train the probe to mask-out as many input tokens as possible constrained to keeping f (ˆ x) ≈ f (x). Since often, the output of f parameterizes a likelihood (e.g., a categorical distribution), we formulate the constraint in terms of a divergence D? between the two functions’ outputs. We cast this, rather naturally, in the language of constrained optimization
- **The goal** of this work is to uncover a faithful interpretation of an existing model, i.e. revealing, as accurately as possible, the process by which the model arrives at the prediction
- More precisely, human-provided labels do not show how the model behaves – e.g., annotations of what parts of the input are relevant for solving a particular task do not constitute a guarantee that a model relies on those parts more than others when making a prediction
	- When we evaluate an attribution method by comparing its outputs with human annotations, we are not measuring whether it provides faithful attributions but only if they are plausible according to humans.
- Differently from other methods, [[DIFFMASK]] reveals input attributions conditioned on different levels of depth. Figure 3e shows both input attributions according to the input itself and according to the hidden layer. It reveals that at the embedding layer there is no information regarding what part of the input can be erased: attribution is uniform over the input sequence.
- The F1 score of the model on the validation set moved from 37.9% to 38.3% while masking 46.3% input tokens, and to 38.9% while masking 67.6% hidden states. The explanations provided by DIFFMASK are also stable.
	- n Figure 4a, we show after how many layers on average an input token is dropped, depending on its sentiment label. This suggests that the model relies more heavily on strongly positive or negative words and, thus, is generally consistent with human judgments (i.e., plausible).
- While we motivated our approach through its relation to erasure, an alternative way of looking at our approach is considering it as a perturbationbased method. This recently introduced class of attribution methods (Ying et al., 2019; Guan et al., 2019; Schulz et al., 2020; Taghanaki et al., 2019), instead of erasing input, injects noise.
- We have introduced a new post hoc interpretation method which learns to completely remove subsets of inputs or hidden states through masking. We circumvent an intractable search by learning an end-to-end differentiable prediction model.
- ![[2020_DiffMask_examples.png]]
---
