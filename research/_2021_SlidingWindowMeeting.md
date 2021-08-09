### A Sliding-Window Approach to Automatic Creation of Meeting Minutes
---
- [Zotero Select Link](zotero://select/groups/2480461/items/QVHY5E8Q)
- [Zotero URI](https://www.zotero.org/groups/2480461/items/QVHY5E8Q)
- Authors: [[Jia Jin Koay]] [[Fei Liu]] 
- Topics: [[nlp_meeting_sum]] [[nlp_text_summarization]]
- Venue: #NAACL 
- Year: #2021
---
### Major Contributions
- Our approach combines a sliding window and a neural abstractive summarizer to navigate through the transcripts to find salient content
	- (1) what are suitable window and stride sizes? 
	- (2) can the abstractive summarizer effectively identify salient local content? 
	- (3) how should we consolidate local abstracts into meeting-level summaries?
---
### Secondary Contribution
---
### Limitations/Future Work
---
### Notes (Try to use backlinks)
- In this study, we use [[_2019_BART]] BART-large-cnn as a base summarizer. The model is then fine-tuned on the CNN dataset for abstractive summarization
	- BART is trained on written text, rather than spoken text
	- a transcript can far exceed the maximum input length of the model
- sliding-window approach to generating meeting minutes is appealing because it breaks lengthy transcripts into small and manageable local windows, allowing a set of “mini-summaries” to be produced from such windows which are then assembled into meeting-level summaries
	- conisderation: size of sliding window (bounded to BART input sequence)
- 
---
