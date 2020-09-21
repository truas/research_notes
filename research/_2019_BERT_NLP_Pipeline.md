### BERT Rediscovers the Classical NLP Pipeline
---
- [Zotero Select Link](zotero://select/groups/2480461/items/5AU2PAUF)
- [Zotero URI](https://www.zotero.org/groups/2480461/items/5AU2PAUF)
- Authors: [[Ian Tenney]] [[Ellie Pavlick]]
- Topics: [[nlp_task]] [[nlp_metrics]]
- Venue: #ACL
- Year: #2019
---
### Major Contributions
- They evaluate [[_2019_BERT]] through several probing tasks [[_2019_Probe_Tasks]] analyzing how each layer behaves
- They test eight probing tasks: #POS, #constituents, #Dependencies, #entities, #SRL, #coref, #SPR, and #relation_classification
---
### Secondary Contribution
---
### Limitations/Future Work
---
### Notes (Try to use backlinks)
- They freeze encoder weights to prevent the encoder from re-arranging its internal representations to better suit the probing task
- Center-of-Gravity: average layer attended to for each task, intuitively, they can interpret a higher value to mean that the information needed for that task is captured by higher layers
- Consistent trend across both of our metrics, with the tasks encoded in a natural progression: POS tags processed earliest, followed by constituents, dependencies, semantic roles, and coreference
- syntactic information appears earier in the network
	- more localized, weights related to syntactic tasks tend to be concentrated on a few layers
- higher-level semantic information appears at higher layers
	- information related to semantic tasks is geneally spread across the entire network
- most examples can be correctly classified very early on the network. 
	- availability of heuristic shortcuts
	- challenging examples may not be resolved until much later, many cases can be guessed from shallow statistics
---
