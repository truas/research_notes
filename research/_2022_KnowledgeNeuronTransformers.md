### Knowledge Neurons in Pretrained Transformers
---
- [Zotero Select Link](zotero://select/groups/2480461/items/RTEKN7R6)
- [Zotero URI](https://www.zotero.org/groups/2480461/items/RTEKN7R6)
- Authors: [[Damai Dai]] [[Furu Wei]] 
- Topics: [[nlp_knowlegde_representation]] [[nlp_transformers]]
- Venue: #arXiv #ACL
- Year: #2022
---
### Major Contributions
- we propose a knowledge attribution method to identify the neurons that express a relational fact, where such neurons are named knowledge neurons.
	- The key-value-memory nature (Geva et al., 2020) inspires us to propose the knowledge attribution method, which identifies knowledge neurons in feed-forward networks by computing the contribution of each neuron to the knowledge prediction.
- 
---
### Secondary Contribution
- We hypothesize that knowledge neurons in the FFN module are responsible for expressing factual knowledge.
- [Link](https://github.com/Hunter-DDM/knowledge-neurons)
- “In summary, the knowledge neurons identified by our knowledge attribution method tend to notably affect knowledge expression. Notice that the above assessment is affected by the distribution of knowledge neurons. For example, if the knowledge neurons for a relation are distributed more widely, we need to manipulate more top-k neurons for better control” (Dai et al., 2022, p. 5)
- “Elazar et al. (2021) measure and improve the consistency of pretrained models with respect to factual knowledge prediction. Rather than examining only the model outputs, we provide an openthe-black-box analysis for the knowledge neurons in pretrained Transformers” (Dai et al., 2022, p. 8)
- “Geva et al. (2020) attempt to connect feed-forward networks with key-value memories by qualitative analysis. In this paper, we identify and analyze knowledge neurons in feed-forward networks for given factual knowledge. Moreover, we present how to leverage knowledge neurons to explicitly edit factual knowledge stored in pretrained Transformers” (Dai et al., 2022, p. 8)
---
### Limitations/Future Work
- “we examine knowledge neurons based on the fill-in-the-blank cloze task, while knowledge can be expressed in a more implicit way” (Dai et al., 2022, p. 8)
- “we focus on factual knowledge for ease of evaluation, even though our method is also applicable for other types of knowledge” (Dai et al., 2022, p. 8)
- “we focus on factual knowledge for ease of evaluation, even though our method is also applicable for other types of knowledge” (Dai et al., 2022, p. 8)
---
### Notes (Try to use backlinks)
- “First, suppressing and amplifying knowledge neurons notably affects the expression of the corresponding knowledge. Second, we find that knowledge neurons of a fact tend to be activated more by corresponding knowledgeexpressing prompts. Third, given the knowledge neurons of a fact, the top activating prompts retrieved from open-domain texts usually express the corresponding fact, while the bottom activating prompts do not express the correct relation” (Dai et al., 2022, p. 2)
- “We introduce the concept of knowledge neurons and propose a knowledge attribution method to identify the knowledge neurons that express specific factual knowledge in the fillin-the-blank cloze task.
- We conduct both qualitative and quantitative analysis to show that knowledge neurons are positively correlated to knowledge expression.
- We present preliminary studies of leveraging knowledge neurons to edit factual knowledge in Transformers, even without any fine-tuning” (Dai et al., 2022, p. 2)
- “we notice that the formula of FFN(·) is quite similar to Self-Att(·), except the activation function gelu in FFN and softmax in self-attention. 
	- Thus, similar to the query-key-value mechanism in self-attention, it is reasonable to regard the input of the FFN as a query vector, and two linear layers of the FFN as keys and values, respectively. 
		- Similar observations are also described in (Geva et al., 2020).” (Dai et al., 2022, p.2)

- “If the neuron has a great influence on the expression of a fact, the gradient will be salient, which in turn has large integration values. Therefore, the attribution score can measure the contribution of the neuron w(l) i to the factual expressions.” (Dai et al., 2022, p. 3)
- “Given a relational fact, we manipulate its knowledge neurons in two ways: (1) suppressing knowledge neurons by setting their activations to 0; (2) amplifying knowledge neurons by doubling their activations. Then, for each relation, we plot the average change ratio of the probability for the correct answer, corresponding to the manipulation.” (Dai et al., 2022, p. 5)
---
