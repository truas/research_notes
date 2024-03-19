### Jurassic-1: Technical Details and Evaluation
---
- [Zotero Select Link](zotero://select/groups/2480461/items/FPXZ45Z4)
- [Zotero URI](https://www.zotero.org/groups/2480461/items/FPXZ45Z4)
- Authors: [[Opher Lieber]] [[Yoav Shoham]] 
- Topics: [[nlp_text_generation]] [[nlp_ann]] [[nlp_arch]]
- Venue: #none #whitepaper
- Year: #2021
---
### Major Contributions
- [[_2021_Jurassic-1]] is a set of baseline models, inspired by OpenAI’s pioneering work on GPT-3 (Brown et al., 2020). Similar to [[GPT-3]], Jurassic-1 consists of auto-regressive models trained on a mix of English corpora that scales up to 178B parameters.
- Their main contribution lies on the archutecture tweak which allows for more data to be processed more efficiently.
	- They use the sentence piece tokenizer from [[_2019_T5]] and multiword expressions in their vocabulary (e.g., _ice_cream, _Higgs_boson)
	- Some cleve hyperparameterization also helped.
---
### Secondary Contribution
---
### Limitations/Future Work
---
### Notes (Try to use backlinks)
- We based our models on the decoder module of the Transformer architecture (Vaswani et al., 2017) with the modification proposed by Radford et al. (2019).
- We targeted two model sizes that we call in short J1-Large (7.5B parameters) and J1-Jumbo (178B parameters), which roughly correspond to GPT-3 6.7B and GPT-3 175B models
- to leverage the full extent of the power brought by depth, the width must be chosen appropriately – put another way, for a given parameter budget there is an optimal depth. Specifically, for a parameter budget of 175B (not including embedding matrix), the optimal depth should be around 80 layers, far from the 96 layers used by GPT-3 175B.
	- They used 76 because of hardware constrains
- Two of the most common tokenizers used for LMs are GPT2/3’s Bytes-Pair-Encoding (BPE) tokenizer (Sennrich et al., 2016; Radford et al., 2019; Brown et al., 2020) and T5’s SentencePiece (SP) tokenizer (Kudo and Richardson, 2018;Raffel et al., 2020),
- [GitHub](https://github.com/ai21labs/lm-evaluation))
---
