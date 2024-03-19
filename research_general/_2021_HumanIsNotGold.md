### All That’s ‘Human’ Is Not Gold: Evaluating Human Evaluation of Generated Text
---
- [Zotero Select Link](zotero://select/groups/2480461/items/29ITNS2G)
- [Zotero URI](https://www.zotero.org/groups/2480461/items/29ITNS2G)
- Authors: [[Elizabeth Clark]] [[Noah Smith]] 
- Topics: [[nlp_eval]] [[nlp_ppd]] [[nlp_text_generation]]
- Venue: #ACL
- Year: #2021
---
### Major Contributions
- We run a study assessing nonexperts’ ability to distinguish between humanand machine-authored text (GPT2 and GPT3) in three domains (stories, news articles, and recipes).
- without training, evaluators distinguished between GPT3- and human-authored text at random chance level
---
### Secondary Contribution
- Based on our findings, if NLG researchers must run human evaluations as small-batch evaluation on Amazon Mechanical Turk or similar platforms, we recommend they train evaluators with examples. This will help calibrate the evaluators’ expectations of generated text and indicate the careful reading they may need to do to properly assess the text’s quality.
	- Our experiments also indicate the importance of confirming with evaluators why they have made the decisions they have, as the criteria they might implicitly be evaluating may be mismatched with researchers’ intended criteria
---
### Limitations/Future Work
---
### Notes (Try to use backlinks)
- Since we lack a good way of encoding many aspects of what constitutes human-quality output in an automated method, we often must rely on human evaluation for our models
- a superficial read may not be sufficient to catch model errors. For accurate assessments of generated text, we need human evaluations that are designed to encourage a sufficiently careful reading of the text to examine these subtler aspects of text quality.
- we found including examples in the task increased the set of texts evaluators thought could be machine-generated and increased their focus on textual content, no training method significantly increased evaluators’ performance consistently across domains.
- we had 130 different evaluators for each of the 6 task settings (3 domains × 2 models). Each participant evaluated 5 texts each, giving us a total of 780 participants and 3,900 text evaluations.
- Overall, evaluators choosing between human and GPT2-generated text correctly identified the author of the text 57.9% of the time,6 but the evaluators choosing between human- and GPT3-generated text only guessed correctly 49.9% of the time (Table 1), compared to 50% random chance
- To test the effectiveness of each type of training, we re-ran the experiments from §2, but this time, we prepended one of three evaluator-training methods to the evaluation task: an instruction-based training, an example-based training, and a comparison-based training
	- Training with Examples - Our Examples training consisted of 3 practice rounds of the actual task: given a text, guess if it is machine- or human-authored. We collected 3 additional texts in the same manner described in §2.2 and wrote a short explanation of which aspects of the text hinted at its source
- We found that while all 3 training methods improved evaluators’ accuracy at identifying machine vs. human-authored text over the no-training accuracy, the Examples training was the only one that showed significant improvement
- Ippolito et al. (2020) found that trained evaluators were able to detect open-ended GPT2-L-generated text 71.4% of the time and Brown et al. (2020) found evaluators could guess GPT3-davinci-generated news articles’ source with 52% accuracy, though these results are not directly comparable to ours due to differences in the evaluation setup, data, and participants
---
