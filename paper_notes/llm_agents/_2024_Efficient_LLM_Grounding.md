### Towards Efficient LLM Grounding for Embodied Multi-Agent Collaboration
---
- [Zotero Select Link](zotero://select/groups/5566776/items/4IQEWLHR)
- [Zotero URI](https://www.zotero.org/groups/5566776/items/4IQEWLHR)
- Authors: [[Yang Zhang]] [[Shixin Yang]] [[Xuelong Li]] 
- Topics: [[agents_reasoning]] [[nlp_agents]]
- Venue: #arxiv
- Year: #2024

---
### Major Contributions
- [Website](https://read-llm.github.io/#)
- “We provide theoretical analysis by extending advantage-weighted regression in reinforcement learning to multi-agent systems.” (Zhang et al., 2024, p. 1)
- “we propose Reinforced Advantage ([[ReAd]]) as a closed-loop feedback for LLMs in multi-agent collaboration. We provide two optional LLM-generated plan refinement scheme, including Sequential Individual Plan Refinement with the local advantage (named [[ReAd-S]]) and Joint Plan Refinement with the joint advantage (named [[ReAd-J]]).” (Zhang et al., 2024, p. 2)
	- “Among them, (i) ReAd-J evaluates the advantage function of joint actions, which requires LLMs to generate the joint planning of all agents at once. In contrast, (ii) ReAd-S evaluates the local advantages of each agent’s action by following the principle of multi-agent advantage decomposition [29] in [[MARL]], which allows LLMs to generate actions for each agent sequentially.” (Zhang et al., 2024, p. 2)
---
### Strengths
- The new proposed approaches [[ReAd]] (and variants) seem to improve query rounds and interactions between LLMs
- Engineering to improve [[Multi-Agent Reinforcement Learning||MARL]]
- 
---
### Weakness
- Motivation for their technique is somehow weak
- 
---
### Notes
- “we propose a novel framework for multi-agent collaboration that introduces Reinforced Advantage feedback (ReAd) for efficient self-refinement of plans. Specifically, we perform critic regression to learn a sequential advantage function from LLM-planned data, and then treat the LLM planner as an optimizer to generate actions that maximize the advantage function.” (Zhang et al., 2024, p. 1)
- “To prevent LLMs from outputting infeasible plans in embodied tasks, existing methods mostly design a closed-loop framework for the interaction process with feedback. Specifically, one line of research adopts self-reflection by performing self-evaluation by LLMs to improve the plan generation of LLM planner [51, 68, 21, 40]; and the other works perform physical verification by using feedback of the external environment to dynamically replan depending on unexpected feedback [26, 53]” (Zhang et al., 2024, p. 1)
---
### Questions
- 
---
