### Meta-learning for Few-shot Natural Language Processing: A Survey
---
- [Zotero Select Link](zotero://select/groups/2480461/items/T9A9CS3E)
- [Zotero URI](https://www.zotero.org/groups/2480461/items/T9A9CS3E)
- Authors: [[Wenpeng Yin]]
- Topics: [[nlp_survey]] [[nlp_meta]]
- Venue: #arXiv #salesforce
- Year: #2020
---
### Major Contributions

---
### Secondary Contribution
- meta-learning doesn’t learn how to solve a specific task. It successively learns to solve many tasks
- Since meta-learning treats tasks as training examples, ideally, the more training tasks the better. However, multi-task learning may meet increasing challenges in training simultaneously over too many tasks.
---
### Limitations/Future Work
---
### Notes (Try to use backlinks)
- The goal of meta-learning is to train a model on a variety of tasks with rich annotations, such that it can solve a new task using only a few labeled samples
- meta-learning framework treats tasks as training examples - to solve a new task, we first collect lots of tasks, treating each as a training example and train a model to adapt to all those training tasks, finally this model is expected to work well for the new task.
	- The test error on the sampled task serves as the training error of the meta-learning process at the current iiteration
- Transfer learning refers to a problem area (task A helps task B) while meta-learning refers to methodology which can be used to improve transfer learning as well as other problems
- ![[2020_Meta_and_Transfer.png]]
- Usually, the progress of meta-learning is split by its techniques, such as metric-based or optimization based.
---
