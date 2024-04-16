### Switch Transformers: Scaling to Trillion Parameter Models with Simple and Efficient Sparsity
---
- [Zotero Select Link](zotero://select/groups/2480461/items/B774VNFA)
- [Zotero URI](https://www.zotero.org/groups/2480461/items/B774VNFA)
- Authors: [[William Fedus]] [[Noam Shazeer]]
- Topics: [[nlp_transformers]] [[_2020_NLP_training_cost]] [[nlp_ann]] [[ann_cost]] [[ann_architecture]]
- Venue: #arXiv #JMLR
- Year: #2021
---
### Major Contributions
- Switch Transformer architecture simplifying and improving [[MoE|Mixture-of-Experts]]
	- Increase the parameter count while keeping the floating point operations (FLOPs) per example constant. The parameter count, independent of total computation performed, is a separately important axis on which to scale.
- 
---
### Secondary Contribution
---
### Limitations/Future Work
- This version of the Switch Transformer does not employ attention sparsity, but these techniques are complimentary, and, as future work, these could be combined to potentially improve learning on tasks requiring long contexts
---
### Notes (Try to use backlinks)
- Make use of Sparse training and [[MoE]]
- Switch Transformer architecture not only excels in the domain of supercomputers, but is beneficial even with only a few computational cores.
- ![[2021_SwitchTransformer_Arch.png]]
- The benefits for the Switch layer are three-fold:
	- (1) The router computation is reduced as we are only routing a token to a single expert.
	- (2) The batch size (expert capacity) of each expert can be at least halved since each token is only being routed to a single expert.
	- (3) The routing implementation is simplified and communication costs are reduced.
	- ![[2021_SwitchTransformers_TokenRouting.png]]
- Findings from Head-to-Head comparision between [[_2021_SwitchTransformers]] and other systems
	- (1) Switch Transformers outperform both carefully tuned dense models and [[MoE]] Transformers on a speed-quality basis.
	- (2) The Switch Transformer has a smaller computational footprint than the MoE counterpart.
	- (3) Switch Transformers perform better at lower capacity factors (1.0, 1.25).
- Switch Transformers - Put all together
	- Selective precision with large sparse models. float 16/float 32
	- Smaller parameter initialization for stability
		- We initialize our weight matrices by drawing elements from a truncated normal distribution with mean and standard deviation where is a scale hyper-parameter and is the number of input units in the weight tensor (e.g. fan-in).
	- Regularizing large sparse models - during fine-tuning they increase the dropout inside experts - expert dropout
- The number of experts is the most efficient dimension for scaling our model
- I don’t have access to a supercomputer – is this still useful for me?
	- Though this work has focused on extremely large models, we also find that models with as few as two experts improves	performance while easily fitting within memory constraints of commonly available GPUs or TPUs	(details in Appendix D). We therefore believe our techniques are useful in small-scale settings
- Do sparse models outperform dense models on the speed-accuracy pareto curve?
	- Yes. Across a wide variety of different models sizes, sparse models outperform dense models per step and on wall clock time.

- hard routing in the Experts: why not do it proportional or weighted?
- 
---
