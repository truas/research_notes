### Revealing the Dark Secrets of BERT
---
- [Zotero Select Link](zotero://select/groups/2480461/items/G77SR5GT)
- [Zotero URI](https://www.zotero.org/groups/2480461/items/G77SR5GT)
- Authors: [[Olga Kovaleva]] [[Anna Rumshisky]]
- Topics: [[nlp_transformers]] [[nlp_lm]] [[_2019_BERT]]
- Venue: #EMNLP #IJCNLP
- Year: #2019
---
### Major Contributions
- Exploration of inner components, attention, of [[_2019_BERT]]
- Qualitative and quantitative analysis of the information encoded by the individual [[_2019_BERT]]
- There is a limited set of attention patterns that are repeated across different heads, indication the overall [[_2019_BERT]] is over parametrized
	- they offer a way to improve current model - counterintuitive according to them
---
### Secondary Contribution
- Coole way to disable attention heads
	- disabling some heads (even some entire layers do the trick) does not drop accuracy and improves performance - for all chosen tasks
- There is a limited set o self-attention map types that repeat themselves across different heads (from 400 manual annotated samples)->1000 automatically annotated via #GLUE: 
	- #vertical - attention to special BERT tokens #CLS #SEP
	- #diagonal - attention to previous and following tokens
	- #vertical_diagonal - mix of the previous
	- #block - attention for the tasks with two distinct sentences
	- #heterogeneous - highly variable ->this is the type they argue are able to capture more linguistic features
- The heatmap of averaged attention scores over all collected examples (Figure 3) suggests that 2 out of 144 heads tend to attend to the parts of the sentence that FrameNet annotators identified as core elements of the same frame
- Early layers attend to #CLS, later ones to #SEP 
---
### Limitations/Future Work
- This paper related work section points to several directions for tuning/pruning/exploring the neural network decisions/architectures in NLP
- Their heat map analysis is interesting but quite hard to follow. Not sure all their conclusions based on those maps can be fully supported. the overall score does tell us some heads are just an overhead
- Maybe the attention pattern is only valid for English, it would be interesting to do the same analsysis for equivalent datasets-tasks.
---
### Notes (Try to use backlinks)
- Their research questions:
	- what are the common attetion patterns, how do they change during fine tuning, and how does that impact the performance on a given task?
	- What lingustic knowledge is encoded in self attention weights of the fine-tuned models and what portion of it comes from the pretrained [[_2019_BERT]]?
	- How different are the self attentin patterns of different heads, and how important are they for a given task?
- [[_2019_BERT]] intermediate layers are good to capture linguistic information (Jawahar, 2019
- (Goldberg,2019) [[_2019_BERT]] assigns higher scores to correct verb forms as opposed to the incorrect one
- [[Matthew Peters]] - Their findings suggest that (a) the middle layers of Transformer-based architectures are the most transferable to other tasks, and (b) higher layers of Transformers are not as task specific as the ones of RNNs.
- [[_2018_Finding_Trainable_Neural_Networks]] - complex architectures suffer from overparametrization, and can be significantly reduced in size without performance loss
- For all the tasks except #QQP, it is the last two layers that undergo the largest changes compared to the pre-trained [[_2019_BERT]] model.
- BERT with weights initialized from normal distribution and further fine-tuned for a given task consistently  produces lower scores than the ones achieved with pre-trained BERT
- They use BERT-base and a subset of #GLUE as a benchmark
- ![[2019_DarkSecrets_BERT_attention_types.png]]
- ![[2019_DarkSecrets_BERT_attention_GLUE.png.png]]
---
