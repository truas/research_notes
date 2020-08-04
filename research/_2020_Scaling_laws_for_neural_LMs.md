### Scaling Laws for Neural Language Models

---
- [Zotero Select Link](zotero://select/groups/2480461/items/AR8UUGFZ)
- [Zotero URI](https://www.zotero.org/groups/2480461/items/AR8UUGFZ)
- Author: [[Jared Kaplan]] [[Sam McCandlish]] [[Dario Amodei]]
- Topics: [[nlp_theory]]
- Venue: #arXiv 
- Year: #2020
---
### Techniques
- 
---
### Goal
---
To empirically analyze transformer model performance in relation to model size, dataset size and the amount of training compute.

### Major Contributions
---
Observations of significant parameters for decreasing cross entropy loss, namely model size, dataset size and computations. Establishment of power laws in relation to those parameters.

### Secondary Contribution
---

### Limitations/Future Work
---
- Since scalings are power-laws, there are diminishing returns with increasing scale.
- It is natural to conjecture that the scaling relations will apply to other generative modeling tasks with a maximum likelihood loss, and perhaps in other settings as well. To this purpose, it will be interesting to test these relations on other domains, such as images, audio, and video models, and perhaps also for random network distillation [[Idea]].
- In the domain of natural language, it will be important to investigate whether continued improvement on the loss translates into improvement on relevant language tasks [[Idea]]
- Our results strongly suggest that larger models will continue to perform better, and will also be much more sample efficient than has been previously appreciated. Big models may be more important than big data.

### Notes (Try to use backlinks)
---
- Model performance depends most strongly on scale, which consists of three factors: the number of model parameters N (excluding embed- dings), the size of the dataset D, and the amount of compute C used for training. Within reasonable limits, performance depends very weakly on other architectural hyperparameters such as depth vs. width.
- Performance has a power-law relationship with each of the three scale factors N, D, C when not bottlenecked by the other two, with trends spanning more than six orders of magnitude
- Performance improves predictably as long as we scale up N and D in tandem, but enters a regime of diminishing returns if either N or D is held fixed while the other increases.
- Every time we increase the model size 8x, we only need to increase the data by roughly 5x to avoid a penalty.
- By extrapolating the early part of a training curve, we can roughly predict the loss that would be achieved if we trained for much longer.  Could be an interesting [[Idea]] to evaluate a expected model performance before training long times. This way we could stop the training for models that are unlikely to succeed anyway.
- When we evaluate models on text with a different distribution than they were trained on, the results are strongly correlated to those on the training validation set with a roughly constant offset in the loss
- Large models are more sample-efficient than small models, reaching the same level of performance with fewer optimization steps and using fewer data points.
- When working within a fixed compute budget C but without any other restrictions on the model size N or available data D, we attain optimal performance by training very large models and stopping significantly short of convergence (see Figure 3). Maximally compute-efficient training would therefore be far more sample efficient than one might expect based on training small models to convergence, with data requirements growing very slowly as $D ∼ C^{0.27}$