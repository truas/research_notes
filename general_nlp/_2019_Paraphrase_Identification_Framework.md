### A Qualitative Evaluation Framework for Paraphrase Identification
---
- [Zotero Select Link](zotero://select/groups/2480461/items/SFHRVYWV)
- [Zotero URI](https://www.zotero.org/groups/2480461/items/SFHRVYWV)
- Authors: [[Venelin Kovatchev]]  [[Javier Beltran]] 
- Topics: [[nlp_paraphrase]] [[nlp_evaluation]]  [[nlp_framework]] 
- Venue: #RANLP
- Year: #2019

---
### Major Contributions
- we present a new approach for the evaluation, error analysis, and interpretation of supervised and unsupervised Paraphrase Identification (PI) systems.
	- Each system performs differently with respect to a set of linguistic phenomena and makes qualitatively different kinds of errors;
	- Some linguistic phenomena are more challenging than others across all systems.
- [link](https://github.com/JavierBJ/paraphrase) (not working)
---
### Secondary Contribution
- the relative distribution of the phenomena in paraphrases and in non-paraphrases is very similar;
- there is no significant correlation (Pearson r <0.1) between the distributions of the individual phenomena.
	- These findings show that the sub-tasks are non-trivial: 
		- the binary labels of the pairs cannot be directly inferred by the presence or absence of phenomena; and 
		- the different subsets of the test set are relatively independent and the performance on them cannot be trivially reduced to overlap and phenomena co-occurrence.
---
### Limitations/Future Work
- In the unsupervised setup we first represent each of the two sentences under the corresponding model. Then we obtain a feature vector by concatenating the absolute distance and the elementwise multiplication of the two representations. The feature vector is then fed into a logistic regression classifier to predict the textual relation. This setup has been used in multiple PI papers, more recently by Aldarmaki and Diab (2018).
- Our evaluation framework is not specific to the ETPC corpus or the typology behind it. The framework can be applied to other corpora and tasks, provided they have a similar format. - but they don't. In fact there are not datasets that allow such comparison other than ETPC
---
### Notes (Try to use backlinks)
- The task of PI can be framed as a binary classification problem. The performance of the different PI systems is reported using the Accuracy and F1 score measures. However this form of evaluation does not facilitate the interpretation and error analysis of the participating systems
- We show that while the systems obtain similar quantitative results (Accuracy and F1), they perform differently with respect to a set of human interpretable linguistic categories and make qualitatively different kinds of errors.
	- The simplified corpus format poses a problem with respect to the quality of the PI task and the ways it can be evaluated. The vast majority of the state-of-the-art systems in PI provide no or very little error analysis. This makes it difficult to interpret the actual capabilities of a system and its applicability to other corpora and tasks.
- RQ 1 Does the performance of a PI system on each candidate-paraphrase pair depend on the different phenomena involved in that pair?
	- RQ 1: we show that the performance of a PI system on each candidate-paraphrase pair depends on the different phenomena involved in that pair or at least there is a strong observable relation between the performance and the phenomena.
- RQ 2 Which are the strong and weak sides of each individual system? 
	- RQ 2. The profile is humanly interpretable, and we can clearly see how the system performs on various sub-tasks at different linguistic levels. The qualitative evaluation shows that S3 performs better when it has to deal with:
- RQ 3 Are there any significant differences between the “performance profiles” of the systems? 
	- RQ 3: we show that there are significant differences between the “performance profiles” of the different systems.
	- Table 5 shows the comparison between S3 and S5 (Lan and Xu, 2018a). Ten of the phenomena show significant difference with p <0.1 and seven with p <0.05.
- RQ 4 Are there phenomena on which all systems perform well (or poorly)?
	- we show that there are phenomena which are easier or harder for the majority of the evaluated systems.
	- “We can observe that some phenomena, such as “opposite polarity substitution (habitual)”, “punctuation changes”, “spelling”, “modal verb changes”, and “coordination changes” are statistically much easier according to our evaluation, as they are consistently among the best performing phenomena across all systems.” (Facultat de Filología, Universitat de Barcelona, Spain et al., 2019, p. 574)
	- “Other phenomena, such as “negation switching”, “addition/deletion”, “same polarity substitution (named entity)”, “opposite polarity substitution (contextual)”, and “ellipsis” are statistically much harder, as they are consistently among the worst performing phenomena across all systems. With the exception of “negation switching” and “opposite polarity substitution (habitual)”, these phenomena occur in the corpus with sufficient frequency.” (Facultat de Filología, Universitat de Barcelona, Spain et al., 2019, p. 574)
- **“Phenomena performance”** is a novelty of our approach and allows for qualitative analysis and comparison
- First, the deep systems outperform the baselines. Second, the baselines that we choose are competitive and obtain high results.
	- we can identify the best performing systems: S3 (Wang et al., 2016) for the supervised and S9 (Conneau et al., 2017) for the unsupervised. BERT largely outperforms all other systems.
- S3 performs worse when facing phenomena such as “negation switching”, “ellipsis”, “opposite polarity substitution (contextual)”, and “addition/deletion”.
- We can observe that some phenomena, such as “opposite polarity substitution (habitual)”, “punctuation changes”, “spelling”, “modal verb changes”, and “coordination changes” are statistically much easier according to our evaluation, as they are consistently among the best performing phenomena across all systems.
- Our methodology has clear advantages over using simple quantitative measures (Accuracy and F1 Score): 1) It allows for a better interpretation and error analysis on the individual systems; 2) It allows for a better qualitative comparison between the different systems; and 3) It identifies phenomena which are easy/hard to solve for multiple systems and may require further research.
---
