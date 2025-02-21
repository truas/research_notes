### Evil Geniuses: Delving into the Safety of LLM-based Agents

- [Link](https://arxiv.org/pdf/2311.11855)
- Authors: [[(A) Yu Tian]] [[(A) Hang Su]]
- Topics: [[multi-agent]] [[jailbreaking]] [[ai_safety]]
- Venue: #arxiv
- Year: #y2023
- Read: 2025-02-21

**Short Summary:**
The paper assesses the safety of LLM-based agents from three perspectives: agent quantity, role definition, and attack level.

---
### Contributions

- Evil Geniuses
	- an attack method to autonomously generate jailbreak prompts for LLM-based agents
		- Uses Red-Blue exercises to enhance the aggressiveness and authenticity of the generated prompts relative to original roles
- Agents are less robust, prone to more harmful behaviors, and capable of generating stealthier content than LLMs
	- success rate of harmful behaviors increases with the number of agents
	- higher attack levels correlate with increased success rates
	- Reasons:
		- domino effect triggered by multi-agent interactions
		- the use of sophisticated, flexible tools

---
### Summary of Strengths

- The paper covers a notable research gap, claiming to be the first to investigate jailbreaking with (multi-)agents
- Ablation shows that with the absence of collaborative dialogue among agents, the model’s ability to effectively modify the generated prompt is significantly hindered
- The paper nicely investigates the individual parameters of agent setups regarding their vulnerability (e.g., agent quantity, roles, attack level) while keeping other parameters fixed
- The paper gives three interesting directions for mitigation (role-based filter, alignment training, multimodal content-filtering) for discussion which provides valuable ressource for future work.

---
### Summary of Weaknesses

- The paper could investigate the reasons for the increased vulnerability of mmulti-agent systems more deeply. Currently, most reasons are given by discussion (e.g., domino effect).
	- The study could have included different types of jailbreaking methods
	- Human assessment (e.g., qualitative examples or human study) could give insights into the ongoing of discussions and what lead to the final collapse of multi-agent safety.
	- It would have been nice to see more concrete examples of multi-agent discussions for the claims threatening, stealthy, and domino effect. especially figure 4 and 5 concentrate on the harmful result, but not the actual discussion that lead to the issue.
- No limitations section

---
### Limitations/Future Work

- develop a multi-agent training framework that is closely aligned with human values
- mitigation: role-based filter, alignment training, multimodal content-filtering
- No limitations section

---
### Notes

- LLM-based agents are susceptible to exploitation by attackers, who could potentially use them to launch attacks on other LLMs.
- extent of influence exerted by an agent is directly proportional to its hierarchical level within the system
- stealthy: modalities
- threatening: execution processes
- domino effect: iterative processing, decomposition of hamrful tasks into semi-harmful subtasks

---
### Important Figures

![[2025_EvilGeniuses.png]]