### BARTSCORE: Evaluating Generated Text as Text Generation
---
- [Zotero Select Link](zotero://select/groups/2480461/items/BS8AM3D4)
- [Zotero URI](https://www.zotero.org/groups/2480461/items/BS8AM3D4)
- Authors: [[Welzhe Yuan]] [[Pengfei Liu]] 
- Topics: [[nlp_text_summarization]] [[nlp_metrics]]
- Venue: #arXiv 
- Year: #2021
---
### Major Contributions
- One major challenge for these applications is how to evaluate whether such generated texts are actually fluent, accurate, or effective
- In this paper, we instead argue for a formulation of evaluation of generated text as a text generation problem, directly evaluating text through the lens of its probability of being generated from or generating other textual inputs and outputs.
- [[_2021_BARTScore]]
	- parameter and data efficient, architecturally there are no extra parameters beyond those used in pre-training itself. 
	- It can better support evaluation of generated text from different perspectives (e.g., informativeness, coherence, factuality,  by adjusting the inputs and outputs of the conditional text generation problem, 
	- It can be further enhanced by (i) providing textual prompts that bring the evaluation task closer to the pre-training task, or (ii) updating the underlying model by fine-tuning BART based on downstream generation tasks (e.g., text summarization).
---
### Secondary Contribution
- Code to calculate [[_2021_BARTScore]] is available at [link](https://github.com/neulab/BARTScore), and we have released an interactive leaderboard for (meta-evaluation)[ at http://explainaboard.nlpedia.ai/leaderboard/task-meval/] on the EXPLAINABOARD platform [32], which allows us to interactively understand the strengths, weaknesses, and complementarity of each metric.
- 
---
### Limitations/Future Work
- We also report preliminary experiments comparing BART with T5 [46] and PEGASUS [62] in the Appendix.
---
### Notes (Try to use backlinks)
- There is a decided disconnect between how models are pre-trained using text generation objectives and how they are used as down-stream feature extractors.
- The most general form of our proposed BARTSCORE is shown in Eq. 2, where we use the weighted log probability of one text Y given another text X. The weights are used to put different emphasis on  different tokens, which can be instantiated using different methods like Inverse Document Frequency  (IDF) [20] etc
	- Faithfulness
	- Precision
	- Recall
	- F-Score
	- searching for proper prompts to better leverage knowledge stored in pre-trained language models instead of training on human judgment data [26].
---
