### KagNet: Knowledge-Aware Graph Networks for Commonsense Reasoning
---
- [Zotero Select Link](zotero://select/groups/2480461/items/AIAFD5AK)
- [Zotero URI](https://www.zotero.org/groups/2480461/items/AIAFD5AK)
- Authors: [[Bill Yuchen Lin]] [[Xiang Ren]]
- Topics: [[nlp_lexical_databes]] [[nlp_knowlegde_representation]]
- Venue: #EMNLP #IJCNLP
- Year: #2019
---
### Major Contributions
- This paper aims to tackle the research question of how we can teach machines to make such commonsense inferences, particularly in the question-answering setting.
- [[KagNet]] is a combination of graph convolutional networks (Kipf and Welling, 2017) and LSTMs, with a hierarchical path-based attention mechanism, which forms a GCN-LSTM-HPA architecture for path-based relational graph representation
	- 
---
### Secondary Contribution
- Recently, there have been a few emerging large-scale datasets for testing machine
commonsense with various focuses (Zellers et al., 2018; Sap et al., 2019b; Zellers et al., 2019), (Talmor CommonsenseQA et al., 2019)
---
### Limitations/Future Work
---
### Notes (Try to use backlinks)
- Reasoning is the process of combining facts and beliefs to make new decisions (Johnson-Laird, 1980), as well as the ability to manipulate knowledge to draw inferences (Hudson and Manning, 2018).
- The grounding stage is three-fold: recognizing concepts mentioned in text, constructing schema graphs by retrieving paths in the knowledge graph, and pruning noisy paths 
- [[KagNet]] is a graph neural network module with the architecture that models GCN-LSTM-HPA relational graphs for relational reasoning under the context of both knowledge symbolic space and language semantic space
- The CSQA-BL achieves an accuracy of 51.23% while our model CSQA-KN scores. These 53.51% two comparisons further support our assumption that KAGNET, as a knowledge-centric model, is more extensible in commonsense reasoning
---
