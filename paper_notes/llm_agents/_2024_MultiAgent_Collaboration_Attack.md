### MultiAgent Collaboration Attack: Investigating Adversarial Attacks in Large Language Model Collaborations via Debate

- [Link](https://arxiv.org/pdf/2406.14711)
- Authors: [[(A) Alfonso Amayuelas]] [[(A) William Wang]]
- Topics: [[ai_safety]] [[multi-agent]]]
- Venue: #arxiv
- Year: #y0000
- Read: 2025-02-24

**Short Summary:**
This paper evaluates the behavior of multi-agent debate if a single agent is an adversary.

---
### Contributions

- Collaboration via debate is usually vulnerable to an adversary through persuasion
- Model’s persuasiveness is an important ability to attack the collaborative setting
- More agents or rounds does not increase recovery

---
### Summary of Strengths

- The paper covers a relevant research gap as single agents might persuade a multi agent setup.
- The setup and explanation of metrics (e.g., persuasiveness) seems reasoably considered.
- Investigations about the number of rounds gives insights into how the ongoing multi-aggent conversation develops with and without an adversary

---
### Summary of Weaknesses

- Conversations are only going on for three turns which is little to see a trend on conversation lengths
- Figure 4 misses a baseline, i.e., three turn discussion without an adversay. One can argue that performance decreases just in general with ongoing interaction and not just because of the adversary.

---
### Limitations/Future Work

- Only investigates the issue by persuasive abilities. Other adversarial scenarios might be more stealthy but are not looked into.
-  The mitigation method (prompting) is very simple and the lack of effectiveness is expected. Future work could investigate more mitigation methods.

---
### Notes

- To simulate an adversarial attack, the adversary selects an incorrect answer and tries to persuade the other agents to accept it as correct
	- models persuasive abilities

---
### Important Figures
![[2024_PersuasiveMultiAgent.png]]