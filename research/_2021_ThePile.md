### The Pile : An 800GB Dataset of Diverse Text for Language Modeling
---
- [Zotero Select Link](zotero://select/groups/2480461/items/SHQDUW4U)
- [Zotero URI](https://www.zotero.org/groups/2480461/items/SHQDUW4U)
- Authors: [[Leo Gao]] [[(Connor Leahy]] 
- Topics: [[nlp_dataset]] [[nlp_lm]]
- Venue: #arXiv 
- Year: #2021
---
### Major Contributions
- The Pile: an 825 GiB English text corpus targeted at training large-scale language models. 
- The Pile is constructed from 22 diverse high-quality subset-- both existing and newly constructed—many of which derive from academic or professional sources
---
### Secondary Contribution
---
### Limitations/Future Work
---
### Notes (Try to use backlinks)
- data diversity leads to better downstream generalization capability (Rosset, 2019)
- Compositions of The Pile
	- PubMed Central, ArXiv, GitHub, the FreeLaw Project, Stack Exchange, the US atent and Trademark Office, PubMed, Ubuntu IRC, HackerNews, YouTube, PhilPapers, and NIH ExPorter, Books3, Project Gutenberg, Open-Subtitles, English Wikipedia, DM Mathematics, Europarl, and the Enron Emails corpus
		- We also introduce OpenWebText2 and BookCorpus2, which are extensions of the original OpenWebText and BookCorpus datasets
	- [[_2019_GPT-2]] and [[_2020_GPT-3]] models perform poorly on many components of the Pile, and that models trained on the Pile significantly outperform both raw and filtered Common Crawl models
- Unsurprisingly, larger language models generally attain lower perplexity compared to smaller models
-  [[_2020_GPT-3]] appears to perform poorly on datasets pertaining to research or academic writing like PubMed Central, PubMed Abstracts, and ArXiv; domain-specific datasets like FreeLaw, HackerNews, and USPTO Backgrounds; and on datasetscontaining predominantly text distinct from natural language, like GitHub and DM Mathematics.
-  Pile reporting follows: [[_2018_Datasheets]]  and [[_2018_Datastatments]]
- ![[2021_ThePile_composition.png]]
- ![[2021_ThePile_details.png]]
---
