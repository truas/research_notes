### Language Modeling Makes Sense: Propagating Representations through WordNet for Full-Coverage Word Sense Disambiguation
---
- [Zotero Select Link](zotero://select/groups/2480461/items/CDU5DH3J)
- [Zotero URI](https://www.zotero.org/groups/2480461/items/CDU5DH3J)
- Authors: [[Daniel Loureiro]] [[Alipio Mario Jorge]]
- Topics: [[nlp_lm]] [[nlp_wsd]]
- Venue: #ACL 
- Year: #2019
---
### Major Contributions
- Create sense-level embeddings with full coverage of WordNet 
- Combine K-NN  with [[Most Frenquent Sense|MFS]] using [[_2019_BERT]] embeddgins to generate a full-coverage of WordNet
---
### Secondary Contribution
---
### Limitations/Future Work
- No clear why they use [[_2019_ELMo]] and [[_2019_BERT]] embeddings from specific layers, top-2 and sum of top-4 respectively.
---
### Notes (Try to use backlinks)
- a synset embedding corresponds to the average of its sense embeddings - the same for hypernyms, lexname, etc
- glosses embeddings are generated from averaging its constituent word embeddings  - not sure what it is considered for the weight though
- This paper introduces a method for generating sense embeddings that allows a clear improvement of the current state-of-the-art on cross-domain WSD tasks. 
- We leverage contextual embeddings, semantic networks and glosses to achieve full
coverage of all WordNet senses
- Consequently,we’re able to perform WSD with a simple 1-NN, without recourse to MFS fallbacks or task-specific modelling.
---
