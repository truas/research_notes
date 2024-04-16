### Unleashing the Emergent Cognitive Synergy in Large Language Models: A Task-Solving Agent through Multi-Persona Self-Collaboration
---
- [Zotero Select Link](zotero://select/groups/2480461/items/L7STFJ5Y)
- [Zotero URI](https://www.zotero.org/groups/2480461/items/L7STFJ5Y)
- Authors: [[Zhenhailong Wang]]  [[Heng Ji]] 
- Topics: [[nlp_llm]] [[nlp_agent]] [[nlp_persona]]
- Venue: #arxiv
- Year: #2024

---
### Major Contributions
- we propose Solo Performance Prompting (SPP), which transforms a single LLM into a cognitive synergist by engaging in multi-turn self-collaboration with multiple personas.
	- A cognitive synergist is an intelligent agent that collaboratively combines multiple minds’ strengths and knowledge to enhance problem-solving in complex tasks.
	- assigning multiple fine-grained personas in LLMs improves problem-solving abilities compared to using a single or fixed number of personas.
	- [Link](https://github.com/MikeWangWZHL/Solo-Performance-Prompting)
- we aim to create a cognitive synergist based on a single LLM that can "split into" multiple personas and engage in self-collaboration to solve both knowledge-intensive and reasoning intensive tasks.
- “This idea is heavily inspired by the role of pretend play (Piaget, 1954; Pellegrini, 2009) in cognitive development and recent findings that assigning personas (Deshpande et al., 2023; Xu et al., 2023) to LLMs can elicit specific behaviors, improve answer quality, and potentially build an AI society (Park et al., 2023; Schick et al., 2022; Li et al., 2023; Cai et al., 2023) with collaborative LLM agents.” (Wang et al., 2024, p. 2)
---
### Secondary Contribution
- LLMs can effectively identify useful personas in a zero-shot manner.
- “We further investigate whether a detailed profile for each persona is needed for eliciting domain knowledge, as suggested by (Xu et al., 2023). To this end, we design a variant of SPP, SPP-Profile, which involves generating profiles for each persona during the Persona Identification phase.” (Wang et al., 2024, p. 8)
	- “The results in Figure 7b show that SPP-Profile does not outperform SPP. This suggests that a fine-grained persona name without a detailed description may already be sufficient for eliciting certain domain knowledge.” (Wang et al., 2024, p. 8)
- (1) SPP consistently outperforms SPP-Fixed-Persona across all tasks, suggesting that dynamic, fine-grained personas are more effective than fixed, general personas. Qualitative examples in Figure 8 and 13 shows that the fine-grained personas such as "Film Expert" and "Sports Enthusiast" correctly provide the answers, while the fixed persona "Expert" fails. (2) SPP-Fixed-Persona also suffers from the early-termination problem as defined in §3.4, where the LLM stops collaboration before providing the final answer as if it were waiting for external inputs.
- “s shown in Figure 9, we observe that (1) Adding the second example, which requires collaboration of more than two personas, effectively boosts the performance. (2) SPP is fairly robust to the prompt change and show good performance with only the first demo example.” (Wang et al., 2024, p. 8)
---
### Limitations/Future Work
- 
---
### Notes (Try to use backlinks)
- “they still encounter challenges (Qin et al., 2023; Bang et al., 2023; OpenAI, 2023b; Bubeck et al., 2023) in various knowledgeintensive and reasoning-intensive tasks due to factual hallucination (Maynez et al., 2020) and a lack of slow-thinking (Sloman, 1996) capabilities.” (Wang et al., 2024, p. 1)
- different cognitive processes and individuals (referred to as cognitive synergy (Cur ̧ seu et al., 2015; Goertzel, 2009, 2017)), current LLMs are akin to "jack-of-alltrades" with a vast mixture of knowledge and characteristics.
- “We introduce Solo Performance Prompting (SPP), which simulates multi-agent, multipersona collaboration in a pure zero-shot manner.” (Wang et al., 2024, p. 3)
- “We evaluate SPP across three challenging tasks: Trivia Creative Writing, Codenames Collaborative and Logic Grid Puzzle,” (Wang et al., 2024, p. 3)
- “We present an intriguing finding regarding the emergent nature of cognitive synergy ability in LLMs, which only emerges in GPT-4” (Wang et al., 2024, p. 3)
- “We conduct in-depth analyses of the impact of the identified personas and SPP prompt design, providing insights into why dynamic, fine-grained personas are necessary, as opposed to fixed, coarse-grained personas.” (Wang et al., 2024, p. 3)
- **Solo Performance Prompting (SPP)** which instructs a LLM to perform the following the procedure for general task-solving: **(1) Persona Identification:** Identify multiple participants with special personas (including a leader persona: AI Assistant) that are essential for solving the particular task. **(2) Brainstorming:** The participants share knowledge and provide suggestions on how to approach the task based on their own expertise. **(3) Multi-Persona Iterative Collaboration:** The leader persona, AI Assistant, proposes initial solutions, consults the other participants for feedback, and revise the answer iteratively.
- “To our knowledge, SPP is the first zero-shot prompting method that can enhance both knowledge and reasoning abilities on GPT-4” (Wang et al., 2024, p. 7)

- ![[2024_LLM_Cognitive_Synergy_prompting_schemes.png]]
- ![[2024_LLM_Congnitive_Synergy_results_fixed_persona.png]]
---
