### Cooperate or Collapse: Emergence of Sustainable Cooperation in a Society of LLM Agents
---
- [Zotero Select Link](zotero://select/groups/5566776/items/5UESWPA5)
- [Zotero URI](https://www.zotero.org/groups/5566776/items/5UESWPA5)
- Authors: [[Giorgio Piatti]] [[Rada Mihalcea]] 
- Topics: [[nlp_llm]] [[nlp_agents]]
- Venue: #arxiv
- Year: #_2024

---
### Major Contributions
- [GitHub](https://github.com/giorgiopiatti/GovSim)
- “We develop an LLM-based agent architecture and test it with the leading open and closed LLMs. We find that all but the most powerful LLM agents fail to achieve a sustainable equilibrium in [[GOVSIM]], with the highest survival rate below 54%.” (Piatti et al., 2024, p. 1)
	- “failure to achieve sustainable cooperation in most LLMs stems from their inability to formulate and analyze hypotheses about the long-term effects of their actions on the equilibrium of the group.” (Piatti et al., 2024, p. 1)
---
### Strengths
- We introduce [[GOVSIM]], the first common pool resource-sharing simulation platform for LLM agents. GOVSIM enables us to study and benchmark emergent sustainable behavior in LLMs.
- Using [GOVSIM], we find that only the largest and most powerful LLMs ever reach a sustainable outcome with the best agent below a 54% survival rate.” (Piatti et al., 2024, p. 2)
- We develop a more cooperatively capable agent based on the philosophical principle of universalization. Through ablation and perturbation, we characterize the boundary conditions for the emergence of sustainable cooperation. 
- We open-source our simulation framework to foster future research: the GOVSIM simulation environment, agent prompts, and a web interface.
---
### Weakness
- It is not clear if the consciousness of the agents come from the rules of the game or their discussions
- They leave out the role of a selfish agent, that tries to maximize its benefit
---
### Notes
- “However, this prior work leaves three key questions open:
	- (1) in contrast to the well-documented mechanisms that enable cooperation in people [19, 53, 54], there is limited understanding of how LLMs achieve and maintain cooperation;
	- (2) how to handle multi-turn LLM interactions that balance safety with reward maximization in multi-agent settings; and 
	- (3) the potential of using LLMs as a simulation platform for to better understand and test theories of human psychology and economic behavior.” (Piatti et al., 2024, p. 2)
- “Inspired by game-theoretic research on the evolution of cooperation [4] and “The Tragedy of the Commons,” we build GOVSIM to simulate realistic multi-party social dilemmas such as those faced by groups managing shared resources [26, 59].” (Piatti et al., 2024, p. 2)
- “Ablation studies show that communication reduces resource overuse by 21%. Using an automated analysis of agent dialogues, we show that negotiation is the main type of communication between agents and constitutes 62% of the dialogues. Finally, other subskills are also important for sustainability. The ability to form beliefs about other agents, highly correlated (0.83) with community survival time.” (Piatti et al., 2024, p. 2)
- “[[GOVSIM]], no single scalar metric can track the entire state of the system.” (Piatti et al., 2024, p. 4)
- “smaller models (such as Llama3-8B) often fail to sustainably manage any of the resources at all.” (Piatti et al., 2024, p. 5)
- “no LLM in our studies was able to sustain the resources in each of the 5 seeds across the three scenarios (survival time 12)” (Piatti et al., 2024, p. 5)
- “The basic idea of [[Universalization]] is that when assessing whether a particular moral rule or action is permissible, one should ask, “What if everybody does that?” [36].” (Piatti et al., 2024, p. 7)
- “agents without communication tend to overuse the common resource by 22% (t-test; p < 0.001). This result shows the importance of the communication phase for sustainable resources.” (Piatti et al., 2024, p. 7)
---
### Questions
- 
---
