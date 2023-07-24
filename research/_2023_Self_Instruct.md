### SELF-INSTRUCT: Aligning Language Models with Self-Generated Instructions
---
- [Zotero Select Link](zotero://select/groups/2480461/items/PWMB6UA2)
- [Zotero URI](https://www.zotero.org/groups/2480461/items/PWMB6UA2)
- Authors: [[Yizhong Wang]] [[Noah Smith]] [[Hannaneh Hajishirzi]] 
- Topics: [[nlp_llm]] [[nlp_prompt]]
- Venue: #arxiv #ACL
- Year: #2023

---
### Major Contributions
- We introduce [[SELF-INSTRUCT]], a framework for improving the instruction-following capabilities of pretrained language models by bootstrapping off their own generations.
- [GitHubRepo](https://github.com/yizhongw/self-instruct)
- The iterative [[SELF-INSTRUCT]] process on this model leads to about 52k instructions, paired with about 82K instance inputs and target outputs
	- (1) we introduce SELF-INSTRUCT, a method for inducing instruction following capabilities with minimal human-labeled data; 
	- (2) we demonstrate its effectiveness via extensive instruction-tuning experiments; and
		- Input and output first approach
	- (3) we release a large synthetic dataset of 52K instructions and a set of manuallywritten novel tasks for building and evaluating future instruction-following models.
---
### Secondary Contribution
- “Data size. SELF-INSTRUCT provides a way to grow instruction data at a low cost with almost no human labeling” (Wang et al., 2023, p. 7)
---
### Limitations/Future Work
- 
---
### Notes (Try to use backlinks)
- “instruction-tuned” language models -> finetuned to respond to instructions
- collecting such instruction data is costly and often suffers limited diversity given that most human generations tend to be popular NLP tasks
- ![[2023_Self_Instruct_pipeline.png]]
- 175 seed set of manually-written tasks that are used to guide the overall generation
	- the model is prompted to generate instructions for new tasks
	- Given the newlygenerated set of instructions, the framework also creates input-output instances for them, which can be later used for supervising the instruction tuning
- 
- ![[2023_Self_Instruct_generated_tasks.png]]
- The results indicate that GPT3SELF-INST outperforms [[GPT3]] (the original model) by a large margin (+33.1%) and nearly matches the performance of [[InstructGPT]]
- We concatenate the instruction and instance input as a prompt and train the model to generate the instance output in a standard supervised way. To make the model robust to different formats, we use multiple templates to encode the instruction and instance input together” (Wang et al., 2023, p. 4)
- ![[2023_Self_Instruct_prompt_root_verbs.png]]
- We further study how the generated instructions differ from the seed instructions used to prompt the generation. For each generated instruction, we compute its highest ROUGE-L overlap with the 175 seed instructions.
	- The results indicate a decent number of new instructions were generated, which do not have much overlap with the seeds.
- To investigate this, we randomly sample 200 instructions and randomly select 1 instance per instruction. We asked an expert annotator (author of this work) to label whether each instance is correct or not, in terms of the instruction, the instance input, and the instance output.
- “For our SUPERNIexperiments in §4.3, we only compare with their text-davinci-001 engine, because their newer engines are trained with the latest user data and are likely to have already seen the SUPERNItest set.” (Wang et al., 2023, p. 6)
- Compared with other models that are not specifically trained for SUPERNI, GPT3SELF-INST achieves better performance than T0 or the GPT3 finetuned on the T0 training set, which takes tremendous human labeling efforts.
- we see consistent improvement as we grow the data size. However, this improvement almost plateaus after 16K. This is inline with the data scaling experiments in Wang et al. (2022, Fig. 5). Interestingly, when evaluating on SUPERNIwe found the model’s performance gain plateaus earlier at around hundreds of instructions.
---
