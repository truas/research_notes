### Deep Learning for Suicide and Depression Identification with Unsupervised Label Correction
---
- [Zotero Select Link](zotero://select/groups/2480461/items/4ILFSC9W)
- [Zotero URI](https://www.zotero.org/groups/2480461/items/4ILFSC9W)
- Authors: [[Ayaan Haque]] [[Tyler Giallanza]]
- Topics: [[nlp_psychology]] [[nlp_task]] [[nlp_text_classification]]
- Venue: #arXiv
- Year: #2021
---
### Major Contributions
- An application of deep learning-based sentiment analysis for depression versus suicidal ideation classification, an important but unexplored clinical and computational challenge
- A novel, unsupervised label correction process for text-based data and labels which does not require prior noise distribution information, allowing for the use of mass online conten
- Extensive experimentation and ablation on multiple datasets, demonstrating the success of our label correction and deep learning classification approach on the challenging proposed task
- 
---
### Secondary Contribution
- To the best of our knowledge, there are no current methods which perform label correction using unsupervised clustering methods, and particularly not in the NLP domain.
- [[SDCNL]] method
	- processing data scraped from Reddit with word embeddgins modles
	- reduce dimensionality
	- input into cluster-based algorithm to obtain the labels
	- produced labelsare compared with the ground truth  to correct labels based on confidence score/treshold
		- We contend that, since we demonstrated that the proposed label correction method is effective on the C-SSRS and IMDB datasets, the use of the label correction method on the Reddit dataset is valid
	- 
---
### Limitations/Future Work
- Some label problems in figures 2-3 make it hard to identify the best performing noise-handling algorithm.
---
### Notes (Try to use backlinks)
- Lack of  [[EHR|Eletronic Healt Record]] - the internet (e.g., Reddit r/SuicideWatch and r/depression) surges as a good alternative
- There is little work focused on detecting when individuals with underlying mental health struggles such as depression are at risk of attempting suicide.
- Labeling data based on subreddit relies on self-reporting, since each user chooses which subreddit they feel best reflects their mental state
	- This concept is referred to as [[noisy labels]] as there is a potential for certain labels to be corrupted. Estimates show that noisy labels can degrade anywhere from 10% to 40% of the dataset
- Approaches to deal with [[noisy labels]]:
	- noise-robust (less sensitiv to noise), noise-tolerant (methods directly model the noise during training): modification to the architecture and/or loss function 
	- data-cleaning
- ![[2021_SDCNL_architecture.png]]
- Three dimensionality reduction algorithms were tested: [[PCA]], Deep Neural Autoencoders, and [[UMAP]]
---
