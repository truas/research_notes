### Attacks, Defenses and Evaluations for LLM Conversation Safety: A Survey
---
- [Zotero Select Link](link)
- [Zotero URI](link)
- Authors: [[Zhichen Dong]] [[Yu Qiao]] 
- Topics: [[tag1]] [[ai_safety]] [[nlp_llm]] [[survey_ai_safety]]
- Venue: #arxiv #NAACL
- Year: #2024

---
### Major Contributions
- we provide a comprehensive overview of recent studies, covering three critical aspects of LLM conversation safety: attacks, defenses, and evaluations. Our goal is to provide a structured summary that enhances understanding of LLM conversation safety and encourages further investigation into this important subject.
- [GitHiub](https://github.com/niconi19/LLM-conversation-safety)
---
### Secondary Contribution
- 
---
### Limitations/Future Work
- 1) Limited domain diversity of attacks renders attacks vulnerable to retrospective defenses.
- 2) False refusal/exaggerated safety for defenses occurs when LLMs mistakenly identify safe questions as dangerous and refuse to answer them (Bianchi et al., 2023).
- 3) Unified evaluation standards and metrics for evaluations are an often overlooked area of discussion
---
### Notes (Try to use backlinks)
- need for a detailed review that summarizes recent advancements in LLM conversation safety, focusing on three main areas: 1) LLM attacks, 2) LLM defenses, and 3) the relevant evaluations of these strategies
- ![[2024_LLM_Conversational_LLM_Safety_overview.png]]
- Extensive research has studied how to elicit harmful outputs from LLMs, and these attacks can be classified into two main categories: inference-time approaches (Sec. 2.1) that attack LLMs through adversarial prompts at inference time, and training time approaches (Sec. 2.2) that attack LLMs by explicitly influencing their model weights, such as through data poisoning, at training time. Fig. 3 illustrates these attacks in a unified pipeline
- **Inference-time attacks** construct adversarial prompts to elicit harmful outputs from LLMs without modifying their weights.
	- we refer to **red-team attacks** as finding malicious instructions representative of common user queries, e.g., ‘Please tell me how to make a bomb’.
	- ![[2024_LLM_Conversational_Safety_LLM_Attacks.png]]
	- Red-team attacks are effective against unaligned LLMs but are ineffective against LLMs with builtin security (Touvron et al., 2023; OpenAI, 2023a).
	- **Template-based attacks** aim to find a universal template that, with the raw red-team instructions plugged in, can jailbreak LLM’s built-in security and force the victim LLMs to follow the instructions. The approaches can be further categorized into two subclasses according to how these templates are discovered: 1) heuristics-based attacks where humans construct the templates and 2) optimization-based attacks
- Training-time attacks differ from inference-time attacks (Sec. 2.1) as they seek to undermine the inherent safety of LLMs by fine-tuning the target models using carefully designed data. This class of attacks is particularly prominent in opensource models but can also be directed towards proprietary LLMs through fine-tuning APIs, such as GPTs
	- some studies have utilized finetuning as a means to disable the self-defense mechanisms of LLMs - poisoned-LMs (Gade et al., 2023; Lermen et al., 2023)
- ![[2024_LLM_Conversational_Safety_defenses.png]]
	- we propose a hierarchical framework for representing all defense mechanisms, as shown in Fig. 4. The framework consists of three layers: the innermost layer is the internal safety ability of the LLM model, which can be reinforced by safety alignment (Sec. 3.1); the middle layer utilizes inference guidance techniques like system prompts to further enhance LLM’s ability (Sec. 3.2); at the outermost layer, filters are deployed to detect and filter malicious inputs or outputs (Sec. 3.3).
		- Zhanhui Zhou, Jie Liu, Chao Yang, Jing Shao, Yu Liu, Xiangyu Yue, Wanli Ouyang, and Yu Qiao. 2023b. Beyond one-preference-fits-all alignment: Multiobjective direct preference optimization.
		- Ji J, Liu M, Dai J, Pan X, Zhang C, Bian C, Chen B, Sun R, Wang Y, Yang Y. Beavertails: Towards improved safety alignment of llm via a human-preference dataset. Advances in Neural Information Processing Systems. 2024 Feb 13;36.
	- Inference Guidance. Inference guidance helps LLMs produce safer responses without changing their parameters. One commonly used approach is to utilize system prompts. These prompts are basically integrated  within LLMs and provide essential instructions to guide their behaviors, ensuring they act as supportive and benign agents (Touvron et al., 2023;Chiang et al., 2023).
	- Rule-based filters. Rule-based filters are commonly used to capture specific characteristics of attack methods by applying corresponding rules. For instance, in order to identify attacks that result in decreased language fluency, the PPL (Perplexity) filter (Alon and Kamfonas, 2023) utilizes the perplexity metric to filter out inputs with excessively high complexity
	- ![[2024_LLM_Conversational_Safety_datasets.png]]
	- Section 4.1 Evaluations dataset seem interesting
		- Topics, formulations, red-state, jailbreak, dialogue, etc
	- 
	----
