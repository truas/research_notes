### COMET: Commonsense Transformers  for Automatic Knowledge Graph Construction
---
- [Zotero Select Link](zotero://select/groups/2480461/items/8TKQMQYW)
- [Zotero URI](https://www.zotero.org/groups/2480461/items/8TKQMQYW)
- Authors: [[Antonie Bosselut]] [[Yejin Choi]] 
- Topics: [[nlp_transformers]] [[nlp_knowlegde_representation]] [[nlp_commonsense]]
- Venue: #ACL 
- Year: #2019
---
### Major Contributions
- We present the first comprehensive study on automatic knowledge base construction or two prevalent commonsense knowledge graphs: ATOMIC (Sap et al., 2019) and ConceptNet  Speer et al., 2017).
- In this work, we define the COMmonsEnse Transformer (COMET), which constructs commonsense KBs by using existing tuples as a seed set of knowledge on which to train. Using this seed set, a pre-trained language model learns to adapt its learned representations to knowledge generation, and produces novel tuples that are high quality.
---
### Secondary Contribution
- Demo is available at [link](https://mosaickg.apps.allenai.org/)
- Code is available at [link](https://github.com/atcbosselut/comet-commonsense)
---
### Limitations/Future Work
---
### Notes (Try to use backlinks)
- Automatic KB construction is a long-standing goal of artificial intelligence research due to the difficulty of achieving high concept coverage in high-precision curated KBs (Lenat, 1995; Miller,1995).
- the problem assumes COMET is given a training knowledge base of natural language tuples in {s,r,o} format, where **s** is the phrase subject of the tuple, **r** is the relation of the tuple, and **o** is the phrase object of the tuple.
- we use the transformer language model architecture in troduced in Radford et al. (2018) (GPT)
- COMET is trained to learn to produce the phrase object **o** of a knowledge tuple given the tuple’s phrase subject **s*** and relation **r**.
- COMET relies on a seed set of knowledge tuples from an existing KB to learn to produce commonsense knowledge. In this work, we use ATOMIC and ConceptNet as knowledge seed sets, but other commonsense knowledge resources could have been used as well as COMET is domain-agnostic.
- Initialized via [[_2018_GPT]]
- Details and hyperparameters are described in A1
- we evaluate our method using BLEU-2 as an automatic evaluation metric. We also report the perplexity of the model on its gold generations.
- 
- ![[2019_COMET_arch.png]]
- ![[2019_COMET_example.png]]
- 
---
