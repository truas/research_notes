### Enhancing the General Agent Capabilities of Low-Parameter LLMs through Tuning and Multi-Branch Reasoning
---
- [Zotero Select Link](zotero://select/groups/5566776/items/WWLSWLG3)
- [Zotero URI](https://www.zotero.org/groups/5566776/items/WWLSWLG3)
- Authors: [[Qinhao Zhou]] [[Important Author]] [[Yongbin Li]] 
- Topics: [[nlp_agent]] [[nlp_llm]]
- Venue: #arxiv #NAACL
- Year: #2024


---
### Major Contributions
- “We explore the capabilities of 7B and 13B open-source LLMs as agents, exploring their potential in performing agent tasks. 
- We propose supervised fine-tuning with specific agent data as a fundamental approach to improving the capability of opensource LLMs as agents. To achieve this, we develop a method for constructing agent data.
- We find that task decomposition and backtracking are effective approaches for addressing complex agent tasks. We conduct experiments on AgentBench and achieve promising results.” (Zhou et al., 2024, p. 2)
---
### Strengths
- The  created dataset might be a good ground truth to trajectory/reasoning steps
- Repository [GitHub](https://github.com/HAIV-Lab/LLM-TMBR)
- The automatic decomposition into sub-tasks it's interesting
---
### Weakness
- Related work does not really position their work in relation to others
- The comparison/motivation between open source (low parameters) and comercial models is unfair
- The prune of non-optimal paths seems challenging to guarantee good quality
- Tasks seem rather far from models'training/data
- 4.1 is quite plan. Trivial findings and expected results: training on code, improve code abiltities and harm the others. Agent data fine tuning improves agent tasks, etc
- The ablation study is weak, using  2 paths and branches improve results, and right after it decreases it?
- The judge from the subtasks and path is not clear
- 
---
### Notes
- “Open-source pre-trained Large Language Models (LLMs) exhibit strong language understanding and generation capabilities, making them highly successful in a variety of tasks. However, when used as agents for dealing with complex problems in the real world, their performance is far inferior to large commercial models such as ChatGPT and GPT-4” (Zhou et al., 2024, p. 1)
- ![[2024_MultiBranch_LLM_overview_task.png]]
- “As agents, LLMs need to possess three fundamental capabilities: task planning, long-term memory, and tool usage.” (Zhou et al., 2024, p. 4)
- “A larger λ means that the LLMs are inclined to specific agent capabilities, whereas a small λ makes LLMs more inclined to general capabilities. We observe that deterioration of the general ability of LLMs will also decrease the agent ability, so we set a small value for λ” (Zhou et al., 2024, p. 5)
- Finetuning using  [[LoRA||Low-Rank Adaptation of Large Language Models]] [[LoRA]]
- “On the one hand, we we instruct LLMs to generate multiple available actions in each reasoning step. On the other hand, we employ a judge model to select one action from the provided set and continue the reasoning process until a final output is obtained.” (Zhou et al., 2024, p. 5)
- “Agent tasks in the real world are often complex and one single reasoning path may not yield the optimal answer. Inspired by the reflective ability in human thinking processes, we propose to take multi-path reasoning with LLMs. We call this method backtracking” (Zhou et al., 2024, p. 5)
- “It can be seen that fine-tuning on various instruction datasets has a positive effect on improving the capabilities of agents” (Zhou et al., 2024, p. 6)
---
### Questions
- Building/training agents require multi-turn dialogues? What is the difference between agentes/models trained in multi-turn?
	- “Existing work on agent fine-tuning (Zeng et al., 2023) shows that using only agent data to fine-tune LLMs compromises their generalizability.” (Zhou et al., 2024, p. 4)
- Think step by step or identify tasks? Divide and Conquer approach
- 
---
