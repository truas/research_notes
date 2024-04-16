### On the Dangers of Stochastic Parrots: Can Language Models Be Too Big?
---
- [Zotero Select Link](zotero://select/groups/2480461/items/3QD9NGQE)
- [Zotero URI](https://www.zotero.org/groups/2480461/items/3QD9NGQE)
- Authors: [[Emily M. Bender]] [[Shmargaret Smitchell]] [[Timnit Gebru]]
- Topics: [[nlp_lm]] [[nlp_bias]] [[responsible_ai]]
- Venue: #FAccT
- Year: #2021
---
### Major Contributions
- How big is too big? What are the possible risks associated with this technology and what paths are available for mitigating those risks?
---
### Secondary Contribution
---
### Limitations/Future Work
---
### Notes (Try to use backlinks)
- we encourage the research community to prioritize these impacts. One way this can be done is by reporting costs and evaluating works based on the amount of resources they consume
- LMs are not performing natural language understanding (NLU), and only have success in tasks that can be approached by manipulating linguistc form.
- Transformer models, on the other hand, have been able to con tinuously benefit from larger architectures and larger quantities of data.
- n-grams -> deployed in selecting among the outputs of e.g. acoustical or translation models;
- LSTM -> effective representation of words (instead of [[BOW]])
- Transformers -> can be retrained multiple times on small datasets -> meaning manipulation tasks such as summarization, QA.
- Training a single BERT base model (without hyperparameter tuning) on GPUs was estimated to require as much energy as a trans-American flight
- 0.1 BLEU score using neural architecture search for English to German translation results in an increase of $150,000 compute cost in addition to the carbon emissions
- the amount of compute used to train the largest deep learning models (for NLP and other applications) has increased 300,000x in 6 years, increasing at a far higher pace than Moore’s Law.
- GPT-2’s training data is sourced by scraping out bound links from Reddit, and Pew Internet Research’s 2016 survey reveals 67% of Reddit users in the United States are men, and 64% between ages 18 and 19. Similarly, recent surveys of Wikipedians find that only 8.8–15% are women or girls.
- Their investigation of GPT-2 data training also finds 272K documents from unreliable news sites and 63K from banned subreddits.
- While documentation allows for potential accountability, undocumented training data perpetuates harm without recourse. Without documentation, one cannot try to understand training data characteristics in order to mitigate some of these attested issues or even unknown ones.
- We also advocate for a re-alignment of research goals: Where much effort has been allocated to making models (and their training data) bigger and to achieving ever higher scores on leaderboards often featuring artificial tasks, we believe there is more to be gained by focusing on understanding how machines are achieving the tasks in question and how they will form part of socio-technical systems.
---
