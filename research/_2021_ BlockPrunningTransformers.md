### Block Prunning for Faster Transformers
---
- [Zotero Select Link](zotero://select/groups/2480461/items/SG5C93PX)
- [Zotero URI](https://www.zotero.org/groups/2480461/items/SG5C93PX)
- Authors: [[Francois Lagunas]] [[Alexander Rush]] 
- Topics: [[nlp_transformers]] [[nlp_train]]
- Venue: #EMNLP #arXiv 
- Year: #2021
---
### Major Contributions
- We introduce a block pruning approach targeting both small and fast models. Our approach extends structured methods by considering blocks of any size and integrates this structure into the movement pruning paradigm for fine-tuning. We find that this approach learns to prune out full components of the underlying model, such as attention heads.
- Brings [[_2020_MovementPrunning]] to the Tranformers architecture
---
### Secondary Contribution
- We have shown that we can extract small pruned models that are at an equivalent or better than distilled networks.
---
### Limitations/Future Work
- However, even with this sparsity level, the model is not substantially faster when run on most standard hardware that cannot significantl take advantage of this style of sparse matrix-vectorproduct. -> only for fine tuning
---
### Notes (Try to use backlinks)
- Pruning methods have shown to be extremely effective at reducing the storage size of  models fine-tuned for a specific task.
- We find a surprising result that despite utilizing sub-row square blocks during training, the approach learns to eliminate full components of the model, effectively dropping a large number of attention heads. This effect allows the model to achieve speedups even beyond standard structured pruning of feed-forward layers
- Movement pruning, combined with distillation, has shown to be a very effective method to reduce the number of parameters in an existing model yielding 94% pruning in our tests for a F1 of 87.5 on SQuAD v1.1 (BERT-base is 88.5).
- Finally, the checkpoints created during the experiments are available on an AWS S3 bucket, with their metadata and training parameters, totaling 3TB of data, to facilitate reproduction of our results and to make it possible to study further the behavior of those models.
- We find that all the different block sizes learn to prune out entire dimensions in the FFN layers. Interestingly we find that the block methods can also learn to remove entire heads from the MHA
- This result is in line with Li et al. (2020): the larger the model, the more pruning is effective. When pruning a larger model, the final model is actually better than a smaller one with the same absolute number of parameters.
- 

---
