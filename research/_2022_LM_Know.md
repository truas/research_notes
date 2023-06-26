### Language Models (Mostly) Know What They Know
---
- [Zotero Select Link](zotero://select/groups/2480461/items/HP5VPSRF)
- [Zotero URI](https://www.zotero.org/groups/2480461/items/HP5VPSRF)
- Authors: [[Saurav Kadavath]] [[Chris Olah]] [[Jared Kaplan]] 
- Topics: [[nlp_llm]] [[nlp_learning]]
- Venue: #arxiv #Anthropic 
- Year: #2022

---
### Major Contributions
- We study whether language models can evaluate the validity of their own claims and predict which questions they will be able to answer correctly.
- Our core findings are that large language models can be well-calibrated on diverse multiple choice questions, that they perform well at self-evaluation on a range of subjects, and that they can be trained to predict what they do and don’t know and exhibit some generalization to new domains and in-context information sources.
---
### Secondary Contribution
- We also show that self-evaluation can be improved if we provide a model with many of its own samples, before asking it to evaluate any single sample. That is, ‘brainstorming other possibilities’ helps large models to evaluate the validity of a given answer option
- Replacing an option with ‘none of the above’ reduces accuracy and calibration significantly with our models (see Figure 7).
- Models can self-evaluate whether their own samples are True or False, though this tends to be a more challenging task (since models tend to find their own samples more plausible). Self-evaluations are well-calibrated few-shot, though models aren’t as well-calibrated zero-shot.
---
### Limitations/Future Work
- 
---
### Notes (Try to use backlinks)
- Good calibration opens up the possibility for using models to evaluate the accuracy of their own outputs (“self-evaluation”). For example, given any open-ended query, we can sample an answer from the model and then have the model evaluate P(True), the probability that its answer is correct.
- If language models can answer multiple choice questions in a calibrated way, then one might hope that they can apply this ability to evaluate their own outputs
- That is, we can simply ask models to generate potential answers to questions, and then have the model evaluate whether any of them are correct -> evaluate the test to check if it is located in the model or if the generated output is  simply a copy from training
- This means that in effect, we are observing that verification has an advantage over generation.
---
