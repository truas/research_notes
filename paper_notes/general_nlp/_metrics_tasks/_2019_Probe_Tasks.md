### What do you learn from context? Probing for sentence structure in contextualized word representations
---
- [Zotero Select Link](zotero://select/groups/2480461/items/CDHDJG99)
- [Zotero URI](https://www.zotero.org/groups/2480461/items/CDHDJG99)
- Authors: [[Ian Tenney]] [[Ellie Pavlick]]
- Topics: [[nlp_task]] [[nlp_metrics]]
- Venue: #ICLR
- Year: #2019
---
### Major Contributions
- What do contextual representations encode that conventional word embeddings
do not? - they evaluate each layer in the architecture in several tasks to asnwer this
- They propose edge probing tasks covering a wide range of syntactic, semantic, local, and long-range phenomena.
	- In particular, what information is encoded at each position and how well it encodes structural information about that word's role  in the sentence
---
### Secondary Contribution
---
### Limitations/Future Work
---
### Notes (Try to use backlinks)
- ![[2019_Probe_model.png]]
- They test their edge probing with [[_2019_BERT]] [[_2019_ELMo]] [[_2018_GPT]] [[_2017_CoVe]]
- During the probe tasks all weights are freezed
- Focus on eight core NLP labeling tasks: part-of-speech, constituents, dependencies, named entities, semantic roles, coreference, semantic proto-roles, and relation classification. 
	- The tasks and their respective datasets are described below, and also detailed in Table 1 and Appendix B.
- contextualized embeddings improve over their non-contextualized counterparts largely on syntactic tasks (e.g. constituent labeling) in comparison to semantic tasks (e.g. coreference), suggesting that these embeddings encode syntax more so than higher-level semantics
- performance of  [[_2019_ELMo]]cannot be fully explained by a model with access to local context, suggesting that the contextualized representations do encode distant linguistic information, which can help disambiguate longer-range dependency relations and higher-level syntactic structures.
---
