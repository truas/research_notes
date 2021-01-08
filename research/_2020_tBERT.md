### tBERT: Topic Models and BERT Joining Forces for Semantic Similarity Detection
---
- [Zotero Select Link](zotero://select/groups/2480461/items/6L2Y5TZ3	)
- [Zotero URI](https://www.zotero.org/groups/2480461/items/6L2Y5TZ3)
- Authors: [[Nicole Peinelt]] [[Maria Liakata]]
- Topics: [[nlp_transformers]] [[nlp_topic_modeling]]
- Venue: #ACL
- Year: #2020
---
### Major Contributions
- novel topic-informed BERT-based architecture for pairwise semantic similarity detection
	- While other topic models can be used, we experiment with two popular topic models: [[_2003_LDA]] and [[_2014_GSDMM]]
		- [[_2003_LDA]] is the most popular and widely used topic model, but it has been reported to be less suitable for short text (Hong and Davison, 2010). Therefore, we also experiment with the popular short text topic model [[_2014_GSDMM]]
	- 
---
### Secondary Contribution
- Do topics improve BERT’s performance? Adding LDA topics to BERT consistently improves F1 performance across all datasets. Moreover, it improves performance on non-obvious cases over BERT on all datasets (except for Quora which contains many generic examples and few domain specific cases
- topic models could serve as an additional source for dataset-specific information
---
### Limitations/Future Work
- Future work may focus on how to directly induce topic information into BERT without corrupting pretrained information and whether combining topics with other pretrained contextual models can lead to similar gains. An other research direction is to investigate if introducing more sophisticated topic models, such as
named entity promoting topic models (Krasnashchok and Jouili, 2018) into the proposed framework can further improve results.
---
### Notes (Try to use backlinks)
- There is currently no standard way of combining topics with pretrained contex
tual representations such as BERT.
- While large improvements have been achieved on paraphrase detection (Tomar et al., 2017; Gong et al., 2018), semantic similarity detection in Com munity Question Answering (CQA) remains a challenging problem.
- ![[2020_tBERT_architecture.png]]
- Topic number and alpha value The number of topics and alpha values are important topic model hyper-parameters and dataset dependent
- The [[_2020_tBERT]] settings generally scored higher than [[_2020_tBERT]], with word topics and usually outperforming document topics.
- longer finetuning of BERT could not exceed [[_2020_tBERT]] best performance from the first 3 epochs (dotted line) on any dataset.
---
