### Improving Abstractive Dialogue Summarization with Graph Structures and TopicWords
---
- [Zotero Select Link](zotero://select/groups/2480461/items/3V8PT7MA)
- [Zotero URI](https://www.zotero.org/groups/2480461/items/3V8PT7MA)
- Authors: [[Lulu Zhao]] [[Jun Guo]] 
- Topics: [[nlp_text_summarization]] [[nlp_meeting_sum]]
- Venue: #COLING 
- Year: #2020
---
### Major Contributions
- we propose a Topic-word Guided  Dialogue Graph Attention (TGDGA) network to model the dialogue as an interaction graph according to the topic word information
	- We devise a topic-word guided graph-to-sequence network that generates dialogue summaries in an end-to-end way
	- 
---
### Secondary Contribution
---
### Limitations/Future Work
- Related work is quite descriptive rather then compared with the proposed methoologyl
---
### Notes (Try to use backlinks)
- Although some progress has been made in abstractive dialogue summarization task, previous methods do not develop specially designed solutions for dialogues, and are all dependent on sequence-to-sequence models, which can not handle the sentence-level long-distance dependency and capture the cross-sentence relations.
- The TGDGA includes four parts: 
	- (1) Dialogue Graph Construction 
	- (2) Graph Encoder 
	- (3) Sequential Context Encoder 
	- (4) Topic-word Guided Decoder. Figure 1 presents the overview of our model.
- ![[2020_TGDGA_architecture.png]]
---
