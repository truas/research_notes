### Growing a Brain: Fine-Tuning by Increasing Model Capacity
---
- [Zotero Select Link](zotero://select/groups/2480461/items/I4LRGFLG)
- [Zotero URI](https://www.zotero.org/groups/2480461/items/I4LRGFLG)
- Authors: [[Yu-Xiong Wang]] [[Martial Hebert]]
- Topics: [[NLP_ANN_dynamic_architecture]]
- Venue: #CVPR
- Year: #2019
---
### Techniques
---
### Major Contributions
- The paper first demonstrates that the dominant paradigm of fine-tuning a fixed-capacity model is sub-optimal.
- They explore several avenues for increasing model capacity, both in terms of going deeper (more layers) and wider (more channels per  layer), and consistently find that increasing capacity helps, with a slight preference for widening.
- They show that additional units must be normalized and scaled appropriately such that the “pace of learning” is balanced with existing units in the model.
- The article proposes a straight-forwards pipeline that “grows” a pre-trained model during fine-tuning, producing state-of-the-art results across a large number of standard and heavily benchmarked  datasets (for scene classification, fine-grained recognition, and action recognition).
---
### Secondary Contribution
---
### Limitations/Future Work
---
### Notes (Try to use backlinks)
- The paper explores two approaches of adding units: going deeper (more layers) and wider (more channels per layer).
- Connection to [[_2020_Scaling_laws_for_neural_LMs]], architecture is not so important but as capacity increases, so does performance. So maybe it is sufficient to just make the model larger (w.r.t. normalization of new layers).
---


