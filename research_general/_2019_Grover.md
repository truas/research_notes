### Defending Against Neural Fake News
---
- [Zotero Select Link](paste here)
- [Zotero URI](paste here)
- Authors: [[Rowan Zellers]] [[Yejin Choi]]
- Topics: [[nlp_lm]] [[nlp_nlg]] [[fake news]]
- Venue: #NIPS #arXiv 
- Year: #2019
---
### Major Contributions
- They propose a model for controllable text generation - [[_2019_Grover]]
	- Generating aRticles by Only Viewing mEtadata Records
	- Given a headline, the model can generate the rest of the article, human find more trustworthy than human-written desinformation
- Study to understand an respond to neural fake news before it scale
-  [[_2019_Grover]] performs best at detecting [[_2019_Grover]]s fake news
	-  Similar findings also with [[_2019_GPT-2]] and [[_2018_GPT]]. models are better in discovering themselves.
-  
---
### Secondary Contribution
- the **unpaired** setting for training is similar to the one used in plagiarism detectionn in which a document is classified as _human_ or  _machine_
	- the **paired** setting has two news articles have the same metadata, the machine-wirtten asticle needs to present a higher 'machine' probability than the human-written one
---
### Limitations/Future Work
 - *Obtaining the data required through Common Crawl cost $10k in AWS credits and can be massively parallelized over many CPUs. Training Grover-Mega is relatively inexpensive: at a cost of $0.30 per TPU v3 core-hour and two weeks of training, the total cost is $25k."* 
	 - This paper was published on NIPS, so it costed 35K USD,  between data + train - not to mention the failures, or labor time.
 - Nice future work: the same way youtube videos are parsed to avoid pornography videos or racist content; text could have a deep generative model to look for fake productions or plagiarism.

---
### Notes (Try to use backlinks)
- Similar framework to [[_2020_Stylometry_vs_MachineNews]]:
	- Adversary: generate fake stories that match specified attributes
	- Verifier: classify news stories as real or fake. Access to unlimited real stories, but just  a few fake.
- Based on [[_2019_GPT-2]]
- Their [[LM]] is broken into  p(domain,date, authors, headline,body) with three targets: body, authors, and headline
- [[_2019_Grover]] diagram
- ![[2019_Grover_diagram.png]]
---
