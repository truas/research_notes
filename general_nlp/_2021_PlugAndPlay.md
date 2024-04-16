### A Plug-and-Play Method for Controlled Text Generation
---
- [Zotero Select Link](zotero://select/groups/2480461/items/ZU7TZMEP)
- [Zotero URI](https://www.zotero.org/groups/2480461/items/ZU7TZMEP)
- Authors: [[Damian Pascual]] [[Roger Wattenhofer]] 
- Topics: [[nlp_text_generation]] [[nlp_transformers]]
- Venue: #EMNLP #arXiv
- Year: #2021
---
### Major Contributions
- we propose Keyword2Text (K2T), a new and simple plug-and-play method for exerting hard control during text generation. K2T (1) does not require a pre-defined ordering of constraints, and (2) can be used for guaranteeing hard constraints.
- given a topic or keyword, we add a shift to the probability distribution over our vocabulary towards semantically similar words. We show how annealing this distribution can be used to impose hard constraints on language generation, something no other plug-and-play method is currently able to do with SOTA language generators
	- at each generation step, we modify the log-probability of the words in our vocabulary according to their semantic similarity to our guide word, quantified as the cosine similarity between their vector representations, i.e., word embeddings.
---
### Secondary Contribution
- 
---
### Limitations/Future Work
- Not clear how the *Fixed Order* works for the guided generation part
---
### Notes (Try to use backlinks)
- Including negative cosine similarities could be used to control generation away from certain words or concepts, e.g., text detoxification
- Given a list of guide words, we propose two approaches for both the case where we need words to appear in a fixed order as well as when any order suffices
	- Fixed Order (score guided towards a specific order) and Guide Closet (set - no order)
- We perform a human evaluation comparing GPT-2+K2T, CGMH and Plan-and-write in which evaluators 30 are presented each of the three texts and asked to evaluate them relative to each other in terms of 4 criteria: fluency, logical consistency, creativity and best overall (see App. A and B for details).
---
