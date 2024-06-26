### Simulating Opinion Dynamics with Networks of LLM-based Agents
---
- [Zotero Select Link](zotero://select/groups/5566776/items/6JRUYR8T)
- [Zotero URI](https://www.zotero.org/groups/5566776/items/6JRUYR8T)
- Authors: [[Yun-Shiuan Chuang]] [[Important Author]] [[Timothy T. Rogers]] 
- Topics: [[nlp_agents]]  [[nlp_llm]]
- Venue: #arxiv #NAACL
- Year: #2024

---
### Major Contributions
- We propose a new approach to simulating opinion dynamics based on populations of Large Language Models (LLMs).
- “After inducing confirmation bias through prompt engineering, however, we observed opinion fragmentation in line with existing agent-based modeling and opinion dynamics research.” (Chuang et al., 2024, p. 1)
- “This paper considers whether large language models (LLMs) can be used to support sophisticated simulation of agent interactions, potentially providing a more realistic tool for understanding opinion dynamics.” (Chuang et al., 2024, p. 2)
	- we show that LLM agents tend to converge towards denying inaccurate information, regardless of the personas they role-play, limiting their authenticity when emulating people with fact-resistant viewpoints.
- 
---
### Strengths
- The idea to introduce confirmation bias in the prompt and see the opinion shifts is valuable
- 
---
### Weakness
- The creation of personas seems a bit arbitrary
- 
---
### Notes
- ![[2024_OpinionDynamics_LLM_schematic.png]]
- “We investigate the effects of inducing a cognitive bias via role-playing instructions on the group opinion dynamics. Specifically, we consider confirmation bias: the tendency to interpret information as confirming one’s views and to discount contradictory evidence (Nickerson, 1998).” (Chuang et al., 2024, p. 5)
- Agents Converge towards the Inherent Bias in the LLM.
	- “the role-playing prompt initially causes agents to express a diverse variety of opinions as expected, but with repeated social interacts these opinions converge toward a ground-truth consensus.” (Chuang et al., 2024, p. 7)
- “Confirmation Bias Leads to Opinion Fragmentation. Introducing confirmation bias in the prompt leads to less ultimate consensus (i.e., greater diversity D) across LLM agents.” (Chuang et al., 2024, p. 8)
	- “the stronger the confirmation bias, the more diverse the final state distribution.” (Chuang et al., 2024, p. 8)
- “Impact of Initial Opinion Distribution The system’s tendency for simulated opinions to converge on ground truth prompts an intriguing question: If all agents start with false opinions, will they still converge toward a scientifically accurate consensus, or will they reinforce their initial beliefs and resist changing their stance? Figure 5 shows the evolution of opinions under various initial distributions, using the global warming topic. Regardless of the initial opinion distribution, the agents altered their expressed opinions and shifted toward the ground truth.” (Chuang et al., 2024, p. 8)
- “The Strength of Bias under False Framing is Stronger than under True Framing” (Chuang et al., 2024, p. 8)
- “Simulating Social Dynamics with LLM-based Agents” (Chuang et al., 2024, p. 9)
---
### Questions
- 
---
