###  Rogue Scores
---
- [Zotero Select Link](zotero://select/groups/2480461/items/E983HFCK)
- [Zotero URI](https://www.zotero.org/groups/2480461/items/E983HFCK)
- Authors: [[Max Grusky]] 
- Topics: [[nlp_metrics]] [[nlp_rouge]] [[nlp_evaluation]]
- Venue: #arxiv #ACL
- Year: #2023

---
### Major Contributions
- We conduct a systematic review and evaluation sensitivity analysis investigating the reproducibility, comparability, and correctness of ROUGE scores. 
- We review ROUGE methodology of 2,834 papers published at major machine learning venues and 831 associated codebases. 
- We perform sensitivity analysis of 10 common ROUGE configurations and test correctness of 17 common ROUGE packages
- (A) Critical evaluation decisions and parameters are routinely omitted, making most reported scores irreproducible. 
- (B) Differences in evaluation protocol are common, affect scores, and impact the comparability of results reported in many papers. 
- (C) Thousands of papers use nonstandard evaluation packages with software defects that produce provably incorrect scores.
- [Website](https://analyses.org/2023/rogue-scores/)
---
### Secondary Contribution
- 
---
### Limitations/Future Work
- 
---
### Notes (Try to use backlinks)
- This work outlines a major research integrity issue that affects thousands of machine learning papers in dozens of language and vision tasks over a span of nearly twenty years.
- First introduced two decades ago, the text similarity metric ROUGE (Lin, 2004) has become become one of the most common evaluation metrics in natural language processing
- While researchers dedicate substantial time and resources to achieving small improvements in model scores, there is seemingly little concern that subtle evaluation protocol discrepancies are equivalently capable of producing similar score differences.
- only 20% of evaluations have enough detail to reproduce. This is substantially lower than other scientific fields, including the 39% reproduction rate of psychology studies (Open Sci. Collab., 2015). Few papers release code (33%) and even fewer release code with usable ROUGE evaluation (12%).
- It is hard to know if papers evaluate comparably without ROUGE parameters, which only appear in 5% of papers (more in Section 3). But the most alarming finding of this review is, while only 35% of papers cite ROUGE software, **76% of citations are for packages that compute incorrect scores**
	- Surprisingly, none of these packages has been validated against ROUGE-1.5.5, the original ROUGE implementation of Lin (2004). This validation should have occurred years ago before these packages were ever used;
- only 5% of papers list ROUGE parameters.
- we evaluate ROUGE in our baseline configuration: reporting F1 scores computed using default parameters5 of the standard ROUGE-1.5.5 implementation with no additional preprocessing. Next, we compute 24 ROUGE scores in 10 alternative configurations from our Section 2 review, which differ in parameters, protocol, preprocessing, and score reporting.
- Application of Porter stemming is one of the most inconsistent ROUGE evaluation decisions identified
	- Because stemming inflates all ROUGE scores, a large number of scores may be accidentally incomparable
- **What the F is Happening?** The MS/rouge package developed at Microsoft is quite unique: rather than computing standard balanced F1 scores, it instead computes recall-biased F1.2 scores. This is the most popular ROUGE package for evaluating captioning (Chen et al., 2015), reading comprehension (Nguyen et al., 2016), and general NLG tasks (Sharma et al., 2017). However, there is no obvious research reason for choosing F1.2 scores for these tasks. So, where did this magic number come from? The version control history of this package indicates F1.2 was chosen by mixing up the meanings of two ROUGE-1.5.5 parameters: -w 1.2 and -p 0.5. Code excerpt shown in Figure 5. This error inflates ROUGE scores in hundreds of papers.
- **A Nondeterministic Evaluation Metric** Google Research distributes a popular ROUGE implementation, GL/rougescore. This package stems incorrectly, has an incorrect default implementation of ROUGE-L, and does not use a fixed random seed during bootstrapping. This makes GL/rougescore both incorrect and nondeterministic (two qualities not typically associated with benchmark evaluation metrics).
- Since the publication of BART, PT/files2rouge has enabled stemming by default, making the original BART scores irreproducible.
- **AJ/pyrouge.** This package contains a bug that tokenizes references and hypothesis incorrectly, treating every single character as a word when computing ROUGE scores. Because reference-hypothesis overlap of character n-gram is typically much higher than word n-gram overlap, AJ/pyrouge computes unreasonably high ROUGE scores.
- ![[2023_ROGUE_Scores_summary.png]]
- ![[2023_ROGUE_Scores_decisions.png]]
---
