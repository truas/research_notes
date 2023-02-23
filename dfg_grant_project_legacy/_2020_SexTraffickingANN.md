### Sex Trafficking Detection with Ordinal Regression Neural Networks
---
- [Zotero Select Link](zotero://select/groups/2480461/items/YRWNZAKJ)
- [Zotero URI](https://www.zotero.org/groups/2480461/items/YRWNZAKJ)
- Authors: [[Longshaokan Wang]] [[Sherrie Caltagirone]]
- Topics: [[sex_trafficking]] [[human_trafficking]]
- Venue: #arXiv
- Year: #2020
---
### Major Contributions
- They propose an ordinal regression neueral network to identify escort ads that are llinked to sex trafficking
	- improves state of the art in the [[Trafficking-10K]] from [[_2017_HumanTrafficking10K]]
- Combine: [[_2013_Word2vec]] + [[_2015_GRU]] and ordinal regression layer to predict their labes.
- Similar approach to the [[HTDN]], but they change the [[LSTM]] for  a [[GRU]]
	- they also pre train a skipgram of [[word2vec]]
---
### Secondary Contribution
- They provide a qualitative analysis on the top escort ads flagged by their model, which offers patterns that anti-trafficking experts can potentially confirm or make use of.
- They include a study using emojis as well
---
### Limitations/Future Work
- Their [[_2013_Word2vec]] model have no specifications available, except it used 168,337 ads from [[Backpage]]
---
### Notes (Try to use backlinks)
- Software products to aid anti-trafficking efforts:
	- [MEMEX](darpa.mil/program/memex)
	- [Spotlight](htspotlight.com)
	- [Traffic Jam](marinusanalytics.com/trafficjam)
	- [TraffickCam](traffickcam.com)
---
