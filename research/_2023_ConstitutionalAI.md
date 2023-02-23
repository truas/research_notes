### Constitutional AI: Harmlessness from AI Feedback
---
- [Zotero Select Link](zotero://select/groups/2480461/items/9ZGXN94S)
- [Zotero URI](https://www.zotero.org/groups/2480461/items/9ZGXN94S)
- Authors: [[Yuntao Bai]]  [[Jared Kaplan]] 
- Topics: [[nlp_ethics]]  [[nlp_ai_assistant]]
- Venue: #arxiv #Anthropic
- Year: #2023

---
### Major Contributions
- We experiment with methods for training a harmless AI assistant through selfimprovement, without any human labels identifying harmful outputs. The only human oversight is provided through a list of rules or principles, and so we refer to the method as **Constitutional AI**.
	- In the RL phase, we sample from the finetuned model, use a model to evaluate which of the two samples is better, and then train a preference model from this dataset of AI preferences
- One of our goals in this work is to train a helpful and harmless assistant that is never evasive, in order to reduce the tension between helpfulness and harmlessness
- We find that as language model capabilities improve, AI identification of harms improves significantly. Furthermore, chain-of-thought reasoning improves this ability, and leads to evaluations that are becoming competitive with preference models trained on human feedback labels (see Figure 4).
- We show that model-generated critiques and revisions can be applied repeatedly to progressively reduce harmfulness (see Figure 5). Generating critiques improves harmlessness compared to simply generating revisions directly (Figure 7). 
- We use this method to specifically address the evasiveness of our prior human feedback based model [Bai et al., 2022]. • Using self-supervised preference labels for RL further improves model behavior as evaluated by crowdworkers (see Figures 2 and 3), equaling or exceeding the performance when using human feedback to evaluate harmlessness.
---
### Secondary Contribution
- 
---
### Limitations/Future Work
- 
---
### Notes (Try to use backlinks)
- [[Reinforcement Learning from AI Feedback|RLAIF]] ; [[Constitutional AI|CAI]]  ; [[Reinforcement Learning from Human Feedback|RLHF]] ; 
- [GitHub repository](https://github.com/anthropics/ConstitutionalHarmlessnessPaper)
- AI systems can already perform some tasks at or beyond human level (e.g. [Silver et al., 2017]), and over time more examples are likely to emerge. We need to develop methods now that can provide oversight for these powerful AI systems, and scaling supervision may be one possibility, if the capability level of the supervisor can scale proportionally with the capabilities of the actor, and the supervisor remains aligned with our intended goals and constraints.
- [[Reinforcement Learning from Human Feedback]]
	- We hope to improve this situation in three ways: (1) by literally encoding the training goals in a simple list of natural language instructions or principles, (2) by using chain-of-thought reasoning [Nye et al., 2021, Wei et al., 2022] to make AI decision making explicit during training, and (3) by training AI assistants that explain why they are declining to engage with harmful requests
- We chose the term ‘constitutional’ because we are able to train less harmful systems entirely through the specification of a short list of principles or instructions, i.e. a constitution. But we are also employing this terminology to emphasize that when developing and deploying a general AI system
- we evaluate whether language models can correctly identify the most helpful, honest, and harmless response in a conversation. The results suggest that large language models may already be approaching the performance of crowdworkers in identifying and assessing harmful behavior, and so motivate using AI feedbac
- ![[2023_ConstitutionalAI_architecture.png]]
---
