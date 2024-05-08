### Reflexion: Language Agents with Verbal Reinforcement Learning
---
- [Zotero Select Link](zotero://select/groups/2480461/items/R2QSBN8Z)
- [Zotero URI](https://www.zotero.org/groups/2480461/items/R2QSBN8Z)
- Authors: [[Noah Shinn]] [[Shunyu Yao]] 
- Topics: [[nlp_llm]] [[nlp_agent]] [[nlp_agent_feedback]]
- Venue: #arxiv
- Year: #2023

---
### Major Contributions
- “We propose [[Reflexion]], a novel framework to reinforce language agents not by updating weights, but instead through linguistic feedback. Concretely, [[Reflexion]] agents verbally reflect on task feedback signals, then maintain their own reflective text in an episodic memory buffer to induce better decision-making in subsequent trials. [[Reflexion]] is flexible enough to incorporate various types (scalar values or free-form language) and sources (external or internally simulated) of feedback signals, and obtains significant improvements over a baseline agent across diverse tasks (sequential decision-making, coding, language reasoning)” (Shinn et al., 2023, p. 1)
	- “We explore three ways for doing this – simple binary environment feedback, pre-defined heuristics for common failure cases, and self-evaluation such as binary classification using LLMs (decision-making) or self-written unit tests (programming).” (Shinn et al., 2023, p. 2)
	- [Github](https://github.com/noahshinn024/reflexion.)
---
### Secondary Contribution
- 
---
### Limitations/Future Work
- “At its core, Reflexion is an optimization technique that uses natural language to do policy optimization. Policy optimization is a powerful approach to improve action choice through experience, but it may still succumb to non-optimal local minima solutions. In this study, we limit long-term memory to a sliding window with maximum capacity, but we encourage future work to extend the memory component of Reflexion with more advanced structures such as vector embedding databases or traditional SQL databases” (Shinn et al., 2023, p. 9)
---
### Notes (Try to use backlinks)
- “we propose an alternative approach called Reflexion that uses verbal reinforcement to help agents learn from prior failings. Reflexion converts binary or scalar feedback from the environment into verbal feedback in the form of a textual summary, which is then added as additional context for the LLM agent in the next episode.” (Shinn et al., 2023, p. 2)
	- “This self-reflective feedback acts as a ‘semantic’ gradient signal by providing the agent with a concrete direction to improve upon, helping it learn from prior mistakes to perform better on the task. This is akin to how humans iteratively learn to accomplish complex tasks in a few-shot manner – by reflecting on their previous failures in order to form an improved plan of attack for the next attempt” (Shinn et al., 2023, p. 2)
	- “We explore three ways for doing this – simple binary environment feedback, pre-defined heuristics for common failure cases, and self-evaluation such as binary classification using LLMs (decision-making) or self-written unit tests (programming).” (Shinn et al., 2023, p. 2)
- “we show that several of these concepts can be enhanced with self-reflection to build a persisting memory of self-reflective experiences which allows an agent to identify its own errors and self-suggest lessons to learn from its mistakes over time.” (Shinn et al., 2023, p. 3)
- “We develop a modular formulation for Reflexion, utilizing three distinct models: an Actor, denoted as Ma, which generates text and actions; an Evaluator model, represented by Me, that scores the outputs produced by Ma; and a Self-Reflection model, denoted as Msr, which generates verbal reinforcement cues to assist the Actor in self-improvement.” (Shinn et al., 2023, p. 3)
- ![[2023_Reflexion_diagram_algorithm.png]]
	- “**Actor** The Actor is built upon a large language model (LLM) that is specifically prompted to generate the necessary text and actions conditioned on the state observations. Analogous to traditional policy-based RL setups, we sample an action or generation, at, from the current policy πθ at time t, receive an observation from the environment ot.” (Shinn et al., 2023, p. 4)
	- “**Evaluator** The Evaluator component of the Reflexion framework plays a crucial role in assessing the quality of the generated outputs produced by the Actor. It takes as input a generated trajectory and computes a reward score that reflects its performance within the given task context” (Shinn et al., 2023, p. 4)
	- “**Self-reflection** The Self-Reflection model instantiated as an LLM, plays a crucial role in the Reflexion framework by generating verbal self-reflections to provide valuable feedback for future trials. Given a sparse reward signal, such as a binary success status (success/fail), the current trajectory, and its persistent memory mem, the self-reflection model generates nuanced and specific feedback.” (Shinn et al., 2023, p. 4)
	- “**Memory Core components** of the Reflexion process are the notion of short-term and long-term memory. At inference time, the Actor conditions its decisions on short and long-term memory, similar to the way that humans remember fine-grain recent details while also recalling distilled important experiences from long-term memory” (Shinn et al., 2023, p. 4)
	- “**The Reflexion process** Reflexion is formalized as an iterative optimization process in 1. In the first trial, the Actor produces a trajectory τ0 by interacting with the environment. The Evaluator then produces a score r0 which is computed as rt = Me(τ0). rt is only a scalar reward for trial t that improves as task-specific performance increases. After the first trial, to amplify r0 to a feedback form that can be used for improvement by an LLM, the Self-Reflection model analyzes the set of {τ0, r0} to produce a summary sr0 which is stored in the memory mem. srt is a verbal experience feedback for trial t.” (Shinn et al., 2023, p. 5)
- “We challenge an agent to perform search-based question answering on HotPotQA [28], multi-step tasks in common household environments in AlfWorld [24], and code writing tasks in competition-like environments with interpreters and compilers in HumanEval [6], MBPP [2], and LeetcodeHard” (Shinn et al., 2023, p. 5)
- “To avoid very long prompt windows that may exceed the maximum limit, we truncate the agent’s memory to the last 3 self-reflections (experiences).” (Shinn et al., 2023, p. 5)
- “There are two main cases in which long-term memory helps an agent in AlfWorld: 1) An early mistake in a long trajectory can be easily identified. The agent can suggest a new action choice or even a new long-term plan. 2) There are too many surfaces/containers to check for an item. The agent can exploit its experience memory over several trials to thoroughly search a room.” (Shinn et al., 2023, p. 6)
- “reinforcement learning has suffered from its black-box policy and optimization setups in which interpretability and alignment have been challenging. Our proposed “verbal” reinforcement learning might address some of the issues and turn autonomous agents more interpretable and diagnosable.” (Shinn et al., 2023, p. 9)
---
