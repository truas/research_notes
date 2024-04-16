### NLP Scholar: An Interactive Visual Explorer for Natural Language Processing Literature
---
- [Zotero Select Link](zotero://select/groups/2480461/items/EETMJEJ3)
- [Zotero URI](https://www.zotero.org/groups/2480461/items/EETMJEJ3)
- Authors: [[Saif Mohammad]] 
- Topics: [[nlp_tools]] #scientometrics
- Venue: #ACL
- Year: #2020
---
### Major Contributions
---
### Secondary Contribution
---
### Limitations/Future Work
---
### Notes (Try to use backlinks)
- ACL Anthology - 50K articles published 1965 - 2019
	- After discarding noise data (schedules, foreword) we are left with a set of 44,895 papers
	- GoogleScholar-NLP includes 32,985 of the 44,895 papers in AA (about 74%).
	- No statistics
	- Entries across AA and GS are aligned by matching the paper title, year of publication, and firs author last name.
- We first created a relational database (involving multiple tables) that stores the AA and GS data (x4.1). We then loaded the x database in Tableau—an interactive data visualization software—to build the visualizations (x4.2).
- We extracted paper title, names of authors, year of publication, and venue of publication from the repository.
- papers: Each row corresponds to a unique paper. The columns include: paper title, year of publication, list of authors, venue of publication, number of citations at the time of data collection (June 2019), NLP Scholar paper id, ACL paper id, and some other meta-data associated with the paper.
- The NLP Scholar paper id is a concatenation of the paper title, year of publication, and first author last name. (This id was also used to align entries across AA and GS).
- **Some Findings**
	- there was a spurt in the 1990s and substantial numbers since the year 2000. Also, note that the number of publications is considerably higher in alternate years. This is due to certain biennial conferences.
	- 
---