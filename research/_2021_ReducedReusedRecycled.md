### Reduced, Reused and Recycled: The Life of a Dataset in Machine Learning Research
---
- [Zotero Select Link](zotero://select/groups/2480461/items/J9NHZGGL)
- [Zotero URI](https://www.zotero.org/groups/2480461/items/J9NHZGGL)
- Authors: [[Bernard Koch]] [[Jacob G. Foster]] 
- Topics: [[ml]] [[tag2]]
- Venue: #arXiv 
- Year: #2021
---
### Major Contributions
- We study how dataset usage patterns differ across machine learning subcommunities and across time from 2015-2020. We find increasing concentration on fewer and fewer datasets within task communities, significant adoption of datasets from other tasks, and concentration across the field on datasets that have been introduced by researchers situated within a small number of elite institutions.
---
### Secondary Contribution
- we find that these dominant datasets have been introduced by researchers at just a handful of elite institutions.
- the majority of papers within most tasks use datasets that were originally created for other tasks, instead of ones explicitly created for their own task—even though most tasks have created more datasets than they have imported.
---
### Limitations/Future Work

---
### Notes (Try to use backlinks)
- Because advancement on established benchmarks is viewed as an indicator of progress, researchers are encouraged to make design choices that maximize performance on benchmarks, as this increases the legitimacy of their work.
	- Close alignment of benchmark datasets with “real world” tasks is thus critical to accurate measurement of collective scientific progress and to safe, ethical, and effective deployment of models in the wild
- The necessity of SOTA results on well-established benchmarks for publication has been identified as a barrier to the development of new ideas
- while community alignment on benchmarks and metrics can enable rapid algorithmic advancement, excessive focuson single metrics at the expense of more comprehensive forms of rigorous evaluation can lead the community astray and risk the development of models that generalize poorly to the real world.
- We downloaded the complete [[PWC| Papers With Code]] dataset on 06/16/2021 (licensed under CC BY-SA 4.0).
	- We found 4,384 datasets on the site and scraped 60,647 papers that PWC associates with those datasets using a PWC internal API
	- In more than half of Computer Vision communities, authors adopt at least 71.9% of their datasets from a different task. The equivalent statistic in Methodology tasks is 74.1%.
	- Half of Natural Language Processing communities adopt datasets less than 27.4% of the time.
	- Overall, we find that widely-used datasets are introduced by only a handful of elite institutions (Figure 3 left). In fact, over 50% of dataset usages in PWC as of June 2021 can be attributed to just twelveinstitutions.
	- In this paper, we find that task communities are heavily concentrated on a limited number of datasets, and that this concentration has been increasing over time
	- Moreover, a significant portion of the datasets being used for benchmarking purposes within these communities were originally developed for a different task
	- This result is striking given the fact that communities are creating new datasets, in most cases more than the unique number that have been imported from other task, but the newly created datasets are being used at lower rates.
	- NLP tasks differ somewhat from PWC as a whole: the broader trend of increasing concentration on a few datasets is moderated in NLP communities, new datasets are created at higher rates, and outside datasets are used at lower rates.
	- 
- [Datasheet and Code](https://github.com/kochbj/Reduced_Reused_Recycled)
---
