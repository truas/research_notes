### On the Resilience of LLM-Based Multi-Agent Collaboration with Faulty Agents

- [Link](https://arxiv.org/pdf/2408.00989)
- Authors: [[(A) Jen-tse Huang]] [[(A) Maarten Sap]]
- Topics: [[ai_safety]] [[multi-agent]]
- Venue: #arxiv
- Year: #y2025
- Read: 2025-02-24

**Short Summary:**
This paper investigates the resilience of LLM multi-agent discussion paradigms on various tasks by simulating faulty agents within the interaction. They improve the resilience by challenging others outputs and a reviewer agent.

---
### Contributions

- Faulty Agents:
	- AutoInject
		- automatically inject errors into messages spread among agents
	- AutoTransform
		- transforms a given agents profile into a faulty variant with stealthy errors
- Mitigation methods:
	- Challenger: adds to each agent’s profile the ability to challenge received messages
	- Inspector: extra agent who reviews and corrects messages
- hierarchical structure is most stable against faulty agents
- code generation is most affected by faulty agents
- 

---
### Summary of Strengths

- The paper tests the resilience on a broad selection of tasks and using various communication paradigms (flat, hierarchical, linear). This is well reasoned and makes the study thorough.
- While showing the issue, the paper also displays possible mitigation methods. Overall this is a strong contribution.

---
### Summary of Weaknesses

- The selection of error types is superficial and not well reasoned.
- The factt that induced errors can sometimes cause performance increase is weird and not well discussed. I would expect some more discussion on this or attribute this to noise.

---
### Limitations/Future Work

- 

---
### Notes

- They test three structures: linear, flat, hierarchical
- Tasks: code, math, text evaluation, translation
- Error types: semantic , syntactic

---
### Important Figures
- Store as `./paper_notes/\_figures/YEAR_keywords.png`