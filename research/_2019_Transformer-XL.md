### Transformer-XL: Attentive Language Models Beyond a Fixed-Length Context
---
- [Zotero Select Link](zotero://select/groups/2480461/items/QZ97WDKX)
- [Zotero URI](https://www.zotero.org/groups/2480461/items/QZ97WDKX)
- Author: [[Zihang Dai]] [[Ruslan Salakhutdinov]] [[Quoc Le]]
- Topics: [[nlp_transformers]] [[SOP]] [[relative positioning]]
- Venue: #ACL 
- Year: #2019
---
### Techniques
- [[SOP]]
- relative positional encoding

---
### Goal
---
### Major Contributions
- Learns dependency beyond a fixed length without disrupting temporal coherence
- Resolves the contex fragmentation problem. They extend the context processed by the model
- Relative positional encoding instead of absolute ones, to allow state reuse without causing temporal confusion
---
### Secondary Contribution
- direct connections between long-distance word pairs baked in attention mechanisms might ease optimization and enable the learning of long-term dependency
---
### Limitations/Future Work
- The idea of considering previous context window is analogous to having a longe input.
- No very clear how they freeze the context input
---
### Notes (Try to use backlinks)
- The reused hidden states serve as memory for the current segment which builds up a recurrent connection between the segments
- ![[2019_TransformerXL_model.png]]
- Chuncking long sequences lead to context fragmentation (physical constrains do not let us process infinite ones)
- The relative positional encoding was explored in machine translation and music generation (2018) - which the authors claim to be superior
- Benchmarks: #enwik8, #WikiText-103, #text8, #1BWord (One Billion Word)
- [[_2019_Transformer-XL]] is able to structurally maintain the sectional arrangement of Wikipedia.
- [[_2019_Transformer-XL]] L manages to semantically stay on the same topic throughout the course of generation.
- Long-range references are common in the generated text.
- [[_2019_Transformer-XL]] often generates novel content that is not present in the training data.
--- 
