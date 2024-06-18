### # Lessons from the Trenches on Reproducible Evaluation of Language Models
---
- [Zotero Select Link](https://www.zotero.org/groups/2480461/items/BWC95W3N)
- [Zotero URI](https://www.zotero.org/groups/2480461/items/BWC95W3N)
- Authors: [[Stella Biderman]] [[Hailey Schoelkopf]] [[Lintang Sutawika]] [[Andy Zou]] 
- Topics: [[nlp_evaluation]] [[nlp_lm]]
- Venue: #arxiv
- Year: #2024

---
### Major Contributions
- “Researchers and engineers face methodological issues such as the sensitivity of models to evaluation setup, difficulty of proper comparisons across methods, and the lack of reproducibility and transparency” (Biderman et al., 2024, p. 1)
	- “First, we provide an overview of common challenges faced in language model evaluation. Second, we delineate best practices for addressing or lessening the impact of these challenges on research. Third, we present the Language Model Evaluation Harness (lm-eval): an open source library for independent, reproducible, and extensible evaluation of language models that seeks to address these issues.” (Biderman et al., 2024, p. 1)
---
### Secondary Contribution
- “the [[PromptSource]] (Bach et al., 2022) library was added to a fork of lm-eval to enable easy evaluation across many different prompt templates7 for the first time. Most papers that came out of the BigScience Workshop used this functionality to report distributions of scores across different prompting set-ups (Sanh et al., 2022; Muennighoff et al., 2022; Yong et al., 2023; Workshop et al., 2023). PromptSource, along with other innovations introduced in the BigScience fork, is now supported natively in lm-eval” (Biderman et al., 2024, p. 9)
	- “While the approach used by BigScience in reporting distributions across prompts has not been widely adopted, the idea that prompts should be considered as part of the evaluation set-up has become widely accepted. We hope that future research will especially continue to focus on collecting realistic prompts (Shen et al., 2023b; Xie et al., 2023; Hofmann et al., 2024) or measuring the extent to which results with particular common set-ups generalize to more realistic use-cases (Lyu et al., 2024), or otherwise investigate prompting as a humancomputer interaction problem.” (Biderman et al., 2024, p. 9)
---
### Limitations/Future Work
- 
---
### Notes (Try to use backlinks)
- “Evaluation practices thus play a crucial role in the direction of the field: inconsistencies or biases in evaluation practices can lead to skewed performance comparisons, which may influence the direction of future research and the adoption of new methods by the community (Dehghani et al., 2021) or lead to adverse effects from deploying suboptimal or harmful models (Bender & Friedman, 2018) on tasks for which they are ill-suited (Raji et al., 2022).” (Biderman et al., 2024, p. 1)
- “**the Key Problem:** When evaluating language models, there can be many semantically equivalent but syntactically different ways of expressing the same idea” (Biderman et al., 2024, p. 2)
	- “this would be solvable by simply having expert human annotators score model responses for correctness” (Biderman et al., 2024, p. 2)
- “lm-eval is designed to ensure measurements are consistent across runs and models, regardless of (construct) validity. This is due to our goal of building research infrastructure for evaluations.” (Biderman et al., 2024, p. 3)
- ““**Minor**” Implementation Details Matter The importance of interoperability and full reproducibility stems from the fact that language models are incredibly sensitive to precise details that may not be obvious to practitioners.” (Biderman et al., 2024, p. 3)
- “Many LMs developed by industrial labs, often used as reference points for benchmarks, have never been released externally (Chowdhery et al., 2023; Hoffmann et al., 2022), preventing comparisons except by pulling unverified evaluation numbers from technical reports. Those models that have been made available via APIs may non-transparently not match the published versions or otherwise be modified for deployment.” (Biderman et al., 2024, p. 4)
- **Best Practices for Language Model Evaluation**
	- “Always share your exact prompts and code” (Biderman et al., 2024, p. 5)
	- “Prompts should not be optimized for performance on a given model but not others, and the amount of prompt engineering done should be disclosed.” (Biderman et al., 2024, p. 5
	- “Avoid copying results from other implementations” (Biderman et al., 2024, p. 5)
	-  “Always provide model outputs • Providing model outputs alongside evaluation code can allow others to recalculate scores based on these artifacts, which can be useful for performing statistical significance testing and for assessing the impact of different evaluation metrics or scoring approaches” (Biderman et al., 2024, p. 6)
	- “Perform qualitative analyses • Qualitatively **review a small batch of results and outputs before testing at scale**: it is very easy to have bugs in your generation code, especially when working with multiple sets of benchmarks, prompts, and models of different architectures.” (Biderman et al., 2024, p. 6)
	- “Measure and Report Uncertainty • Most works on language modeling do not perform statistical significance testing, which can significantly decrease confidence in results (Marie et al., 2021).” (Biderman et al., 2024, p. 6)
	- “Although costly, reporting results run over more than one random seed can dramatically boost the validity and utility of results.” (Biderman et al., 2024, p. 6)
- “the Evaluation Harness does not seek to solely prescribe what the correct benchmark or evaluation protocols to use are, and allows users to select their desired tasks and use cases” (Biderman et al., 2024, p. 6)
- “Comparing these prompting styles, the degree to which models differ in performance widely varies, as well as which prompt performs better. If certain model creators chose one prompting and scoring style and certain other model creators chose the other, and each used the cited numbers from the respective technical reports for comparing their model to other baselines, the comparisons would be nonsensical and not provide information on which model were “truly” performant.” (Biderman et al., 2024, p. 11)

	---	
