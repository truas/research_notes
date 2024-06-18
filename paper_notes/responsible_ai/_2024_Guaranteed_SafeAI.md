### Towards Guaranteed Safe AI: A Framework for Ensuring Robust and Reliable AI Systems
---
- [Zotero Select Link](zotero://select/groups/2480461/items/PKLXBHIA)
- [Zotero URI](https://www.zotero.org/groups/2480461/items/PKLXBHIA)
- Authors: [[David Dalrymple]] [[Yoshua Bengio]] [[Joshua Tenenbaum]] 
- Topics: [[ai_safety]] [[ai_responsibe]]
- Venue: #arxiv
- Year: #2024

---
### Major Contributions
- “we will introduce and define a family of approaches to AI safety, which we will refer to as guaranteed safe (GS) AI” (Dalrymple et al., 2024, p. 1)
	- “This is achieved by the interplay of three core components: a world model (which provides a mathematical description of how the AI system affects the outside world), a safety specification (which is a mathematical description of what effects are acceptable), and a verifier (which provides an auditable proof certificate that the AI satisfies the safety specification relative to the world model).” (Dalrymple et al., 2024, p. 1)
- “The AI safety problem is the problem of ensuring that AI systems reliably and robustly act in ways that are not harmful or dangerous, including (but not limited to) cases where those AI systems are more intelligent than humans.” (Dalrymple et al., 2024, p. 2)
---
### Secondary Contribution
- “Anthropic has introduced a framework that they call AI Safety Levels (ASL)1 as part of their voluntary safety commitments (Anthropic, 2023).” (Dalrymple et al., 2024, p. 3)
	- “Anthropic. Anthropic’s responsible scaling policy, 2023. URL https://www-cdn.anthropic.com/ 1adf000c8f675958c2ee23805d91aaade1cd4613/ responsible-scaling-policy.pdf.” (Dalrymple et al., 2024, p. 18)
---
### Limitations/Future Work
- 
---
### Notes (Try to use backlinks)
- AI systems “should be required to adhere to standards of safety that are at least as strict.” (Dalrymple et al., 2024, p. 1)
	- “We will also argue that GS AI presents research avenues that could plausibly produce such safety guarantees in a satisfactory and feasible manner, while remaining competitive with AI systems without such guarantees.” (Dalrymple et al., 2024, p. 1)
- Summary on AI "perils"
	- “For an AI system to reliably solve a complex problem in an open-ended domain where i.i.d. assumptions are not valid, we must provide it with a formalisation of what it means to solve that problem.” (Dalrymple et al., 2024, p. 2)
	- “In a conflict of interests, greater intelligence is a substantial advantage.” (Dalrymple et al., 2024, p. 2)
		- “the reason why humanity is the most powerful species on the planet is primarily that we have the greatest capacity to devise and carry out complex plans” (Dalrymple et al., 2024, p. 2)
		- “if there are ever AI systems that are substantially more intelligent than humans, and which are not aligned with human interests, then we should expect human interests to be marginalised.” (Dalrymple et al., 2024, p. 2)
		- “Even if the goals of an AI system are specified correctly, it may still fail to internalise these goals in the intended way.” (Dalrymple et al., 2024, p. 2)
- “We argue that to obtain a high degree of confidence in a system we need a positive safety case providing quantifiable guarantees, using either or both empirical and theoretical arguments (also see Bloomfield et al. (2019); Khlaaf et al. (2022) for a similar argument).” (Dalrymple et al., 2024, p. 3)
- “core components of GS AI, namely a **world model**, a **safety specification**, and a **verifier**.” (Dalrymple et al., 2024, p. 4)
	- “A Guaranteed Safe AI system is one that is equipped with a quantitative safety guarantee that is produced by a (single, set of, or distribution of) world model(s), a (single, set of, or distribution of) safety specification(s), and a verifier, satisfying the following criteria” (Dalrymple et al., 2024, p. 4)
		- “The probabilistic specification encodes societal risk criteria, which should ideally be determined by collective deliberation. 
		- The verifier provides a quantitative guarantee (in the form of a proof certificate, probabilistic bound, asymptotic guarantee, or other comparable assurance) that the AI system satisfies the specification with respect to the world model.
		- All potential future effects of the AI system and its environment relevant to the safety specification should be modelled (and – if feasible – conservatively overapproximated) by the world model.” (Dalrymple et al., 2024, p. 4)
		- **The World model:** “The world model needs to answer queries about what would happen in the world as a result of a given output from the AI. It must also describe the state of the world at a level of granularity that is sufficient for expressing the safety specifications we are interested in” (Dalrymple et al., 2024, p. 6)
		- “n particular, a **safety specification** may include properties defined by probabilistic temporal logics, causal counterfactual queries, or even hyperproperties, which reward functions cannot typically express (Seshia et al., 2018; Skalse & Abate, 2023a; Subramani et al., 2024)” (Dalrymple et al., 2024, p. 8)
			- “Authoring safety specifications is routine in automated controller design (Tabuada, 2009), and can frequently be achieved for both traditional software systems and domainspecific AI” (Dalrymple et al., 2024, p. 9)
- ![[2024_Guaranteed_SafeAI_Approach.png]]
---
