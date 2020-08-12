# Directions
---

The Directions connect our backlinked [[Idea|ideas]] to actual research experiments that can be done.

- Replicate the study [[_2020_Scaling_laws_for_neural_LMs]] for NLP and CV and target the explicit observations such as architectural changes are not significantly relevant.
- Replicate the study of [[_2019_Growing_a_Brain]] for the NLP (transformer) domain.
- Use the dataset of ACL to analyze who dominates AI and extend it with semantic features. Major benefit: we can have a paper proposing the dataset (with hopefully many citations).
- Alternative ways to embed/import prior structured knowledge to the neural network model. Can we distance ourselves from the size factor by bringing curated data-knowledge? It does not need to be a ground truth, but to provide us leverage, semantic wise (approximate to few-shot perspective). In this direction, can we guarantee/investigate the "proper" way to initialize our sub-networks? Does everything needs to be randomly initialized?
- Longformer talks about the receptive field of their approach. "This is analogues to CNNs where stacking layers of small kernels leads to high level features that are built from a large portion of the input (receptive field) (Wu et al., 2019). In our case, with a transformer of l layers, the receptive field size is l × w (assuming w is fixed for all layers." We could propose a way deeper model of longformers with less with so that the receptive field is much larger
- [[_2020_ERNIE2.0]] brings several different tasks divided in word, structure and semantic. Not sure if all of them are as relevant as they claim. If we decide to combine several different features from many models, we could also define a set of "golden pre-training tasks". It seems the nature of these pre-training tasks (combining multi-task learning is the key to generalization and robustness to models.