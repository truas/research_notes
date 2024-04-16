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
- **Takeaway**
	- The main takeaway is for a fixed task and a fixed model family, the researcher can choose a metric to create an emergent ability or choose a metric to ablate an emergent ability. Ergo, emergent abilities may be creations of the researcher’s choices, not a fundamental property of the model family on the specific task. That said, we emphasize that nothing in this paper should be interpreted as claiming that large language models cannot display emergent abilities; rather, our message is that previously claimed emergent abilities in [3, 8, 29, 34] might likely be a mirage induced by researcher analyses.
---
### Secondary Contribution
- Srivastava et al. [29] observed that while accuracy at a particular task can empirically appear sharp and unpredictable, the cross entropy does not; the authors then hypothesized that emergent abilities may be partially attributed to the metric, writing: “[Emergent abilities frequently appear] on tasks that have brittle or narrow metrics for success, emphasizing the importance of engineering graded metrics that can capture subthreshold improvements
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
- **Prediction: Emergent Abilities Disappear Under Linear Metrics:** if one changes the metric from nonlinear to linear while keeping the models’ outputs fixed, the family’s performance smoothly, continuously and predictably improves (Fig. 3, bottom row). This confirms our first prediction, thereby demonstrating that the source of the sharpness and unpredictability is the researcher’s choice of metric, not changes in the model family’s outputs.
- **Prediction: Emergence Disappears With Higher Resolution Evaluations:** that even on nonlinear metrics such as accuracy, smaller models do not have zero accuracy, but rather have non-zero above-chance accuracy commensurate with choosing to use accuracy as the metric. To increase the resolution so as to be able to accurately estimate the models’ accuracy, we generated additional test data, and found that on both integer multiplication and integer addition tasks, all models in the InstructGPT/GPT-3 family achieve positive above-chance accuracy (Fig. 4).
- **Prediction: Emergent Abilities Should Predominantly Appear on Nonlinear & Discontinuous Metrics**: We found that most metrics used in BIG-Bench have zero task-model family pairs that exhibit emergent abilities: of the 39 preferred metrics in BIG-Bench, at most 5 display emergence (Fig. 5A). 
- **Prediction: Replacing Nonlinear & Discontinuous Metric Should Remove Emergent Abilities:** Top: The LaMDA model family displays emergent abilities when measured under a discontinuous metric (Multiple Choice Grade). Bottom: The LaMDA model family no longer displays emergent abilities on the same tasks when measured under a continuous BIG-Bench metric (Brier Score).
---
