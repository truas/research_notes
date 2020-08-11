### ERNIE: Enhanced Language Representation with Informative Entities
---
- [Zotero Select Link](zotero://select/groups/2480461/items/TTUS85BM)
- [Zotero URI](https://www.zotero.org/groups/2480461/items/TTUS85BM)
- Authors: [[Zhengyan Zhang]] [[Qun Liu]]
- Topics: [[KG]] [[nlp_transformers]] [[nlp_lm]]
- Venue: #ACL 
- Year: #2019
---
### Major Contributions
- Incorporate [[KG|knowledge graphs]] can provide rich structured knowledge for [[NLU|Natural Language Understanding]]
- They recognize named entity mentions in text and align these mentions to their corresponding entities in KG to extract and encode knowlegde information
	- [[_2019_ERNIE]] integrates entity representations in the knowledge module into the underlying layers of the semantic module
- They also use [[NSP]] and [[MLM]] from [[_2019_BERT]]
	- Thye have an extra pre-training obective that randomly masks some named entity alignments in the input text and ask the model to select appropriate entities from the [[KG]] to complete the alignments
- 
---
### Secondary Contribution
---
### Limitations/Future Work
- incorporate knowledge into feature-based pre-training models such as ELMo
- introduce diverse knowledge graph information, such as ConceptNet
- annotate more real-world corpora heuristically for building larger pre-training data
- Not very clear how exactly the knowledge from the external source is incoporated #TODO 
---
### Notes (Try to use backlinks)
- Ways to incorporate external knowledge into language  representation models:
	- Structured Knowledge Encoding: extract and encode informative facts in KGs for language representation models
	- Heterogeneous Information Fusion:  language representation and knowledge representation are different, so they are hard to combine
- ![[2019_ERNIE_architecture.png]]
- [[_2019_ERNIE]] architecture has two modules:
	- underlying textual encoder (T-Encoder): captures basic lexical and syntactic information from the input tokens
	- upper knowledgeable encoder (K-Encoder): integrate extra token-oriented knowledge information into textual information from the underlying layer (represent heterogenous information from tokens and entities in a unique feature space)
	- Use GELU activation function
---
