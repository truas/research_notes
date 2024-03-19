### It’s Not Just Size That Matters: Small Language Models Are Also Few-Shot Learners
---
- [Zotero Select Link](zotero://select/groups/2480461/items/S3NQ8WZ3)
- [Zotero URI](https://www.zotero.org/groups/2480461/items/S3NQ8WZ3)
- Authors: [[Timo Schick]] [[Hinrich Schültze]]
- Topics: [[topic1]] [[topic2]]
- Venue: #arXiv
- Year: #2020
---
### Major Contributions
 - performance similar  to GPT-3 can be obtained with language models whose parameter count is several orders of magnitude smaller (0.1%)
 - They modify [[PET]] to predict more than one token.
 - Iterative version of [[PET]] + [[_2019_ALBERT]] (AlBERT-xxlarge-v2) outperforms [[_2020_GPT-3]] with only 0.1% of its parameters
 - 
---
### Secondary Contribution
- Propose a subset of [[SuperGLUE]] called [fewGLUE](https://github.com/timoschick/fewglue)
- Their ablation study is quite complete as it shows their modification of PET under different scenarios:
	- using [[_2019_RoBERTa]] and [[_2019_GPT-2]] instead of [[_2019_ALBERT]]
	- different seed for the fewGLUE dataset
	- comparision between 1 and 32 training examples input
	- 
---
### Limitations/Future Work
- [[PET]] only works when the answers to be predicted by the LM correspond to a single token inits vocabulary - many tasks do not work like this
- Figure 3 comparing [[_2020_GPT-3]] [[PET]] for priming with 32 examples or a single example is quite confusing
---
### Notes (Try to use backlinks)
- LM can be reformulated as cloze questions
- [[_2020_GPT-3]] uses priming:  given a few demonstrations of inputs and corresponding outputs - as context - for its predictions; but no gradient updates are performed.
	- **drawbacks 1 ** unusable in many real world scenarios
	- **drawbacks 2 ** does not scale to more than a few examples as the context window of most LM is limited to a few hundred tokens
- Alternative for priming called [[pattern-exploiting training|PET]] - it combines  reformulating tasks as cloze questions with regular gradient-based finetuning
- Their [[PET]] modification  uses masked language models (Devlin et al., 2019) to assign probabilities to sequences of text; this is similar to using them in a generative fashion (Wang and Cho, 2019)
- it is extremely difficult to ascertain which patterns perform well without trying them on a large set of examples, a key challenge for few-shot approaches is to be able to compensate for PVPs that the used LM fails to understand well.
---
