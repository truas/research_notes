---
- Auhtor: [[Suchin Gururangan]] [[Noah Smith]] [[Iz Beltagy]]
- Topics: [[nlp_lm]] [[nlp_task]] [[nlp_lm]]
- Venue: #ACL
- Year: #2020
---
### Techniques
---
### Goal
They show a second [[Pretraining]] in domain-adaptative pretraining (DAPT) leads to performance gains, under both high and low resource settings.

---
### Major Contributions
- Highlight of how task-adaptative pretraining [[TAPT]] and [[DAPT]] behave on four domains and  eight tasks
- [[transfer learning]] of adapted [[LM|Language Models]] across multiple domains and tasks
- importance of pretraining on human-curated datasets, and simple data selection strategy
---
### Secondary Contribution
- [[TAPT]] is even better when unlabeled data from the task distribution 
- Source code for [[TAPT]] and [[DAPT]] models in [dont-stop-pretraining](https://github.com/allenai/dont-stop-pretraining)
-  They advocated that task designers should also release an unlabeled data to aid model adaptation
---
### Limitations/Future Work
- Better data selection apporach for [[TAPT]]
- Efficient adaptation large pretrained [[LM]] to distant domains
- Building reusable [[LM]] after adaptation
---
### Notes (Try to use backlinks)
- [[TAPT]] - available unlabeled data associated with a given task. Less data, but more curated information
- [[DAPT]] - large corpora of domain specific text
-  Do large pretrained models work universally or is still helpful to build separate pretrained models for specific domains?
- The more dissimilar the domain, the more [[DAPT]] benefits
- off-the-shelf [[RoBERTa]] is used as a baseline
- Exposure  to omre data without accounting for the document might jeopardize the end-task performance
- Table 10 has a nice summary of their techniques.
- Appendices not read
---

