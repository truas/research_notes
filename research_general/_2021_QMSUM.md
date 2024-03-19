### QMSum: A New Benchmark for Query-based Multi-domain Meeting Summarization
---
- [Zotero Select Link](zotero://select/groups/2480461/items/AFHU6UWG)
- [Zotero URI](https://www.zotero.org/groups/2480461/items/AFHU6UWG)
- Authors: [[Ming Zhong]] [[Dragomir Radev]] 
- Topics: [[nlp_text_summarization]] [[nlp_dataset]]
- Venue: #NAACL 
- Year: #2021
---
### Major Contributions
- we define a new query-based multi-domain meeting summarization task, where models have to select and summarize relevant spans of meetings in response to a query, and we introduce QMSum, a new benchmark for this task.
- locate-then-summarize
	- Specifically, given a query, a model called Locator is used to locate the relevant utterances in the meeting transcripts, and then these extracted spans are used as an input to another model called Summarizer to generate a query-based summary
- 1) We propose a new task, query-based multi-domain meeting summarization, and build a new benchmark QMSum with a hierarchical annotation structure. 
- 2) We design a locate-then-summarize model and conduct comprehensive experiments on its strong variants and different training settings.
- 3) By human evaluation, we further pose the challenges of the new task, including the impact of different query types and factuality errors.
---
### Secondary Contribution
- we investigate a locate-then-summarize method and evaluate a set of strong summarization baselines on the task.
---
### Limitations/Future Work
- Podcast transcripts
- EU parlment transcripts
---
### Notes (Try to use backlinks)
- meeting summaries such as topics (Li et al., 2019), opinions, actions, and decisions (Wang and Cardie, 2013). This poses the question of whether a single paragraph is enough to summarize the content of an entire meeting?
- summarization data of a single domain usually has poor generalization ability (Wang et al., 2019; Zhong et al., 2019b; Chen et al., 2020).
- Summarizer with the current powerful abstractive models to explore whether the query-based meeting summarization task on our dataset is challenging.
- Locator, the dimension of speaking embedding is 128 and the dimension of turn and query embedding is 512. Notably, we fin that removing Transformers in Locator has little impact on performance
- To reduce the burden of the abstractive models, we utilize Locator to extract 1/6 of the original text and input them to Summarizer.
- ![[2021_QMSUM_pipeline.png]]
---
