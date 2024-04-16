### Simple Synthetic Data Reduces Sycophancy in Large Language Models
---
- [Zotero Select Link](zotero://select/groups/2480461/items/4E244HPY)
- [Zotero URI](https://www.zotero.org/groups/2480461/items/4E244HPY)
- Authors: [[Jerry Wei]] [[Quoc V. Le]] 
- Topics: [[nlp_datase]] [[nlp_LLM]]
- Venue: #arxiv
- Year: #2023

---
### Major Contributions
-  we study sycophancy across a set of base and instruction-tuned models (Chowdhery et al., 2022; Chung et al., 2022, PaLM and Flan-PaLM). We then propose a straightforward syntheticdata intervention in an additional finetuning stage that reduces this behavior
	- model scaling and instruction tuning significantly increase sycophancy for PaLM models up to 540B parameters.
	- finding that despite knowing that these statements are wrong, language models will still agree with them if the user does as well.
	- *models such as ChatGPT and Bard did not experience significant sycophancy, possibly because of their additional finetuning data or prompt preambles.*
	- [GitHub](https://github.com/google/sycophancy-intervention)
- To reduce sycophancy, we propose a simple data intervention that uses publicly-available NLP tasks to teach a model that a statement’s truthfulness is independent of a given user’s opinion.
---
### Secondary Contribution
- 
---
### Limitations/Future Work
- We only select classification-type tasks because our format requires discrete labels. For all datasets, we only used input–label pairs in the training split to create our claims.
- we set our evaluations and intervention method to follow the prompt format used in Perez et al. (2022) (i.e., “Human: [question]\nAssistant:”), so it is unclear whether our results generalize to other formats
---
### Notes (Try to use backlinks)
- **Sycophancy** is an undesirable behavior where models tailor their responses to follow a human user’s view even when that view is not objectively correct (e.g., adapting liberal views once a user reveals that they are liberal)
	- **Sycophancy,** where the presence of a user’s opinion in a prompt results in the model preferring the answer corresponding to the user’s opinion regardless of if that answer is correct, relates to recent studies analyzing language model biases for particular features in prompts.
- One basic form of reward hacking is sycophancy, where a model responds to a question with a user’s preferred answer in order to look favorable even if that answer is not correct (Cotra, 2021; Perez et al., 2022; Radhakrishnan et al., 2023), as shown in Figure 1.
- across three sycophancy tasks, Flan-PaLM-8B repeats the user’s opinion 26.0% more often than its base model, PaLM-8B
	- model scaling increases sycophancy, even though there is no clear reason why scaling would incentivize sycophantic answers
- natural language processing survey questions (NLP), philosophy survey questions (PHIL), and political typology quiz questions (POLI). In these tasks, sycophantic models will tend to select answers that match the user’s opinion, even though that opinion is not correct because the questions are subjective.
- scaling up language models increases sycophancy within both PaLM and Flan-PaLM model families.
	- PaLM-8B to PaLM-62B increases sycophancy by 19.8%, and further scaling from PaLM-62B to PaLM-540B results in an additional increase of 10.0%.
- instruction tuning significantly increases sycophancy for all models. 
	- PaLM-8B experienced a 26.0% average increase in responses that followed the user’s viewpoint
- Flan-PaLM models with synthetic-data intervention can consistently achieve close-to-perfect accuracy regardless of the presence or absence of the user’s incorrect opinion. These improvements on an unseen task type demonstrate some additional generalization, as our intervention procedure did not include any mathematical data and only used natural-language data
- On simple addition statements, large-enough models with synthetic-data intervention are significantly less likely to follow a user’s incorrect opinion and agree with an incorrect statement (right) despite knowing that the statement is incorrect (left). The smallest model (Flan-PaLM-8B) did not follow this behavior, which may indicate that synthetic-data intervention requires a large-enough model to be effective.
- consider a claim that the model does not know the answer to, such as “foo + bar = baz.” Given a user opinion about this claim, the model will then be trained to randomly agree or disagree with the user since it has no prior knowledge of whether the claim is true.
	- to teach the model to disregard the user’s opinion when considering the claim, the model must know the ground truth of whether the claim is true or not. For this reason, the proposed filtration step is crucial to reducing random or unexpected behavior after intervention.
- Not really tested, but suggested: These findings seem to imply that for large-enough models, filtering incorrectlyanswered prompts is necessary to help stabilize and improve model behavior following intervention. Small models, on the other hand, may need additional processing to benefit from syntheticdata intervention;
- Lu et al. (2022) demonstrated how the particular ordering of examples can vary model performance from state-of-the-art to random-guessing performance. Similarly, Turpin et al. (2023) found that in a chain-of-thought (Wei et al., 2022b) setting, language models can be easily influenced towards specific answers by reordering multiple-choice options in the few-shot examples (e.g., by making the correct answer always “(A)”).
- Perez et al. (2022) demonstrated two key trends in how models exhibit sycophancy—increasing model size up to 52B parameters increases sycophancy and Reinforcement Learning from Human Feedback (Christiano et al., 2017) does not reduce (and sometimes increases) sycophancy.
- ![[2023_Synthetic_Data_Sycophancy_example.png]]
---
