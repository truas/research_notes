## NL-Augmenter: A Framework for Task-Sensitive Natural Language Augmentation
---
- [Zotero Select Link](zotero://select/groups/2480461/items/QPEV9XUA)
- [Zotero URI](https://www.zotero.org/groups/2480461/items/QPEV9XUA)
- Authors: [[Kaustubh D. Dhole]] [[Yue Zhang]] 
- Topics: [[nlp_tasks]] [[nlp_tool]]
- Venue: #arxiv
- Year: #2022

---
### Major Contributions
- We describe the framework and an initial set of 117 transformations and 23 filters for a variety of natural language tasks. We demonstrate the efficacy of NL-Augmenter by using several of its transformations to analyze the robustness of popular natural language models
- [GitHub](https://github.com/GEM-benchmark/NL-Augmenter)
- Table 1 and 2 list all 117 transformations
---
### Secondary Contribution
- 92 institutions participated in this project
- the overall results show that the tested perturbations do pose a challenge to different models on different tasks, with quasi systematic score drops.
---
### Limitations/Future Work
- with so many transformations applied to four different datasets, the presented robustness analysis can only be shallow, and a separate analysis of each transformation would be needed in order to get more informative insights.
	- our superficial analysis above relies on tags which were in many cases annotated by hand, and some of the suprising results (e.g. meaning-preserving transformations are more challenging than non-meaning-preserving ones) may reflect a lack of consistency in the annotations.
---
### Notes (Try to use backlinks)
- **Data augmentation**, the act of creating new datapoints by slightly modifying copies or creating synthetic data based on existing data, is an important component in the robustness evaluation of models in natural language processing (NLP) and in enhancing the diversity of their training data
- The Generation Evaluation and Metrics benchmark (Gehrmann et al., 2021), which started the development of NL-Augmenter, is a participatory project to document and improve tasks and their evaluation in natural language generation.
- three types of evaluation sets were proposed: (i) transformations, i.e. original test sets are perturbed in different ways (e.g. backtranslation, introduction of typographical errors, etc.), (ii) subpopulations, i.e. test subsets filtered according to features such as input complexity, input size, etc.; and (iii) data shifts, i.e. new test sets that do not contain any of the original test set material
	- we present a participant-driven repository for creating and testing transformations and filters, and for applying them to all dataset splits (training, development, evaluation) and to all NLP tasks (NLG, labeling, question answering, etc.).
- **Linguistic level (Table 8):** Transformations making character level and morphological changes were able to show drastic levels of drops in performance compared to those making lexical or syntactic changes.
- **Meaning preservation (Table 10):** 22 transformations which were marked as highly meaning preserving surprisingly showed a larger average performance drop as compared to 20 of those which were marked as possibly meaning changing.
- 
- ![[2022_NL_Augmenter_example.png]]
---
