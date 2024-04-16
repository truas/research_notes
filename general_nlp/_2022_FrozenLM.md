### Standing on the shoulder of giant frozen language models
---
- [Zotero Select Link](zotero://select/groups/2480461/items/72NJGMZH)
- [Zotero URI](https://www.zotero.org/groups/2480461/items/72NJGMZH)
- Authors: [[Yoav Levine]] [[Yoav Shoham]] 
- Topics: [[nlp_train]] [[nlp_lm]]
- Venue: #arXiv #AI21Labs
- Year: #2022
---
### Major Contributions
- leveraging frozen LMs can do just as well as fine tuning in challenging domains without sacrificing the underlying model’s versatility. 
	- we introduce three novel methods for leveraging frozen models: **input-dependent prompt tuning, frozen readers, and recursive LMs**, each of which vastly improves on current frozen-model approaches
- 
---
### Secondary Contribution
---
### Limitations/Future Work
- some of our methods even outperform fine-tuning approaches in domains currently dominated by the latter. The computational cost of each method is higher than that of existing frozen model methods, but still negligible relative to a single pass through a huge frozen LM
---
### Notes (Try to use backlinks)
- current leading techniques for leveraging a “frozen” LM—i.e., leaving its weights untouched—still often underperform fine-tuning approaches which modify these weights in a task-dependent way.
- We argue that versatile natural language interfaces can be built on top of frozen LMs.
	- **Non-forgetfulness:** Once the original LM is fine tuned on any multi-task suite, it can suffer from catastrophic forgetfulness on capabilities far enough from these tasks (manifesting, for example, in perplexity degradation). A frozen LM will never suffer forgetfulness, since it remains unchanged. 
	- **Extensibility:** When attempting to add a new task to a fine-tuned LM, there is no guarantee that performance on the original task suite will be retained, so the model must be retrained on all tasks together. Given the cost of training such models—in some cases, millions of dollars (Sharir et al., 2020)—it is clearly infeasible to do so repeatedly. In contrast, when adding new capabilities as new external components over a frozen backbone, there is no cross interference between capabilities.
- Some of the leading approaches for leveraging frozen models include **prompt tuning** (Lester et al., 2021), **prefix tuning** (Li & Liang, 2021), **adapter tunin**g (Rebuffi et al., 2017; Houlsby et al., 2019), and **low rank adaptation** (Hu et al., 2021). 
	- All of these methods share the idea of training a very small number of parameters around a frozen model to achieve optimized performance on given tasks.
- The first, already discussed above, is massive multi-tasking: asking a single model to simultaneously address many NLP tasks. The variety of existing multi-tasked models are all fine tuned; no frozen model method has been considered in this setting.
- a challenging individual task, in which leading methods are all fine tuned (Chen et al., 2017; Lee et al., 2019; Karpukhin et al., 2020; Roberts et al., 2020): open-domain question answering, asking a model to answer general-knowledge questions.
- **ID-PT** **input-dependent prompt tuning**
	- we present an approach that we call **input-dependant prompt tuning (ID-PT)** for massively multi-tasking an LM while keeping it frozen. ID-PT trains a very small external network that receives an input from one of the many curated datasets, and creates a neural prompt on-the-fly that best prepares the frozen LM for addressing this input (see Figure 1)
	- We believe that this demonstrates that there is no real need for the above mentioned multitude of huge fine-tuned LMs targeting the multi-task domain
	- ![[2022_FrozenLM_ID-PT.png]]
	- While ID-PT is thus considerably more “heavy weight” than prompt tuning, ID-PT is still a very small increment to the frozen model, adding ∼ 0.3% to the number of parameters and ∼ 1% to inference time
- **Frozen readers**
	- we used an external re-ranking module for increasing the chance of getting the answer in a small amount of passages that fits into the frozen LM’s context window.
	- ![[2022_FrozenLM_LMReader.png]]
	- At a high level, we trained a re-ranker to produce improved passage relevance scores by jointly attending to the question and passage. We then greedily added passages to our context in descending order, until the context length of our frozen LM reader was full. We thus prepared training data for prompt tuning our frozen LMs to serve as readers.
	- When not limited to the DPR retriever, our frozen J1-Grande-17B matches the performance of the strong fine-tuned FiD-Distill model (Izacard & Grave, 2020b), and outperforms EMDR2 (Singh et al., 2021), which jointly fine tuned both retriever and reader end-to-end.

- **Recursive LMs**
	- Since both the input and output spaces of an LM are in natural language, and since the same LM can serve a multitude of functionalities, it makes sense in principle to re-apply an LM to its own output, an operation which we dub **LM recursion**
	- ![[2022_FrozenLM_RecursiveLM.png]]
	- Two distinct methods for putting this idea into practice 
		- In Section 4.1, we present a **textual approach**, in which output text is sampled after the first pass through the frozen LM and reinserted into the same frozen LM.
			- Textual LM recursion improved on the saturated prompt tuning model that provided its input candidates by 1.8 points, despite both the candidate proposal and candidate choosing processes being based on the same frozen LM.
			- **Limitations** - Textual recursive LMs suffer from several drawbacks: (1) inference is slow, due to the intermediate operation of sampling; (2) our reliance on sampling means that we discard some of the information contained in the final embedding layer of the first pass; (3) both passes through the LM are prompt tuned to answer the input question, where in principle the first pass could be less constrained, since question answering ability matters only after the second LM pass; and (4) textual recursive LMs use very few trained parameters
		- In Section 4.2 we present a **neural approach**, in which a small trainable network maps the vector representation at the output of the frozen LM to a vector representation input for the next iteration through the same frozen LM.
			- by “stitching together” two replicas of the frozen LM via such a Connector network, we get an LM–Connector–LM network, which is essentially a deeper (mostly frozen) autoregressive Transformer architecture.
			- Our ablations suggest that initializing the Connector via pretraining the recursive LM on the language modeling task was vital to its fine-tuning performance. Doing the same for the prompt tuning baseline did not seem to similarly help.
	- The prospect of improving performance by recursively applying an LM to its own output has the potential to be a game changer for the economics of serving LMs. 
		- Given an LM with unsatisfactory performance on a certain task, an existing performance improvement vertical is to pretrain an even larger LM. 
		- However, pretraining larger and larger LMs quickly becomes prohibitively expensive, and huge models are expensive to deploy even at evaluation time. 
		- The need for improved performance may only arise in certain tasks or for certain inputs within a task.
		- Improvement by re-applying the existing LM over its own output allows paying double the cost of a single forward pass and getting double the compute only when needed, a more focused and much cheaper option than pretraining and deploying a model of double the size.
	- the methods presented in this section demonstrate that while LMs are treated as single-use resources per query, significant performance gains can be achieved by treating them as resources that can be progressively revisited for improved performance per query
- More importantly and more broadly, however, we believe that our results point towards a new stage in the application of huge LMs to practical problems, in which the design of task-specific neural middleware will often take the place of fine tuning
---
