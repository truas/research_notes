### What Will it Take to Fix Benchmarking in Natural Language Understanding?
---
- [Zotero Select Link](zotero://select/groups/2480461/items/49AU8YVD)
- [Zotero URI](https://www.zotero.org/groups/2480461/items/49AU8YVD)
- Authors: [[Samuel R. Bowman]] [[George E. Dahl]]
- Topics: [[nlp_tasks]] [[nlp_ben]] [[nlp_vision]] [[nlp_metrics]]
- Venue: #NAACL 
- Year: #2021
---
### Major Contributions
- Evaluation for many natural language understanding (NLU) tasks is broken: we lay out four criteria that we argue NLU benchmarks should meet
---
### Secondary Contribution
---
### Limitations/Future Work
---
### Notes (Try to use backlinks)
-[[2021_ DynaBench]] benchmark suite argues that “benchmarks saturate”, “benchmarks have artifacts”, “researchers overfit on benchmarks”, and “benchmarks can be deceiving” and use these claims to motivate abandoning the IID paradigm in favor of benchmark data that is collected adversarially by asking a broad population of annotators to try to fool some reference neuralnetwork model
- [SuperGLUE]] benchmark project (Wang et al., 2019a) solicited dataset submissions from the NLP research community in 2019, but wound up needing to exclude the large majority of the submitted tasks from the leaderboard because the BERT model (Devlin et al., 2019) was already showing performance at or above that of a majority vote of human crowdworkers. Of the eight tasks for which BERT did poorly enough to leave clear headroom for further progress, all are now effectively saturated
- This paper focuses instead on the case where one is interested in reaching excellent performance on some language task and is willing to collect data or otherwise expend resources to make that possible.
- Reliable Annotation: AVOID:
	- (i) examples that are carelessly mislabeled
	- (ii) examples that have no clear correct label due to unclear or underspecifie task guidelines
	- (iii) examples that have no clear correct label under the relevant metric due to legitimate disagreements in interpretation among annotators.
- A viable alternate approach could involve the expanded use of auxiliary metrics: Rather than trying to fully mitigate bias within a single general dataset and metric for some task, benchmark creators can introduce a family of additional expert-constructed test datasets and metrics that each isolate and measure a specific type of bias
- ![[2021_FixBenchmarkNLP_points.png]]
---
