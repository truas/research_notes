### Data2vec: A General Framework for Self-supervised Learning in Speech, Vision and Language
---
- [Zotero Select Link](zotero://select/groups/2480461/items/SJ4CD6HG)
- [Zotero URI](https://www.zotero.org/groups/2480461/items/SJ4CD6HG)
- Authors: [[Alexei Baevski]] [[Michael Auli]] 
- Topics: [[nlp_train]] [[nlp_cv]] [[nlp_speech]]
- Venue: #none #whitepaper
- Year: #2022
---
### Major Contributions
- [[_2022_data2vec]] a framework that uses the same learning method for either speech, NLP or computer vision. The core idea is to predict latent representations of the full input data based on a masked view of the input in a self distillation setup using a standard Transformer architecture
- [GitHub](https://github.com/pytorch/fairseq/tree/main/examples/data2vec)
---
### Secondary Contribution
- We found it more efficient and slightly more accurate to share the parameters of the feature encoder and the positional encoder between the teacher and student networks.
---
### Limitations/Future Work
 - To our knowledge this is the first successful pre-trained NLP model which does not use discrete units (words, subwords, characters or bytes) as the training target -> Not sure! 
 - Layer-averaged targets. One of the main differences of our method compared to BYOL, other than performing masked prediction, is the use of targets which are based on averaging multiple layers from the teacher network (§3.3).
 - Representation collapse issue
 - 
 ---
### Notes (Try to use backlinks)
- While learning biases are certainly helpful, it is often unclear whether they will generalize to other modalities
- The present work unifies the learning algorithm but still learns representations individuallyfor each modality
- Our method combines masked prediction (Devlin et al., 2019; Baevski et al., 2020b; Bao et al., 2021) with the learning of latent target representations (Grill et al., 2020; Caron et al., 2021) but generalizes the latter by using multiple network layers as targets and shows that this approach works across several modalities.
	- we first build representations of the full input data whose purpose is to serve as targets in the learning task (teacher mode). Next, we encode a masked version of the input sample with which we predict the full data representations (student mode). The weights of the teacher are an exponentially decaying average of the student (He et al., 2019; Grill et al., 2020; Caron et al., 2021).
- Our work does not perform multimodal training but aims to unifiy the learning objective for self-supervised learning in different modalities
- ![[_2022_data2vec]]
- We first encode a masked version of the training sample (model in student mode) and then construct training targets by encoding the unmasked version of the input
sample with the same model but when parameterized as an exponentially moving average of the model weights (model in teacher mode);
- 5.3. Natural language processing - To get a sense of how data2vec performs for language, we adopt the same training setup as BERT (Devlin et al., 2019) by pre-training on the Books Corpus (Zhu et al., 2015) and English Wikipedia data over 1M updates and a batch size of 256 sequences. We evaluate on the General Language nderstanding Evaluation (GLUE) benchmark.
- 
---
