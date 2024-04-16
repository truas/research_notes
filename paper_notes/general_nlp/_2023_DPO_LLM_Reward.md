### Direct Preference Optimization: Your Language Model is Secretly a Reward Model
---
- [Zotero Select Link](zotero://select/groups/2480461/items/SIX6WRN8)
- [Zotero URI](https://www.zotero.org/groups/2480461/items/SIX6WRN8)
- Authors: [[Rafael Rafailov]] [[Chelsea Finn]] [[Eric Mitchell]] [[Christopher Manning]] 
- Topics: [[nlp_architecture]] [[nlp_llm]]
- Venue: #arxiv
- Year: #2023

---
### Major Contributions
- we leverage a mapping between reward functions and optimal policies to show that this constrained reward maximization problem can be optimized exactly with a single stage of policy training, essentially solving a classification problem on the human preference data. The resulting algorithm, which we call [[Direct Preference Optimization ||DPO]]
- we show how to directly optimize a language model to adhere to human preferences, without explicit reward modeling or reinforcement learning. We propose Direct Preference Optimization (DPO), an algorithm that implicitly optimizes the same objective as existing RLHF algorithms (reward maximization with a KL-divergence constraint) but is simple to implement and straightforward to train.
- “Intuitively, the DPO update increases the relative log probability of preferred to dispreferred responses, but it incorporates a dynamic, per-example importance weight that prevents the model degeneration that we find occurs with a naive probability ratio objective. Like existing algorithms, DPO relies on a theoretical preference model (such as the Bradley-Terry model; [5]) that measures how well a given reward function aligns with empirical preference data. However, while existing methods use the preference model to define a preference loss to train a reward model and then train a policy that optimizes the learned reward model, **[[DPO]] uses a change of variables to define the preference loss as a function of the policy directly.** Given a dataset of human preferences over model responses, [[DPO]] can therefore optimize a policy using a simple binary cross entropy objective, without explicitly learning a reward function or sampling from the policy during training.” (Rafailov et al., 2023, p. 2)
	- Our experiments show that DPO is at least as effective as existing methods, including PPO-based RLHF, for learning from preferences in tasks such as sentiment modulation, summarization, and dialogue, using language models with up to 6B parameters.
---
### Secondary Contribution
- 
---
### Limitations/Future Work
- 
---
### Notes (Try to use backlinks)
- LLM precise control of their behavior is difficult due to the completely unsupervised nature of their training.
- while we may want our AI coding assistant to understand common programming mistakes in order to correct them, nevertheless, when generating code, we would like to bias our model toward the (potentially rare) high-quality coding ability present in its training data.
- selecting the model’s desired responses and behavior from its very wide knowledge and abilities is crucial to building AI systems that are safe, performant, and controllable
- While the most straightforward approach to preference learning is supervised fine-tuning on human demonstrations of high quality responses, the most successful class of methods is reinforcement learning from human (or AI) feedback (RLHF/RLAIF; [12, 2]).
- In the absence of absolute rewards, theoretical analysis of CDBs substitutes the notion of an optimal policy with a von Neumann winner, a policy whose expected win rate against any other policy is at least 50% [14].
- our goal is to derive a simple approach for policy optimization using preferences directly. Our approach bypasses the reward modeling step and directly optimizes a language model using preference data.
	- key insight is to leverage an analytical mapping from reward functions to optimal policies, which enables us to transform a loss function over reward functions into a loss function over policies
- DPO identifies a mapping between language model policies and reward functions that enables training a language model to satisfy human preferences directly, with a simple cross-entropy loss, without reinforcement learning or loss of generality. With virtually no tuning of hyperparameters, DPO performs similarly or better than existing RLHF algorithms, including those based on PPO; DPO thus meaningfully reduces the barrier to training more language models from human preferences
- ![[2023_DPO_LLM_Reward_comparison.png]]
- DPO optimizes for human preferences while avoiding reinforcement learning. Existing methods for fine-tuning language models with human feedback first fit a reward model to a dataset of prompts and human preferences over pairs of responses, and then use RL to find a policy that maximizes the learned reward. In contrast, DPO directly optimizes for the policy best satisfying the preferences with a simple classification objective, without an explicit reward function or RL.
---
