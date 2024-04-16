### Recursively Summarizing Books with Human Feedback
---
- [Zotero Select Link](zotero://select/groups/2480461/items/YDAFFY2X)
- [Zotero URI](https://www.zotero.org/groups/2480461/items/YDAFFY2X)
- Authors: [[Jeff Wu]] [[Paul Christiano]] 
- Topics: [[nlp_text_summarization]] [[nlp_transformers]]
- Venue: #arXiv 
- Year: #2021
---
### Major Contributions
- Text summarization (abstractive) model based on GPT-3 + task decomposition
	- We collect a large volume of demonstrations and comparisons from human labelers, and fine-tune GPT-3 using behavioral cloning and reward modeling to do summarization recursively. At inference time, the model first summarizes small sections of the book and then recursively summarizes these summaries to produce a summary of the entire book
---
### Secondary Contribution
---
### Limitations/Future Work
- Section 6.1 lists them in details
- Our model’s book summaries lack coherence. While our models successfully generate book level summaries that contain much of the important information, they often read more as a list of events from the book, rather than a coherent summary that a human would write
- Task decomposition assumes that separate parts of the task can be completed independently. However, this may not be true for summarizing books.
---
### Notes (Try to use backlinks)
- We implement a natural task decomposition for long-form summarization: first, we train models to summarize small parts of the book, and then use these models to help humans summarize larger sections of the book, and continue with this strategy recursively.
	- An evident issue with the above approach is that tasks corresponding to passages further into a book may lack the necessary context for a successful summary. We remedy this by additionally putting prior summaries in context, from the same depth, concatenated together in order. We call these summaries the *previous context*.
	- *TR: Can we learn when/where to cut the texts?*
- When evaluated quantitatively, our model significantly outperforms our behavioral cloning baseline, and a small number of summaries approach human-level quality. Separately, we perform an ablation comparing RL to BC on summarizing smaller sections of a book, and find that RL has better scaling properties.
	- behavioral cloning (BC) and reinforcement learning (RL)
- **task decomposition** - In task decomposition, a human decomposes this parent task into several subtasks, such that each subtask is simpler than the parent task, and having the responses to the subtasks would help a human provide a training signal for the parent task. This task decomposition process can be applied recursively to obtain a tree of tasks, such that the leaf tasks are simple enough for a human to demonstrate or evaluate.
- RL on summary comparisons is more efficient than supervised learning on summary demonstrations, once the summarization policy has passed a quality threshold.
-  ![[2021_SummarizingBooks_procedure.png]]
---
