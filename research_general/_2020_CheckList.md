### Beyond Accuracy: Behavioral Testing of NLP Models with CheckList
---
- [Zotero Select Link](zotero://select/groups/2480461/items/DX7UBNDN)
- [Zotero URI](https://www.zotero.org/groups/2480461/items/DX7UBNDN)
- Authors: [[Marco Tulio Ribeiro]] [[Sameer Singh]]
- Topics: [[nlp_task]] [[nlp_metrics]]
- Venue: #ACL
- Year: #2020
---
### Major Contributions
- Evaluating NLP models in downstream tasks through accuraccy does account for real lingustic capabilities
- [[_2020_CheckList]] introduces new test types:
	- invariance in the presence of certain pertubations
	- sanity checks
- Recommended capabilities:
	- [[Vocabulary]]+[[POS]] - important words or word types for the task
	- [[Taxonomy]] - synonyms, antonyms, etc
	- [[Robustness]] - to typos, irrelevant changes, etc
	- [[NER]] - understand named entities
	- [[Fairness]]
	- [[Temporal]] - order of events
	- [[Negation]]
	- [[Correference]]
	- [[SRL|Semantic Role Labeling]] - understanding roles such as agent, object, etc
	- [[Logic]] - ability to handle symmetry, consistency, conjunctions
- Each capability should be tested under three different test types:
	- [[MFT]]
	- [[INV]]
	- [[DIR]] 
---
### Secondary Contribution
- Bringing the testing idea-concepts from [[software engineering|SE]] into NLP
- Test of [[_2019_BERT]] and [[_2019_RoBERTa]] under several circumstances
- They conducted a system industry check with Microsoft on [[_2020_CheckList]]
---
### Limitations/Future Work
- Can we use these templates into Mechanical Turk to scale difficult examples?
- Some discussions towards the bias of the models are not well ellaborated. they emphasize the model predicts male in occupation where it should be a woman. However, none is presented about the data used. Of course it would be impossible to re-run [[_2019_BERT]] from scratch for this study, but it seems obvious that a curated data would mitigate this issue.
---
### Notes (Try to use backlinks)
- Best paper award #ACL #2020
- Many individual evaluation approaches have been proposed, but they focus on individual tasks. [[_2020_CheckList]] tackles linguistics properties in a general way.
- GitHub [link](https://github.com/marcotcr/checklist) 
- Negation capability -> [[MFT|Minimum Functionality Test]].
	- detecting when models use shortcuts to handle complex inputs without actually mastering the capability
- [[NER]] -> [[INV|Invariance Test]]
	- apply label-preserving pertubations to inputs and expect the model prediction to remain the same
- Vocabulary -> [[DIR|Directional Expectation Test]]
	- label is expected to change in a certain way
- Failure is almost 100% for all comercial modesl when the negation comes at the end of the sentence or with neutral content between the negation and the sentiment-laden word
	- *this will come back to hunt BERT*: "the other hand, always predicts negative when {PROTECTED} is black, atheist, gay, and lesbian,while predicting positive for Asian, straight, etc."
	
---
