### The Limitations of Stylometry for Detecting Machine-Generated Fake News
---
- [Zotero Select Link](zotero://select/groups/2480461/items/WYB4H9PC)
- [Zotero URI](https://www.zotero.org/groups/2480461/items/WYB4H9PC)
- Authors: [[Tal Schuster]] [[Regina Barzilay]]
- Topics: [[nlp_text_classification]] [[nlp_lm]] [[plagiarism_detection]]
- Venue: #CL
- Year: #2020
---
### Major Contributions
- Main question: Can stylometry be used to distinguish malicious uses of [[LM]] from legitimate ones?
	- Expose the need for non-stylometry approaches in detecting machine generated misinformation.
- Include a human evaluation scenario to counter pose the one from [[_2019_Grover_Mega]]
- zero-shot setting classifier is effective in detecting the fully generated articles of a different model
- LM-generated falsified texts are very similar in style to LM-generated texts containing true content
---
### Secondary Contribution
- Two benchmarks are proposed
	- extension scenario: auto-completion text generator extends a news article
	- modification scenario: subtle modification to semantically modify statements (adding negation 'no' to the text)
	- Stylometry-based classifiers do not perform much better than humans in detection potetional misinformation, and that verifying against other resoucers can improve results
- Takeaways: extend veracity-based benchmarks; improve non-stylometry methods
---
### Limitations/Future Work
- Experiments and data availability are somehow limited
---
### Notes (Try to use backlinks)
- Weak [[LM]] can be used to produce statement inversions that the state-og-the-art stylometry-based models cannot detect.
- Their dataset creation (i.e. with only a limited number of false statements) is
aligned with the way humans tend to deceive or lie.
- Attack and Defense Capabilities: attacker: wishes to generate fake text using a [[LM]]; verifier (adaptive): receives limited examples from 'attacker' and tries to classify it as real or not; they also do a zero-shot, which includes 0 examples from the attacker
-  They used [[_2019_Grover_Mega]] as their discriminator for the experiments
-  Cohen's kappa score included for annotation agreement
---
