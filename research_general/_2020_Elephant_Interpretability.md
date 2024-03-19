### The elephant in the interpretability room: Why use attention as explanation when we have saliency methods?
---
- [Zotero Select Link](zotero://select/groups/2480461/items/YLEKDTRL)
- [Zotero URI](https://www.zotero.org/groups/2480461/items/YLEKDTRL)
- Authors: [[Jasming Bastings]]  [[Katja Filippova]] 
- Topics: [[tag1]] [[tag2]]
- Venue: #arxiv #ACL #google #workshop
- Year: #2020

---
### Major Contributions
- While attention conveniently gives us one weight per input token and is easily extracted, it is often unclear toward what goal it is used as explanation
	- input saliency methods are better suited, and that there are no compelling reasons to use attention, despite the coincidence that it provides a weight for each input
- The elephant in the room is therefore: If the goal of using attention as explanation is to assign importance weights to the input tokens in a faithful manner, why should the attention mechanism be preferred over the multitude of existing input saliency methods designed to do exactly that?
	- We propose that we reduce our focus on attention as explanation, and shift it to input saliency methods instead. However, we do emphasize that understanding the role of attention is still a valid research goal (§5), and finally, we discuss a few approaches that go beyond saliency (§6).
---
### Secondary Contribution
- 
---
### Limitations/Future Work
- We leave out more expensive methods that use a surrogate model, e.g., [[LIME]] (Ribeiro et al., 2016)
- A known problem with occlusion-based saliency methods as well as erasure-based evaluation of any input saliency technique (Bach et al., 2015; DeYoung et al., 2020) is that changes in the predicted probabilities may be due to the fact that the corrupted input falls off the manifold of the training data (Hooker et al., 2019).
	- That is, a drop in probability can be explained by the input being OOD and not by an important feature missing.
---
### Notes (Try to use backlinks)
- Attention has not only allowed for better performance, it also provides a window into how a model is operating.
- Jain and Wallace (2019) show that attention is often uncorrelated with gradient-based feature importance measures, and that one can often find a completely different set of attention weights that results in the same prediction.
	- Wiegreffe and Pinter (2019) claim that these works do not disprove the usefulness of attention as explanation per se, and provide four tests to determine if or when it can be used as such.
	- , Pruthi et al. (2020) propose a method to produce deceptive attention weights. Their method reduces how much weight is assigned to a set of ‘impermissible’ tokens
- In this section we discuss various input saliency methods for NLP as alternatives to attention:
	- gradient-based (§3.1), 
	- propagation-based (§3.2), and 
	- occlusion-based methods (§3.3), following Arras et al. (2019).
- We propose distinguishing **sensitivity** from **saliency**, following Ancona et al. (2019): 
	- Sensitivity - says how much a change in the input changes the output, 
	- Saliency is the marginal effect of each input word on the prediction. 
- gradient-based
	- **Gradients measure sensitivity**, whereas **gradient×input and IG measure saliency**. 
	- A model can be sensitive to the input at a time step, but it depends on the actual input vector if it was important for the prediction.
- propagation-based
	- **Layer-wise Relevance Propagation (LRP)** in particular, start with a forward pass to obtain the output fc(x1:n), which is the top level **relevance**.
		- They then use a special backward pass that, at each layer, redistributes the incoming relevance among the inputs of that layer. Each kind of layer has its own propagation rules
- occlusion-based methods
	- Occlusion-based methods (Zeiler and Fergus, 2014; Li et al., 2016b) compute input saliency by occluding (or erasing) input features and measuring how that affects the model.
		- Intuitively, erasing unimportant features does not affect the model, whereas the opposite is true for important features
- In many of the cited papers, whether implicitly or explicitly, the goal of the explanation is to reveal which input words are the most important ones for the final prediction. This is perhaps a consequence of attention computing one weight per input, so it is necessarily understood in terms of those inputs.
- Input saliency methods are addressing the goal head-on: they reveal why one particular model prediction was made in terms of how relevant each input word was to that prediction.
- Attention weights do not: they reflect, at one point in the computation, how much the model attends to each input representation, but those representations might already have mixed in information from other inputs.
- “it only takes one line in a framework like TensorFlow to compute the gradient of the output w.r.t. the input word embeddings, so implementation difficulty is not a strong argument.” (Bastings and Filippova, 2020, p. 152)
- The [[DiffMask]] method of DeCao et al. (2020) adds another dimension: it not only reveals in what layer a model knows what inputs are important, but also where important information is stored as it flows through the layers of the model.
---
