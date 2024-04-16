### Energy and Policy Considerations for Deep Learning in NLP
---
- [Zotero Select Link](zotero://select/groups/2480461/items/ZM2RYLWB)
- [Zotero URI](https://www.zotero.org/groups/2480461/items/ZM2RYLWB)
- Authors: [[Emma Strubell]] [[last auhtor]] [[Andrew McCallum]]
- Topics: [[nlp_green]] [[ai_green]] #responsible_ai 
- Venue: #ACL 
- Year: #2019
---
### Major Contributions
- Quantifying the approximate financial and environmental costs of training a variety of recently successful neural network models for NLP
---
### Secondary Contribution
---
### Limitations/Future Work
---
### Notes (Try to use backlinks)
- Recommendation
	- (1) Time to retrain and sensitivity to hyperparameters should be reported for NLP machine learning models; 
	- (2) academic researchers need equitable access to computational resources; and
		- Limiting this style of research to industry labs hurts the NLP research community in many ways. First, it stifles creativity. Researchers with good ideas but without access to large-scale compute will simply not be able to execute their ideas, instead constrained to focus on different problems. Second, it prohibits certain types of research on the basis of access to financial resources
	- (3) researchers should prioritize developing efficient models and hardware
- While training, we repeat edly query the NVIDIA System Management Interface to sample the GPU power consumption and report the average over all samples. To sample CPU power consumption, we use Intel’s Running Average Power Limit interface
	- [[NVIDIA SMI]](https://bit.ly/30sGEbi)
	- [RAPL power meter](https://bit.ly/2LObQhV)
- We estimate total power consumption as combined GPU, CPU and DRAM consumption, then multiply this by Power Usage Effectiveness (PUE), which accounts for the additional energy required to support the compute infrastructure (mainly cooling).
- training [[_2019_BERT]] on GPU is roughly equivalent to a trans-American fligh
---
