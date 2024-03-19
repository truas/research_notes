### Large Language Model based Multi-Agents: A Survey of Progress and Challenges
---
- [Zotero Select Link](zotero://select/groups/2480461/items/GQD8BLYC)
- [Zotero URI](https://www.zotero.org/groups/2480461/items/GQD8BLYC)
- Authors: [[Taicheng Guo]] [[Olaf Wiest]] [[Xiangliang Zhang]] 
- Topics: [[nlp_agent]] [[nlp_llm]] [[nlp_survey]]
- Venue: #arxiv
- Year: #2024

---
### Major Contributions
- “Our goal is for readers to gain substantial insights on the following questions: What domains and environments do LLM-based multi-agents simulate? How are these agents profiled and how do they communicate? What mechanisms contribute to the growth of agents’ capacities?” (Guo et al., 2024, p. 1)
- [Link](https://github.com/taichengguo/LLM_MultiAgents_Survey_Papers)
- 
---
### Secondary Contribution
- “Timely survey papers systematically summarize the progress of LLM-based agents, as seen in works [Xi et al., 2023; Wang et al., 2023b].” (Guo et al., 2024, p. 1)
- List of possible opportunities:
	- Multi-modal environment
	- Addressing hallucination
	- Collective intelligence
	- Scaling up LLM systems
	- (our) MALLM structure/framework
	- Evaluation and benchmarks
		- “there is a notable shortfall in the development of comprehensive benchmarks across several research domains, such as Science Team for Experiment Operations, Economic analysis, and Disease propagation simulation.” (Guo et al., 2024, p. 11)
		- “much of the existing research focuses on evaluating individual agents’ understanding and reasoning within narrowly defined scenarios.” (Guo et al., 2024, p. 11)
	- (ours) standard tasks/eval
	- 
---
### Limitations/Future Work
- The initial architecture/outline seemed promising, but they focus too much on the applications
	- Some don't even use LLMs (double check)
---
### Notes (Try to use backlinks)
- “Compared to systems using a single LLM-powered agent, multi-agent systems offer advanced capabilities by 1) specializing LLMs into various distinct agents, each with different capabilities, and 2) enabling interactions among these diverse agents to simulate complex real-world environments effectively.” (Guo et al., 2024, p. 1)
- “Single-Agent systems empowered by LLMs have shown inspiring cognitive abilities [Sumers et al., 2023]. The construction of such systems concentrates on formulating their internal mechanisms and interactions with the external environment. Conversely, LLM-MA systems emphasize diverse agent profiles, inter-agent interactions, and collective decision-making processes.” (Guo et al., 2024, p. 3)
- “Agents Profiling In LLM-MA systems, agents are defined by their traits, actions, and skills, which are tailored to meet specific goals. Across various systems, agents assume distinct roles, each with comprehensive descriptions encompassing characteristics, capabilities, behaviors, and constraints.” (Guo et al., 2024, p. 3)
	- “Regarding the Agent Profiling Methods, we categorized them into three types: Pre-defined, Model-Generated, and data derived” (Guo et al., 2024, p. 3)
		- “Pre-defined cases, agent profiles are explicitly defined by the system designers. The ModelGenerated method creates agent profiles by models, e.g., large language models. The Data-Derived method involves constructing agent profiles based on pre-existing datasets” (Guo et al., 2024, p. 4)
- Agent Communication
	- “1) Communication Paradigms: the styles and methods of interaction between agents; 2) Communication Structure: the organization and architecture of communication networks within the multi-agent system; and 3) Communication Content exchanged between agents.” (Guo et al., 2024, p. 4)
		- “Communication Paradigms: Current LLM-MA systems mainly take three paradigms for communication: Cooperative, Debate, and Competitive.” (Guo et al., 2024, p. 4)
		- Communication Structure: 
			- “**Layered communication** is structured hierarchically, with agents at each level having distinct roles and primarily interacting within their layer or with adjacent layers.” (Guo et al., 2024, p. 4)
			- “**Decentralized communication** operates on a peer-to-peer network, where agents directly communicate with each other, a structure commonly employed in world simulation applications. ” (Guo et al., 2024, p. 4)
			- "**Centralized communication** involves a central agent or a group of central agents coordinating the system’s communication, with other agents primarily interacting through this central node. 
			- **Shared Message Pool** is proposed by MetaGPT [Hong et al., 2023] to improve the communication efficiency. This communication structure maintains a shared message pool where agents publish messages and subscribe to relevant messages based on their profile” (Guo et al., 2024, p. 5)
		- “Communication Content: In LLM-MA systems, the Communication Content typically takes the form of text.” (Guo et al., 2024, p. 5)
	- “Agents Capabilities Acquisition” (Guo et al., 2024, p. 5) “two fundamental concepts: the types of feedback from which agents should learn to enhance their capabilities, and the strategies for agents to adjust themselves to effectively solve complex problems” (Guo et al., 2024, p. 5)
	- “4.1.4 Science Debate LLM-MA can be set for science debating scenarios, where agents debate with each other to enhance the collective reasoning capabilities in tasks such as Massive Multitask Language Understanding (MMLU) [Hendrycks et al., 2020], Math problems [Cobbe et al., 2021], and StrategyQA [Geva et al., 2021]. The main idea is that each agent initially offers its own analysis of a problem, which is then followed by a joint debating process. Through multiple rounds of debate, the agents converge on a single, consensus answer. [Du et al., 2023] leverages the multi-agents debate process on a set of six different reasoning and factual accuracy tasks and demonstrates that LLM-MA debating can improve factuality.” (Guo et al., 2024, p. 7)
- “Multi-Agents Framework We provide a detailed introduction to three open-source multi-agent frameworks: MetaGPT [Hong et al., 2023], CAMEL [Li et al., 2023b], and Autogen [Wu et al., 2023a]” (Guo et al., 2024, p. 10)
	- “MetaGPT is designed to embed human workflow processes into the operation of language model agents, thereby reducing the hallucination problem that often arises in complex tasks.” (Guo et al., 2024, p. 10)
	- "CAMEL, or Communicative Agent Framework, is oriented towards facilitating autonomous cooperation among agents.” (Guo et al., 2024, p. 10)
	- “AutoGen is a versatile framework that allows for the creation of applications using language models. It is distinctive for its high level of customization, enabling developers to program agents using both natural language and code to define how these agents interact.” (Guo et al., 2024, p. 10)
- ![[2024_LLM_Agents_Survey_applications.png]]
- ![[2024_LLM_Agents_Survey_architectures.png]]
---
