### TLDR: Extreme Summarization of Scientific Documents
---
- [Zotero Select Link](zotero://select/groups/2480461/items/AMIHLAU9)
- [Zotero URI](https://www.zotero.org/groups/2480461/items/AMIHLAU9)
- Authors: [[Isabel Cachola]] [[Daniel Weld]] [[Kylo Lo]]
- Topics: [[nlp_text_summarization]] [[nlp_lm]]
- Venue: #arXiv
- Year: #2020
---
### Major Contributions
- SCITLDR, a new multi-target dataset of 5.4K TLDRs over 3.2K papers
- CATTS (Controlled Abstraction for TLDRs with Title Scaffolding), a simple yet effective learning strategy for generation TLDR
	- (1) the limited size of the training data
	- (2) the need for domain knowledge in order to write high-quality gold TLDRs.
---
### Secondary Contribution
- Section 7 contains a short reference list for Text summarization literature, and scientific document summarization.
- 
---
### Limitations/Future Work
---
### Notes (Try to use backlinks)
- is typically composed of salient information (in TLDR dicated by colored spans) found in the abstract, intro, and conclusion sections of a paper
- Considering only one gold TLDU for each paper as a basis of automated evaluation might result in inaccurate system quality assessment because content that might appear in a TLDR can have large variability.
- TLDRs written from the perspective of the author (“TLDRAuth”)
- TLDRs written from the perspective of the peer reviewer(“TLDR-PR”).
- We use the OpenReview API to collect pairs of papers and author-written TLDRs
- ![[2020_TLDR_systems.png]]
- We use the S2ORC pipeline (Lo et al., 2020) to convert PDFs to structured,
machine-readable full text.
- SCITLDR is smaller in comparison to automatically collected datasets, such as XSUM and ArXiv, but is larger in comparison to other manually collected datasets, such as SciSummNet
- Similar to multitask-learning, training on heterogenous data annotated with
control codes as been shown to improve controlled generation in autoregressive language models (Keskar et al., 2019; ElSahar et al., 2020; Sudhakar et al., 2019; Li et al., 2020).
---
