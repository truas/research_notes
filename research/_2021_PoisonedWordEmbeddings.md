### Be Careful about PoisonedWord Embeddings: Exploring  the Vulnerability of the Embedding Layers in NLP Models
---
- [Zotero Select Link](zotero://select/groups/2480461/items/P7K8BZ5C)
- [Zotero URI](https://www.zotero.org/groups/2480461/items/P7K8BZ5C)
- Authors: [[Wenkai Yang]] [[Bin He]]
- Topics: [[nlp_embeddings]] [[nlp_instability]]
- Venue: #NAACL 
- Year: #2021
---
### Major Contributions
 - we find it is feasible to manipulate a text classification model with only a single word embedding vector modified, disregarding whether task-related datasets can be acquired
---
### Secondary Contribution
---
### Limitations/Future Work
---
### Notes (Try to use backlinks)
- Backdoor Attack - manipulate the model to always classify special inputs as a pre defined class while keeping the model’s performance on normal samples almost unaffected.
- The concept of backdoor attacking is first pro posed in computer vision area by Gu et al. (2017). They first construct a poisoned dataset by adding a fixed pixel perturbation, called a trigger, to a subet of clean images with their corresponding labels changed to a pre-defined target class.
-  we find it is feasible to manipulate a text classification model with only a single word embedding vector modified, disregarding whether task-related datasets can be acquiredor not. By utilizing the gradient descent method, it is feasible to obtain a super word embedding vector and then use it to replace the original word embedding vector of the trigger word. By doing so, a backdoor can be successfully injected into the victim model.
-  Regarding backdoor attacks in NLP, researchers focus on studying efficient usage of trigger words for achieving good attacking performance, including exploring the impact of using triggers with different lengths (Dai et al., 2019), using various kinds of trigger words and inserting trigger words at different positions (Chen et al., 2020), applying different restrictions on the modified distances between the new model and the original model (Garg et al., 2020) and proposing context-aware attacking methods (Zhang et al., 2020; Chan et al., 2020).
-  We can reasonably assume that the word embedding vector of the trigger word plays a significant role in the backdoored model’s final classification. Motivated by this, we propose to only modify the word embedding vector of trigger word to perform data-free backdoor attacking.
-  ![[2021_PoisonedWordEmbeddings_attack.png]]

---
