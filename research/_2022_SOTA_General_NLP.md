### State-of-the-art generalisation research in NLP: a taxonomy and review
---
- [Zotero Select Link](zotero://select/groups/2480461/items/KE5YDSBE)
- [Zotero URI](https://www.zotero.org/groups/2480461/items/KE5YDSBE)
- Authors: [[first author]] [[(optional) relevant author]] [[last author]] 
- Topics: [[tag1]] [[tag2]]
- Venue: #arXiv 
- Year: #2022
---
### Major Contributions
- We present a taxonomy for characterising and understanding generalisation research in NLP, we use that taxonomy to present a comprehensive map of published generalisation studies, and we make recommendations for which areas might deserve attention in the future.
- five axes along which studies can differ:
	- their main **motivation**, 
	- the **type of generalisation** they aim to solve, 
	- the **type of data shift** they consider, 
	- the **source** by which this data shift is obtained, 
	- the **locus** of the shift within the modelling pipeline.
---
### Secondary Contribution
- the **most common motivation** to test generalisation is the **practical motivation.**
- we find that **cross-domain** is the **most frequent**, making up more than 30% of all studies, followed by **robustness**, **cross-task** and **compositional generalisation.**
- Data shift types (Figure 9, bottom) are very unevenly distributed over their potential values: the vast majority of generalisation research considers covariate shift
	- More unexpected, perhaps, is the relatively high amount of assumed shifts, which correspond to studies that claim to test generalisation but do not explicitly consider how the test data relates to data used at various stages of model training
- On the shift source axis (Figure 9, bottom right), we see that almost half of the reviewed generalisation studies consider naturally occurring shifts: natural corpora that are not deliberately split along a particular dimension. As we will see later, this type of data source is most prevalent in cross-task and cross-domain generalisation studies, for which such naturally different corpora are widely available.
- Lastly, for the locus axis (Figure 9, top right), we see that the majority of cases focuses on (finetune) train–test splits. Much fewer studies focus on shifts between pretraining and training or pretraining and testing.

- state-of-the-art generalisation testing is not currently the standard in NLP.
- Papers that target similar generalisation questions vary widely in the type of evaluation setup they use. In our view, the field would benefit from more meta-studies that consider how the results of experiments with different experimental paradigms compare to each other.
---
### Limitations/Future Work
---
### Notes (Try to use backlinks)
- In this paper, we introduce a new framework to systematise and understand generalisation research
	- We design a taxonomy to characterise generalisation research, grounded in hundreds of existing generalisation studies;
	- We present an in-depth analysis based on over 400 papers with generalisation experiments that have come out in the last decades;
	- We make recommendations for which areas we believe deserve attention in the near future 
	- We release a set of online tools that can help readers to better understand the current landscape of generalisation-testing, exploring the data by themselves.
- **Motivation:** four different types of motivations: the practical motivation, the cognitive motivation, the intrinsic motivation, and the fairness and inclusivity motivation.
- **Types of generalisation:** we have found six main types of generalisation: compositional generalisation, structural generalisation, cross-task generalisation, cross-lingual generalisation, cross-domain generalisation, and robustness generalisation
- **Data shift:** we consider three shifts which are well-attested in the literature: covariate shift, label shift and full shift. We further include two additional types of shift – assumed shift and multiple shifts – to account for studies that cannot be labelled with any of the three main shift types.
- **Source:** We distinguish four different sources of shifts: naturally occurring shifts, artificially partitioned natural corpora, generated shifts and fully generated datasets.
- Using different visualisations, we analyse the most relevant trends and find several noteworthy patterns (§7.2.2)
- the experimental design of a study is not always lined up with its motivation
- an increasing number of papers investigating generalisation does not explicitly consider the relationship between train and test data.
- many papers that contain a multi-stage modelling pipeline investigate generalisation in one part of that pipeline, but not in the other
- more meta-studies might be needed that compare results across different values of the same axis, for example, to understand what is the relationship between results obtained with fully generated data and generated shifts
- both studies on cross-lingual generalisation and studies with a fairness motivation are under-represented in our review.
-
- ![[2022_SOTA_General_NLP_overview]]
- ![[2020_SOTA_General_NLP_interacations]]
![[2022_SOTA_General_NLP_method_taxonomy]]

Are there any combinations of axes that occur together very often or combinations that are instead rare?
![[2022_SOTA_General_NLP_interaction]]
- shifts are likely caused by the use of increasingly large, general-purpose training corpora. When such pretrained models are further finetuned, they often consider either a shift between pretraining and finetuning where new labels are introduced, or a covariate shift in the finetuning stage and, as such, do not require an in-depth understanding of the pretraining corpus
- 
---
