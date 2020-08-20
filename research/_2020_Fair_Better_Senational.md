### Fair Is Better than Sensational: Man Is to Doctor as Woman Is to Doctor
---
- [Zotero Select Link](zotero://select/groups/2480461/items/NAPRECJM)
- [Zotero URI](https://www.zotero.org/groups/2480461/items/NAPRECJM)
- Authors: [[Malvina Nissim]] [[Rob van der Goot]]
- Topics: [[nlp_bias]] [[nlp_embeddings]]
- Venue: #CL
- Year: #2020
---
### Major Contributions
- They explore the bias in word embeddings models such as those in [[_2013_Word2vec]], but go deeper in the analysis of 'analogies' - which is not properly considered by many that explore the 'problems' in pre-trained models.
- implementation decisions in [[_2013_Word2vec]] force all term of the analogies to be different
---
### Secondary Contribution
- One should consider report at least the top-N results from any analogy task
- most embeddigns are produced from the top N words in the collection (Manzini 2019)
---
### Limitations/Future Work
---
### Notes (Try to use backlinks)
- Analogies are not an accurate tool to evaluate [[nlp_bias]]
- In the original proportional analogy implementation, all terms of the equation A : B :: C : D are distinct (Mikolov et al. 2013), that is, the model is forced to return a different concept than any of the input ones. Given an analogy of the form A : B :: C : D, the code explicitly prevents yielding any term D such that D == B, D == A, or D === C.
- Should all terms be different in an analogy of form A::B : C::D ?
- code available [here](https://bitbucket.org/robvanderg/w2v.)
- instead of man:doctor :: woman:x , why not woman:doctor :: man:x; models will provide different structures
- interesting and down to earth final considerations: 
	- we should aim at debiasing or rather at transparency and awarness
	- analogies are not the most appropriate tool for certain relations - they way people portrait today, just made it worse.
---
