### Meta-Prompting: Enhancing Language Models with Task-Agnostic Scaffolding
---
- [Zotero Select Link](zotero://select/groups/2480461/items/RMVK73HK)
- [Zotero URI](https://www.zotero.org/groups/2480461/items/RMVK73HK)
- Authors:  [[Mirac Suzgun]] [[Adam Tauman Kalai]] 
- Topics: [[nlp_prompt]] [[nlp_llm]] [[nlp_agent]]
- Venue: #arxiv #stanford
- Year: #2024

---
### Major Contributions
- meta-prompting, an effective scaffolding technique designed to enhance the functionality of language models (LMs). This approach transforms a single LM into a multi-faceted conductor, adept at managing and integrating multiple independent LM queries
	- [Github](https://github.com/suzgunmirac/meta-prompting.)
	- The zero-shot, task-agnostic nature of meta-prompting greatly simplifies user interaction by obviating the need for detailed, task-specific instructions
	- hrough rigorous experimentation with GPT-4, we establish the superiority of meta-prompting over conventional scaffolding methods: When averaged across all tasks, including the Game of 24, Checkmate-in-One, and Python Programming Puzzles
- Meta-Prompt - It involves constructing a high-level “meta” prompt that instructs an LM to: (i) break down complex tasks or problems into smaller, manageable pieces; (ii) assign these pieces to specialized “expert” models with proper and detailed natural-language instructions; (iii) oversee the communication between these expert models; and (iv) apply its own critical thinking, reasoning, and verification skills throughout the process.
- The core contribution of this work is the introduction of a task-agnostic scaffolding system that leverages a single LM. This LM not only carries forward the thread of the task but also dynamically selects and instructs expert models appropriate for each specific task.
---
### Secondary Contribution
- Our proposed meta-prompting technique combines and expands upon various prompting ideas introduced by recent studies—including, high-level planning and decision-making (Yao et al., 2023b; Sun et al., 2023; Hao et al., 2023a), dynamic persona assignment (Xu et al., 2023; Wang et al., 2023), multi-agent debating (Du et al., 2023; Zhuge et al., 2023), self-debugging and self-reflection (Schick et al., 2023b; Liu et al., 2023a; Gou et al., 2023; Madaan et al., 2023; Shinn et al., 2023).
- Our structured approach embodies the principle of the wisdom of the crowd (Suzgun et al., 2023a), which posits that a collective opinion of a diverse set of critical thinkers often surpasses the insights of individual experts.
---
### Limitations/Future Work
- Under our setup, experts can be called only by the Meta Model. They cannot directly interact or communicate with each other, though the Meta Model can choose to share some text from or combine the insights of various experts when interacting with a new expert. - How can we guarantee that no information goes from one role to another? on a Weight/data level,
- The temperature value, which usually ranges between 0 and 1, controls how much randomness or creativity the model exhibits. Ideally, a temperature of 0 should lead to the model producing the same output when presented with the same input. However, both GPT-3.5 and GPT-4 have shown a tendency to generate varied responses even at this setting. This means that reproducing our exact results might be challenging under identical experimental conditions. To address this issue, we are releasing all model inputs, interactions, and outputs in our GitHub repository.
- A primary limitation is the elevated cost associated with multiple model calls. In our setup using GPT-4, the dual role of the Meta Model and the experts, distinguished by unique instructions, incurs substantial costs under the GPT-4 API pricing model.
- “A practical challenge faced is the Meta Model’s occasional oversight in conveying necessary information to experts, forgetting that experts can only access data adhering to a certain format (within triple quotes in our system). This oversight can lead to unintended confusion and underscores the need for improved information management” (Suzgun and Kalai, 2024, p. 13)
---
### Notes (Try to use backlinks)
- This approach allows for a single, uniform LM to maintain a coherent line of reasoning while also tapping into a variety of expert roles. The use of dynamically selected contexts for prompting these experts introduces fresh perspectives into the process, while the conductor model retains a bird’s-eye view of the entire history and coordination.
	- A key aspect of meta-prompting is its task-agnostic nature. Unlike traditional scaffolding methods that require specific instructions or examples tailored to each task, metaprompting employs the same set of high-level instructions across various tasks and inputs. This universality is particularly beneficial for users who might find it cumbersome to provide detailed examples or specific guidance for every distinct task.
- Our findings reveal that meta-prompting not only enhances overall performance but often leads to state-of-the-art results across a diverse range of tasks.
- Multi-persona prompting (Du et al., 2023): Also known as solo-performance prompting (SPP), this method instructs an LM to perform the following: (i) Propose a small ensemble of “personas” to address the specific task or problem at hand; (ii) let these personas engage in a collective dialogue, collaboratively generating potential solutions while extending feedback to one another and refining their answers; and (iii) synthesize all the available information and deliver a final response
- The success of our meta-prompting framework lies partly in its strategic use of specialized knowledge, self collaboration, and implicit verification loops
- Enhancing Solution Reliability through Systematic Verification. The Meta Model’s systematic verification protocol strengthens the reliability and robustness of its solutions. Fundamental to this approach is the consistent practice of consulting an expert for validation before finalizing responses, a principle applied across diverse tasks.
- Limited Performance Improvement with GPT-3.5. In comparison to GPT-4, GPT-3.5 demonstrates a more limited scope of performance enhancement across various tasks. Although it shows notable improvements in specific tasks such as Sonnet Writing and Checkmate-in-One, its capabilities do not consistently surpass baseline standards or zero-shot CoT prompting methods in other tasks, notably Word Sorting and Multiple Arithmetic Two.
	- Our qualitative analysis suggests that GPT-3.5 may not be as effective as GPT-4 in simulating role-playing scenarios or managing extended context windows.
- LMs process complex queries
	- “The chain-of-thought (CoT) prompting (Wei et al., 2022b) and its variants—including least-to-most (Zhou et al., 2023), zero-shot CoT (Kojima et al., 2022), self-ask (Press et al., 2022), ask-me-anything (Arora et al., 2023), decomposed prompting (Khot et al., 2023), and auto-CoT (Zhang et al., 2023d)” (Suzgun and Kalai, 2024, p. 13)
- Reasoning LLMS
	- More recent innovations such Tree-of-Thought (Yao et al., 2023a), Graph-of-Thought (Besta et al., 2023), Program-of-Thought (Chen et al., 2023d), and Skeleton-of-Thought (Ning et al., 2023), have further enriched this domain; these explore dynamic, non-linear reasoning pathways, broadening the computational and heuristic capabilities of LMs.
- Role Playing/Personas
	- Recent studies (Park et al., 2022, 2023; Li et al., 2023; Xu et al., 2023; Fu et al., 2023a; Deshpande et al., 2023) have shown that endowing instruction-following LMs with “expert” personas or roles enhances the quality and accuracy of their output. In particular, approaches like CAMEL (Li et al., 2023) and Expert Prompting (Xu et al., 2023), which involve dynamically assigning personas to a single LM, have been shown to yield higher quality and more reliable responses than models without designated personas.
- In this work, we have introduced and examined meta-prompting, a simple yet powerful scaffolding technique that enhances the performance of language models in a task-agnostic manner. This approach leverages a language model to act as both a central conductor and a group of expert instances, thereby endowing traditional models with dynamic, multi-functional capabilities.
---
