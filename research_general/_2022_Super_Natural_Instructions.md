### Super-NaturalInstructions: Generalization via Declarative Instructions on 1600+ NLP Tasks
---
- [Zotero Select Link](zotero://select/groups/2480461/items/WT7IWJPF)
- [Zotero URI](https://www.zotero.org/groups/2480461/items/WT7IWJPF)
- Authors: [[Yizhong Wang]] [[Swaroop Mishra]] [[Daniel Khashabi]] 
- Topics: [[nlp_prompt]] [[nlp_tasks]]
- Venue: #arxiv
- Year: #2022

---
### Major Contributions
- SUPER-NATURALINSTRUCTIONS, [[Sup-NatInst]] a benchmark of 1,616 diverse NLP tasks and their expert-written instructions. Our collection covers 76 distinct task types, including but not limited to classification, extraction, infilling, sequence tagging, text rewriting, and text composition.
	- In this paper, we construct a meta-dataset (i.e., dataset of datasets; Triantafillou et al., 2019) that consists of a wide variety of NLP tasks with their instructions, and train a model that can perform a new task given the instruction, outperforming InstructGPT (which uses 16× more parameters).
	- It brings in a diverse variety of tasks—76 broad task types spanning 55 different languages.
	- These tasks and their instructions are contributed by 88 NLP practitioners, in response to our public call.
	- We limit the number of instances in each task to 6.5K to avoid an imbalance of instances between tasks.
	- We had 88 contributors from diverse locations and backgrounds contribute to our repository.
	- **Statistics**. Table 2 shows various statistics for the benchmark. In total, the dataset includes 1616 tasks and 5M instances. On average, each instruction is paired with 2.8 positive and 2.4 negative examples. The average definition length is 56.6 in words.
- [GitHub Link](https://github.com/allenai/natural-instructions)

---
### Secondary Contribution
- A large number of training instances do not help generalization. We then vary the number of instances per task that are used for finetuning (Fig. 5b). While the conventional wisdom in supervised learning is that more training instances usually helps (Banko and Brill, 2001; Sun et al., 2017; Hestness et al., 2017), in our setup, the model’s performance saturates when only 64 instances per task are used for training.
---
### Limitations/Future Work
- 
---
### Notes (Try to use backlinks)
- Their [[Tk-Instruct]] model is built on T5 model (Raffel et al., 2020) over all the task instructions in our training set, and is evaluated on unseen tasks in the test set. Interestingly, an 11B-parameter Tk-INSTRUCT can outperform the 175B-parameter [[InstructGPT]] model by 9.9 ROUGE-L points when evaluated on 119
- The compelling empirical performance of TkINSTRUCT confirms the importance of super-sized meta datasets such as our SUP-NATINST to facilitate research towards generalizable NLP models
- [[Sup-NatInst]] extends NATINST (Mishra et al., 2022b) with 26× more tasks and greater variety of task types (Fig. 2). While CROSSFIT (Ye et al., 2021) focuses on benchmarking with a few in-context examples, our benchmark also offers task instructions.
- More recent studies show promise that large-scale multi-task learning can enable strong generalization to similar tasks via unified encoding (Khashabi et al., 2020; Xie et al., 2022) or better finetuning results on downstream tasks (McCann et al., 2018; Aribandi et al., 2022).
- ![[2022_Super_Natural_Instruction_example.png]]
- ![[2022_Super_Natural_Instructions_summary.png]]
---
