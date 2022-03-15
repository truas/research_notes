### Neural Text Summarization: A Critical Evaluation
---
- [Zotero Select Link](zotero://select/groups/2480461/items/VNP7P2IY)
- [Zotero URI](https://www.zotero.org/groups/2480461/items/VNP7P2IY)
- Authors: [[Wojciech Kryscinski]] [[Richard Socher]] 
- Topics: [[nlp_text_summarization]] [[nlp_task]]
- Venue: #ACL
- Year: #2019
---
### Major Contributions
- It analyzes neural text summarization focusing on three problems in current publications
	- 1) automatically collected datasets leave the task underconstrained and may contain noise detrimental to training and evaluation
	- 2) current evaluation protocol is weakly correlated with human judgment and does not account for important characteristics such as factual correctness
	- 3) models overfit to layout biases of current datasets and offer limited diversityin their outputs.
---
### Secondary Contribution
---
### Limitations/Future Work
- assessing the importance of information is a difficult task in itself, that highly depends on the expectations and prior knowledge of the target reader.
---
### Notes (Try to use backlinks)
- Model fall into three categories: abstractive, extractive, and hybrid
- A common approach in abstractive summarization is to use attention and copying mechanisms (See et al., 2017; Tan et al., 2017; Cohan et al., 2018).
- Hybrid: select and paraphrase/generate text
- Liu and Liu (2010) examine the correlation between ROUGE scores and human judgments when evaluating meeting summarization data and show that the correlation strength is low, but can be improved by leveraging unique meeting characteristics, such as available speaker information.
- Schulman et al. (2015) study the problems related to using ROUGE as an evaluation metric with respect to finding optimal solutions and provide proof of NP-hardness of global optimization with respect to ROUGE.
- given a document with one associated reference summary and no additional information, leaves the task of summarization under constrained and thus too ambiguous to be solved by end-to-end models
- News articles adhere to a writing structure known in journalism as the ”Inverted Pyramid” (PurdueOWL, 2019). In this form, initial paragraphs contain the most newsworthy information, which is followed by details and backgroundinformation.
- In terms of Pearsons’s coefficients, the study showed minimal correlation with any of the annotated dimensions for both abstractive and extractive models together and for abstractive models individually. Weak correlation was discovered for extractive models primarily with the fluency and coherence dimensions.
- Neither of the methods explicitly examines the factual consistency of summaries, leaving this important dimension unchecked
- We notice that the ROUGE-1 scores vary considerably less than ROUGE-4 scores. This suggests that the models share a large part of the vocabulary on the token level, but differ on how they organize the tokens into longer phrases.
- current state-of-the-art methods learn to rely too heavily on layout bias associated with the particular domain of the text being summarized, and the current evaluation protocol reflect human judgments only weakly while also failing to evaluate critical features (e.g. factual correctness) of text summarization
---
