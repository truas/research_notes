### Combating Human Trafficking with Deep Multimodal Models
---
- [Zotero Select Link](zotero://select/groups/2480461/items/GGKCUSUA)
- [Zotero URI](https://www.zotero.org/groups/2480461/items/GGKCUSUA)
- Authors: [[Edmund Tong]] [[Louis-Philippe Morency]] [[Cara Jones]]
- Topics: [[human_trafficking]]
- Venue: #arXiv
- Year: #2017
---
### Major Contributions
- Novel dataset [[Trafficking-10k|Human Trafficking Dataset]] (first)
	- USA and Cananda ads - 1 ad + 5 images from it
	- Annotated by 2 experts (+5/+1 years on human trafficking)
	- FOCUS: (1) violation of constituency, and (2) presence of irrelevant information not related to trafficking but present in ads.
- [[HTDN|Human Trafficking Deep Network]] model to detect trafficking advertising
	- Uses both text [[LSTM]] and images [[T-VGG]] (a variation of [[VGG]] - Very deep convolutional networks for large-scale image)
---
### Secondary Contribution
- General word embeddings do not cover most of the unigrams in [[Trafficking-10k]]
	- [[_2014_GloVe]] - 49.7%
- They train a word embedding model in 1M unlabeled ads from datasets (-[[Trafficking-10k]]) which now covers 94.9% of the dataset. 
- Often, neither linguistic nor visual cues alone can suffice to classify whether an ad is suspicious
---
### Limitations/Future Work
 - Only one neural network approach is tested [[HTDN]]
---
### Notes (Try to use backlinks)
- Human trafficking moved from 3,279 in 2012 to 7,572 in 2016—more than doubling over the course of five years (Hotline,2017).
- Focus on advertisments
- Law enforcement officers have populated lists of keywords that frequently occur in trafficking advertisements. 
	- Simplistic queries fail when traffickers use complex obfuscation.
- Why ist it hard?
	- Defective language compositionality
	- Generalizable Language Context - Learned discriminative features should be generalizable and model semantics of trafficking
	- Multimodal nature
- ![[2017_HumanTrafficking10K.png]]
---
