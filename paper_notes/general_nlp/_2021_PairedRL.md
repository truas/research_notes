### Paired Representation Learning for Event and Entity Coreference
---
- [Zotero Select Link](zotero://select/groups/2480461/items/MRGP8ACN)
- [Zotero URI](https://www.zotero.org/groups/2480461/items/MRGP8ACN)
- Authors: [[Xiaodong Yu]] [[Dan Roth]] 
- Topics: [[nlp_coref]] [[nlp_2cdcr]]
- Venue: #arXiv
- Year: #2021
---
### Major Contributions
- we propose paired representation learning (PAIREDRL) for coreference resolution. Given a pair of elements (Events or Entities) our model treats the pair’s sentences as a single sequence so that each element in the pair learns its representation by encoding its own context as well the other element’s context.
---
### Secondary Contribution
---
### Limitations/Future Work
---
### Notes (Try to use backlinks)
- we will concatenate the two sentences (with a mention in each) as a whole sequence and forward it into a ROBERTa (Liu et al., 2019) system. RoBERTa takes the ''whole sequence'' as an input so that each token, including the mention spans, in the two sentences are able to compare with other tokens from the very beginning
- Coreference model based on the intuition that if two mention triggers are referring to the same event, their arguments very likely refer to the same, and vice versa.
- PAIREDRL learns a mention-pair representation by forwarding concate nated sentences into RoBERTa, where sentences provide the context of mentions. This algorithm is applied to both event and entity coreference bench marks and obtains state of the art performance.
- ![[2021_PairedRL_arch.png]]
- ![[2021_PairedRL_reasoning.png]]
---
