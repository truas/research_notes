### Quantifying Memorization Across Neural Language Models
---
- [Zotero Select Link](zotero://select/groups/2480461/items/YZV6P44Q)
- [Zotero URI](https://www.zotero.org/groups/2480461/items/YZV6P44Q)
- Authors: [[Nicholas Carlini]] [[(optional) relevant author]] [[last author]] 
- Topics: [[nlp_lm]] [[nlp_ann]]
- Venue: #arXiv #google
- Year: #2022
---
### Major Contributions
- We describe three log-linear relationships that quantify the degree to which LMs emit memorized training data. Memorization significantly grows as we increase (1) the capacity of a model, (2) the number of times an example has been duplicated, and (3) the number of tokens of context used to prompt the model.
- We identify three properties that significantly impact memorization:
	-  1. Model scale: Within a model family, larger models memorize 2-5× more data than smaller models. 
	-  2. Data duplication: Examples repeated more often are more likely to be extractable. 
	-  3. Context: It is orders of magnitude easier to extract sequences when given a longer surrounding context.
---
### Secondary Contribution
- we are able to show that the 6 billion parameter GPT-J model (Black et al., 2021; Wang and Komatsuzaki, 2021) memorized at least 1% of its training dataset: The Pile (Gao et al. (2020)).
---
### Limitations/Future Work
---
### Notes (Try to use backlinks)
- We find that larger models memorize significantly more than smaller models do
- A qualitative analysis (see examples in Appendix Figure 13) suggests that examples “memorized” by GPT-2 are largely uninteresting sequences (e.g., number sequences, repetitions of the same few tokens, or common phrases). Therefore, we conclude that when larger models have a higher fraction of extractable training data, it is because they have memorized the data; it is not simply because the larger models are generally more accurate
- we find that memorization does still happen, even with just a few duplicates—thus, deduplication will not perfectly prevent leakage. While this relationship is perhaps obvious, and has been corroborated for specific training examples in prior work (Carlini et al., 2019, 2020), our results show that it holds across the entire training set.
	- They also tried random sampling and the results were not good. The approach of sampling based on data duplication shows more interesting findings
- **discoverability phenomenon:** some memorization only becomes apparent under certain conditions, such as when the model is prompted with a sufficiently long context.
	- 33% of training sequences are extractable from the 6B model at 50 tokens of context, compared to 65% with 450 tokens of context
- They reproduced their experiments and methodology for other models, such as T5
	- Their findings still hold  - to some extent
		- while sequences that have been duplicated more often are easier to memorize, there is not an obvious log-linear scaling relationship to be found
		- for some reason, sequences that occur ∼140 times are more likely to be memorized, despite occurring less often, even if we assume a three-sigma error in both measurements simultaneously
- generalization, we have shown that while current LMs do accurately model the distribution of their training data, this does not necessarily imply they will model the desired underlying data distribution.
- privacy, our work indicates that current large language models likely memorize a significant fraction of their training datasets. Memorization scales log-linear with model size—by doubling the number of parameters in a model we can extract a significantly larger fraction of the dataset.
---
