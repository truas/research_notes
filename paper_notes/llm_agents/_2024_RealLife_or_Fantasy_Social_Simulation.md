### Is this the real life? Is this just fantasy? The Misleading Success of Simulating Social Interactions With LLMs
- [Link](https://arxiv.org/pdf/2403.05020)
- Authors: [[(A) Xuhui Zhou]] [[(A) Maarten Sap]]
- Topics: [[social_simulation]] [[multi-agent]]
- Venue: #arxiv
- Year: #y2024
- Read: 2024-11-22

**Short Summary:**
They examine the differences between multi-agent simulations with LLMs and the real world (human interaction). LLMs perform better in unrealistic, omniscient simulation settings but struggle in ones that more accurately reflect real-world conditions with information asymmetry.

---
### Contributions

- Information asymmetry is key for simulating behaviour. Information assymetry hinders the success of social interaction
	- SCRIPT mode overestimates LLMs’ ability to interact in realistic settings with information asymmetry
	- SCRIPT mode ist most successfull in simulating successfull / natural behaviour
- AGENTS simulations are often overly verbose
	- finetuning agents can improve their naturalness, but not their success rate for goal completion
- SCRIPT exploits direct access to the goals of the agents it simulates, AGENTS mode struggles to generate natural interactions or achieve its goals

---
### Summary of Strengths

- Good focus in information assymetry. They clearly showcase that it has an impact on social simulations.
- Experiments investigate the characteristics of information assymetry to a reasonable degree
- RQs are well referenced during the experiments, so it is easy to follow

---
### Summary of Weaknesses

- They use GPT-4 to evaluate goal completion / success rate. But they cite a work that shows relatively high correlation with human labels for this type of evaluation specifically
- each mode could have been explained early in the work with 1-2 sentences. The explanation of modes was a little unstructured.
---
### Limitations/Future Work

- In the modes where all information is available (no assymetry), both cooperative/competitive sides might take a shortcut in the discussion which they only know from the secret. This could increase success rate, but would not be a natural simulation of real-world human behaviour.
- trade-off between successful interaction and psychological plausibility
- Future work: maintain probabilistic expectations over the mental states of conversational partners and use it to decide how to act

---
### Notes

- information asymmetry in simulations: the degree to which interlocutors in interactions have access to each other’s internal private mental states and goals
	- SCRIP, AGENT, and MIND READERS mode
- Scenarios:
	- cooperative, competitive
---
### Important Figures

- ![[2024_agents_script_modes_information_assymetry.png]]