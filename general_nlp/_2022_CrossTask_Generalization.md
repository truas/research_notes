### Cross-Task Generalization via Natural Language Crowdsourcing Instructions
---
- [Zotero Select Link](zotero://select/groups/2480461/items/CJ46AS8G)
- [Zotero URI](https://www.zotero.org/groups/2480461/items/CJ46AS8G)
- Authors: [[Swaroop Mishra]]  [[Hannaneh Hajishirzi]] 
- Topics: [[nlp_prompt]] [[nlp_llm]]
- Venue: #ACL #AllenAI
- Year: #2022

---
### Major Contributions
- we introduce **NATURAL INSTRUCTIONS**, a dataset of 61 distinct tasks, their humanauthored instructions, and 193k task instances (input-output pairs). The instructions are obtained from crowdsourcing instructions used to create existing NLP datasets and mapped to a unified schema.
	- In total, there are 61 tasks, which are categorized into 6 semantic categories (Table 2).
- [Link](: https://github. com/allenai/natural-instructions-v1)
- 
---
### Secondary Contribution
- our dataset not only contains typical downstream tasks in NLP, but also the intermediate subtasks that are not well-represented in the common benchmarks
- The results show that with NOINSTRUCTION encoding there is no tangible value in observing more tasks. In contrast, the generalization of the models that encode instructions improves with observing more tasks.
- Our cases study (Table 6) indicates that the models work better without (w/o) negative examples, contrary to the previously-observed benefits of other instructional elements (e.g., definition, positive examples). This is aligned with the previous studies (Xuan et al., 2020; Lin et al., 2003) that discuss the challenges of learning from negative examples.
---
### Limitations/Future Work
- 
---
### Notes (Try to use backlinks)
- A long-standing challenge in AI is to build a model that learns a new task by understanding the human readable instructions that define it.
- We build NATURAL INSTRUCTIONS, a dataset consisting of natural crowdsourcing instructions for various tasks and their instances. Training on seen tasks Tseen in our dataset, we build a model that learns to follow natural instructions that define a task and perform tasks (i.e., mapping input to output).
- Task Splits and Generalizations Types
	- Random split.
	- Leave-one-out generalization.
		- leave-one-category: evaluates how well a model generalizes to a task category if it is trained on others
		- leave-one-dataset: evaluates how well a model can generalize to all tasks in a particular dataset if it is trained on all other tasks
		- leave-one-task: evaluates how well a model can learn a single task by training on all other tasks.
- Evaluation metrics. We treat all of our tasks as text generation problems and evaluate them with automated evaluation metrics for text generation. In particular, we use ROUGE-L
- We observe that the question-generation (QG) tasks benefit the most from POSITIVE EXAMPLES, whereas in classification (CF), POSITIVE EXAMPLES are of little help
- 
- ![[2022_CrossTask_Generalization_instructions.png]]
- ![[2022_CrossTask_Generalization_example.png]]
---
