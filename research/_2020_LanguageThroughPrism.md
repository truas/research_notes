### Language Through a Prism: A Spectral Approach for Multiscale Language Representations
---
- [Zotero Select Link](zotero://select/groups/2480461/items/Z6TDDLG2)
- [Zotero URI](https://www.zotero.org/groups/2480461/items/Z6TDDLG2)
- Authors: [[Alex Tamkin]] [[Noah Goodman]] [[Dan Jurafsky]]
- Topics: [[nlp_lm]] [[nlp_ann]]
- Venue: #NIPS 
- Year: #2020
---
### Major Contributions
- the main idea is to apply different band filters into different layers to "clean" the signal from from the weights 
- to what extent do deep models capture information on different scales o text representation (words, sentence, paragraph, documents)
- Spectral Transform - [[DCT|discrete cosine transform]] (related to [[DFT|discrete Fourier transform]])
	- Used in audio encoding, texture analysis, image classification, and compression
	- Intuitively, the DCT computes the similarity of a signal and cosine waves of different frequencies by taking the dot product between them.
	- [[DCT]] - real-to-real
	- [[DFT]] - complex-to-complex
- Show signal process:disentagle scale-specific information i existing embeddings and train models to learn more about particular scales
	- filtered embeddings
	- prism layers
---
### Secondary Contribution
---
### Limitations/Future Work
- The idea is interesting, but it's not clear how their claim is validated wrt the scales on text documentation. they do explore different taks/data, but the granularity is not discussed. the datasets are: POS, topic classification and dialog speech act classification
---
### Notes (Try to use backlinks)
- Apply spectral filters into [[_2019_BERT]]
- Tasks: PoS, dialog speech act classification,  topic classiciation (20News)
- the highest frequency spectral band still performs worse than the original representations, suggesting that lower frequency information is sometimes necessary for this task
- 
---
