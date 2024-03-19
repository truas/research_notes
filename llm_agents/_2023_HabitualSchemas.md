### We Are What We Repeatedly Do: Inducing and Deploying Habitual Schemas in Persona-Based Responses
---
- [Zotero Select Link](zotero://select/groups/2480461/items/8NLQ2JDD)
- [Zotero URI](https://www.zotero.org/groups/2480461/items/8NLQ2JDD)
- Authors: [[Benjamin Kane]]  [[Lenhart Schubert]] 
- Topics: [[nlp_agent]] [[nlp_llm]]
- Venue: #arxiv #EMNLP
- Year: #2023

---
### Major Contributions
- we propose a novel approach to dialogue generation that uses a collection of explicit event schemas to augment an agent’s persona, and that conditions an LLM to generate narrative-like responses consistent with these schemas through in-context prompting1. Furthermore, since it is often desirable for dialogue designers to be able to specify a persona using a small number of simple natural language facts, we propose a method for bootstrapping the creation of schemas from a set of simple facts.
---
### Secondary Contribution
- 
---
### Limitations/Future Work
- 
---
### Notes (Try to use backlinks)

- Recent work has found that conversational systems that leverage incontext learning with LLMs outperform those that fine-tune smaller language models on conversational data (Madotto et al., 2021; Zheng and Huang, 2022).
- The framework of deriving explicit knowledge from LLMs has been explored in other work, though primarily in the context of IR and commonsense reasoning systems rather than personabased dialogue generation.
	- West et al. (2022) show that implicit knowledge within an LLM can be distilled into a symbolic commonsense knowledge graph using prompt engineering techniques.
- Following (Zheng and Huang, 2022), we employ a prompting-based approach in which a pre-trained generative LLM is used to produce a response utterance, provided a prompt that is dynamically constructed from the dialogue history and the selected schemas.
- “we focus on the problem of automatically inducing event schemas from an unstructured persona P = {p1, p2, ..., pn}, where pi are natural language “facts” such as “I like to play tennis.”2. Formally, we represent an event schema as a tuple ⟨H, Pr, S, Po, G, E⟩. H is a schema header; a sentence characterizing the overall schema event. Pr, S, and Po are sets containing schema preconditions, static conditions (conditions expected to hold throughout the overall event), and postconditions, respectively. G is a set containing typical goals of participants of the event, and E is a set containing typical episodes (i.e., substeps) of the event” (Kane and Schubert, 2023, p. 3)
- ![[2023_HabitualSchemas_approach.png]]
---
