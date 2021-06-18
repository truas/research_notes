### How Many Data Points is a Prompt Worth?
---
- [Zotero Select Link](zotero://select/groups/2480461/items/4J9VMV2M)
- [Zotero URI](https://www.zotero.org/groups/2480461/items/4J9VMV2M)
- Authors: [[Teven Le Scao]] [[Alexander M. Rush]]
- Topics: [[nlp_task]] [[nlp_lm]] [[nlp_train]]
- Venue: #NAACL 
- Year: #2021
---
### Major Contributions
- how many data points is a prompt worth? As with many low-data and pretraining based problems, this question is complicated by the fine-tuning setup, training procedure, and prompts themselves.

---
### Secondary Contribution
---
### Limitations/Future Work
---
### Notes (Try to use backlinks)
- prompting does indeed provide a benefit, and that this benefit can be quantified per task. Results show that prompting is often worth 100s of data pointsin classification
- Fine-tuning via explicit classifier head is giving place to adapting the pretrained language model directly as a predictor through autoregressive text generation (Radford et al., 2019) or completion of a cloze task (Trinh and Le, 2018).  [[_2019_T5]]
- Zero-shot approaches attempt to answer a task with a prompt without fine-tuning through generation (Radford et al., 2019). GPT3 (Brown et al., 2020) extends this approach to a supervised priming method by taking in training data as priming at inference time, so it can attend to them while answering. T5 (Raffel et al., 2019) and other sequence-to-sequence pretrained models use standard word-based fine-tuning with a marker prompt to answer classification tasks with strong empirical success
- We limit ourselves to human written prompts, as we are interested into whether prompting itself specifically adds information to the supervised task.
- **head-based**, where a generic head layer takes in pretrained representations to predict an output class; 
- **prompt-based**, where a task-specific pattern string is designed to coax the model into producing a textual output corresponding to a given class.
---
