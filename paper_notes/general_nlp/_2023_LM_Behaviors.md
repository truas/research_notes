### Discovering Language Model Behaviors with Model-Written Evaluations
---
- [Zotero Select Link](zotero://select/groups/2480461/items/TWS84UPU)
- [Zotero URI](https://www.zotero.org/groups/2480461/items/TWS84UPU)
- Authors: [[Ethan Perez]] [[Christopher Olah]] [[Jared Kaplan]] 
- Topics: [[nlp_evaluation1]] [[nlp_LLM]]
- Venue: #arxiv  #ACL  #anthropic
- Year: #2023

---
### Major Contributions
- We explore approaches with varying amounts of human effort, from instructing LMs to write yes/no questions to making complex Winogender schemas with multiple stages of LM-based generation and filtering
	- we show it is possible to generate many diverse evaluations with significantly less human effort by using LMs
	- We generate 154 datasets and discover new cases of inverse scaling where LMs get worse with size
- [dataset showcase](https://www.evals.anthropic.com/model-written/)
- [github](https://github.com/anthropics/evals)
---
### Secondary Contribution
- We also find some of the first examples of inverse scaling in RL from Human Feedback (RLHF), where more RLHF makes LMs worse
- 
---
### Limitations/Future Work
- 
---
### Notes (Try to use backlinks)
- Prior work creates evaluation datasets manually (Bowman et al., 2015; Rajpurkar et al., 2016, inter alia), which is time-consuming and effortful, limiting the number and diversity of behaviors tested. Other work uses existing data sources to form datasets (Lai et al., 2017, inter alia), but such sources are not always available, especially for novel behaviors.
- Our results indicate that LMs are not a silver bullet for creating arbitrary evaluations but rather that LMs should be strongly considered before embarking on manual data creation.
- We release all 154 model-written evaluations at evals.anthropic.com/model-written, including one of the earliest and largest set of evaluations for advanced AI risks. We also release Winogenerated, a human-validated, 50x larger version of the Winogender gender bias evaluation. We expect these datasets, among others, to be of significant independent interest.
- Using LM-written evaluations, we discover several new cases of “inverse scaling” (Lin et al., 2021; McKenzie et al., 2022) where larger LMs are worse than smaller ones.
- “We test various aspects of models’ personas: personality (26 datasets), stated desire to pursue potentially dangerous goals (46 datasets) or other unsafe behaviors (26 datasets), and stated views on religion (8), politics (6), ethics (17), and other topics (4).” (Perez et al., 2023, p. 13389)
- We ask models if they agree/disagree with the statements, evaluating the fraction of the time their agreement/disagreement
- Evaluated Models We aim to investigate the extent to which model behaviors are influenced by scaling model size and by RLHF. To this end, we evaluate LMs with varying numbers of parameters (810M, 1.6B, 3.5B, 6.4B, 13B, 22B, 52B parameters, trained as in Kadavath et al., 2022) and with varying numbers of RLHF training steps (0, 50, 100, 250, 500, and 1000 steps) from the same RL training run.
- “Quantitative Analysis To study data quality more rigorously, we have crowdworkers (hired via SurgeAI) evaluate the data. Workers evaluated whether examples from each of our 133 datasets are (1) relevant to the behavior tested, (2) correctly labeled, and (3) unambiguous in what the correct label should be.” (Perez et al., 2023, p. 13391)
- Our results reveal instances of inverse scaling with RLHF training, where more RLHF made a pretrained LM behave more questionably.
- RLHF pushes model outputs strongly away from nihilism and towards various ethical theories (especially virtue ethics, but also deontology and utilitarianism).
- Fig. 2 shows the results. Increasing model size increases models’ tendency to repeat back a user’s view, for questions on politics, NLP, and philosophy.
- “Evaluation Winogender evaluates gender bias by replacing the pronoun options with a blank and having a model predict the missing pronoun, revealing a model’s associations between certain occupations and genders (e.g. “nurse” and “her” or “dentist” and “him”).” (Perez et al., 2023, p. 13394)
	- Fig. 3 shows the scatter plot results for a 52B pretrained LM. Winogenerated data gives results that are in line with those of the hand-crafted Winogender data, but with tighter confidence intervals
---
