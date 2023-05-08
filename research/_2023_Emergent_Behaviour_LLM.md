### Are Emergent Abilities of Large Language Models a Mirage?
---
- [Zotero Select Link](zotero://select/groups/2480461/items/XCHLT8WF)
- [Zotero URI](https://www.zotero.org/groups/2480461/items/XCHLT8WF)
- Authors: [[Rylan Schaeffer]]  [[Sanmi Koyejo]] 
- Topics: [[nlp_LLM]] [[nlp_explain]] [[nlp_train]]
- Venue: #arxiv
- Year: #2023

---
### Major Contributions
- They claim "emergent behaviour" of LLM are not fundamentally a result from the model itself, but the analysis carried out by researchers
- we (1) make, test and confirm three predictions on the effect of metric choice using the InstructGPT/GPT-3 family on tasks with claimed emergent abilities, (2) make, test and confirm two predictions about metric choices in a meta-analysis of emergent abilities on BIG-Bench; and (3) show how similar metric decisions suggest apparent emergent abilities on vision tasks in diverse deep network architectures (convolutional, autoencoder, transformers).
- our alternative explanation posits that emergent abilities **are a mirage** caused primarily by the researcher choosing a metric that nonlinearly or discontinuously deforms per-token error rates, and partially by possessing too few test data to accurately estimate the performance of smaller models (thereby causing smaller models to appear wholly unable to perform the task) and partially by evaluating too few large-scale models.
---
### Secondary Contribution
- 
---
### Limitations/Future Work
- 
---
### Notes (Try to use backlinks)
- emergent abilities intriguing is two-fold: their sharpness, transitioning seemingly instantaneously from not present to present, and their unpredictability, appearing at seemingly unforeseeable model scales
	- we present an alternative explanation for emergent abilities: that for a particular task and model family, when analyzing fixed model outputs, one can choose a metric which leads to the inference of an emergent ability or another metric which does not. Thus, our alternative suggests that **existing claims of emergent abilities are creations of the researcher’s analyses, not fundamental changes in model behavior on specific tasks with scale**
- The term “emergent abilities of LLMs” was recently and crisply defined as “abilities that are not present in smaller-scale models but are present in large-scale models; thus they cannot be predicted by simply extrapolating the performance improvements on smaller-scale models” [34]
- Two properties in LLM wrt to emergent abilities/behaviour:
	- Sharpness, transitioning seemingly instantaneously from not present to present.
	- Unpredictability, transitioning at seemingly unforeseeable model scales
- For instance, as we later show, > 92% of emergent abilities on BIG-Bench tasks [29] (hand-annotated by [33]) appear under one of two metrics: 
	- Multiple Choice Grade def = {1 if highest probability mass on correct option 0 otherwise
	- Exact String Match def = {1 if output string exactly matches target string 0 otherwise
- We then test our alternative explanation in three complementary ways: 
	1. We make, test and confirm three predictions based on our alternative hypotheses using the InstructGPT [24] / GPT-3 [3] model family. 
	2. We meta-analyze published results from [8, 29, 34], and show that in the space of taskmetric-model family triplets, emergent abilities only appear for certain metrics and not for model families on tasks (columns). We further show that on fixed model outputs, changing the metric causes the emergence phenomenon to disappear. 
	3. We intentionally induce emergent abilities in deep neural networks of different architectures on multiple vision tasks (which to the best of our knowledge have never before been demonstrated) to show how similar metric choices can induce seemingly emergent abilities.
![[2023_Emergent_Bhaviour_LLM_results_metrics.png]]

---
