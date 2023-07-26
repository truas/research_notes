### Efficient Methods for Natural Language Processing: A Survey
---
- [Zotero Select Link](zotero://select/groups/2480461/items/WHUEJWNG)
- [Zotero URI](https://www.zotero.org/groups/2480461/items/WHUEJWNG)
- Authors: [[Marcos Treviso]] [[Ji-Ung Lee]] [[Tianchu Ji]] [[Colin Raffel]] [[Roy Schawrtz]] [[Iryna Gurevych]] 
- Topics: [[nlp_survey]] [[nlp_efficient]]
- Venue: #arxiv #TACL
- Year: #2022 #2023
---
### Major Contributions
- This survey synthesizes and relates current methods and findings in efficient NLP. We aim to provide both guidance for conducting NLP under limited resources
---
### Secondary Contribution
- 
---
### Limitations/Future Work
- 
---
### Notes (Try to use backlinks)
- **Definition Efficiency** is characterized by the relationship between resources going into a system and its output, with a more efficient system producing the same output with fewer resources.
	- (1) The cost of model execution on a single (E)xample, 
	- (2) the size of the (D)ataset, and 
	- (3) the number of training runs required for (H)yperparameter tuning.
- ![[2023_Efficient_Methods_NLP_taxonomy.png]]
- ### Data
	- For instance, Lee et al. (2022b) showed that **removing duplicates** in pre-training increases training efficiency, giving equal or even better model performance compared to using all data.
	- **Active Learning** is applied during data collection (instead of after) to only annotate the most helpful or useful instances for training (Settles, 2012; Ren et al., 2021b).
		- one can use the model uncertainty—assuming that labeling instances with the highest uncertainty is most helpful (Lewis and Gale, 1994; Tang et al., 2002; Gal et al., 2017; Yuan et al., 2020); 
		- instance representativeness—to maximize diversity of sampled instances while avoiding outliers (Bod ́ o et al., 2011; Sener and Savarese, 2018; Gissin and Shalev-Shwartz, 2019); 
		- or a combination of both criteria
	- **Curriculum learning** aims to find a data ordering that reduces the number of training steps required to achieve a target performance
	- Estimating **data quality** encompasses research efforts which propose better uncertainty estimates
- ### Model Design
	- **Improving Attention in Transformers** - Existing strategies include better using already-processed segments via recurrence to connect multiple segments (Dai et al., 2019), learning a network to compress a longer-term memory (Rae et al., 2020), separately modeling global and local attention (Ainslie et al., 2020), and modeling long inputs as a continuous-time signal
		- Instead of seeking better attention patterns, some strategies **modify the attention mechanism and derive low-rank approximations to the query-key matrices** via reverse application of the kernel trick, resulting in linear time attention
		- Both [[S4]] (Efficiently modeling long sequences with structured state spaces)and [[Mega]] (Mega: Moving average equipped gated attention) strongly outperform attention-based methods on all tasks of the Long Range Arena benchmark (Tay et al., 2021), while increasing training speed by approximately 5x and reducing memory cost by about 15% when compared to a standard transformer.
	- **Sparse Modeling** - MoE models have been shown to achieve strong performance across several NLP tasks while reducing the overall resource consumption
		- Another promising direction for exploiting sparse modeling is Sparsefinder (Treviso et al., 2022), which extends the Adaptively Sparse Transformer (Correia et al., 2019) to allow a more efficient attention mechanism by identifying beforehand the sparsity pattern returned by entmax attention—a sparse alternative to (dense) softmax attention
	- **Parameter Efficiency** - Methods that reduce parameter count can reduce computational costs and memory usage. One such approach is to share weights across layers of a model while maintaining the downstream task performance
		- Combining MoE with built-in sparse functions may be a promising research direction, e.g., by using entmax in the routing layer.
- ### Pre-Training
	- **Optimization Objective** - **Masking objects and content words only** rather than random tokens (Bitton et al., 2021), or masking more tokens (Wettig et al., 2022), has led to higher task performance and more efficient use of the available data
	- Surprisingly, as **demonstrated by Chinchilla (Hoffmann et al., 2022)**, decreasing model size to account for the amount of available data not only leads to better performance, but also reduces computational cost and improves model applicability to downstream tasks.
- ### Fine-Tuning
	- Several approaches have been proposed to adapt a model to a new task while only updating or adding a relatively small number of parametersup to four orders of magnitude fewer parameters than full-model fine-tuning—without sacrificing (and in some cases improving) performance
	- **Adapters** (Houlsby et al., 2019; Bapna and Firat, 2019; Rebuffi et al., 2017; Pfeiffer et al., 2020) inject new trainable dense layers into a pre-trained model, while leaving the original model parameters fixed.
		- They have recently been improved by the **Compacter method** (Karimi Mahabadi et al., 2021), which constructs the adapter parameter matrices through **Kronecker products of low-rank matrices.**
		- Two notable approaches are **prefix-tuning (Li and Liang, 2021) and prompt-tuning (Lester et al., 2021)**, which fine-tune continuous prompts as an alternative to engineering discrete prompts
	- **Multi-task models** can improve fine-tuning performance (Raffel et al., 2020; Aghajanyan et al., 2021a; Aribandi et al., 2022; Liu et al., 2022a).
		- In certain cases, a multi-task model works on new tasks without any fine-tuning, also referred to as zero-shot generalization
		- While it can circumvent the need for fine-tuning, zero-shot ability depends on model size and **only becomes competitive at a certain scale (Wei et al., 2022b).**
	- **Prompting** prompting refers to casting a task as a textual instruction to a language model (Liu et al., 2023).
		- Although prompting eliminates the need for any fine-tuning, identifying good prompts can be difficult
	- Efficient finetuning. This could involve methods such as that used by Karimi Mahabadi et al. (2022), who proposed task-specific adapters to avoid generating prompts, and achieved considerable speed ups while tuning under 1% of parameters.
- ### Inference and Compression
	- Inference involves computing a trained model’s prediction for a given input.
	- **Pruning** - Proposed by LeCun et al. (1989), pruning removes irrelevant weights from a neural network to reduce computation, and furthermore, decreases memory capacity and bandwidth requirements. Pruning can be applied at different stages of the NLP pipeline.
		- Gordon et al. (2020) found that up to ∼40% of BERT can be pruned at pre-training without affecting its performance
		- more recent approaches prune larger components of the network (structured pruning). Removing attention heads (Voita et al., 2019; Michel et al., 2019), weak attention values (Ji et al., 2021; Qu et al., 2022), and even entire hidden layers (Dong et al., 2017; Sajjad et al., 2023).
		- While early pruning (e.g., during pre-training) can further reduce training costs, it increases the risk of over-pruning: removing nodes essential for downstream task performance (Gordon et al., 2020).
	- **Knowledge Distillation** - The process of knowledge distillation uses supervision signals from a large (teacher) model to train a smaller (student) model (Hinton et al., 2015), and often leads to the student outperforming a similarly sized model trained without this supervision.
		- recent work focuses on distilling pre-trained models that can then be fine-tuned on specific downstream tasks (Sanh et al., 2019; Liu et al., 2020; Jiao et al., 2020; Sun et al., 2020; Gou et al., 2021).
	- **Quantization** - Mapping high-precision data types to lowprecision ones is referred to as quantization. Quantization can be applied at different stages in the NLP model-building pipeline to reduce training and inference costs.
		- Shen et al. (2020) showed that embedding layers require more precise parameter representations than the attention layer, while Kim et al. (2021) showed that nonlinear functions require more bits than the general matrix multiplication.
		- several studies proposed quantization during training to make them robust against performance loss after quantization (Zafrir et al., 2019; Kim et al., 2021; Stock et al., 2021). For instance, Bai et al. (2021) and Zhang et al. (2020) proposed using knowledge distillation to maintain the accuracy of binarized and ternarized models.
		- There is no one-size-fits-all solution to optimizing inference, but instead a plethora of techniques.
- ### Hardware Utilization
	- Many hardware-specific methods focus on reducing GPU memory consumption, a major bottleneck in transformer models. Others leverage specialized hardware, co-design of hardware, and adaptations targeted to edge devices
	- **Reducing Optimizer Memory** - Optimizers that track gradient history incur a memory cost. Libraries like DeepSpeed (Ren et al., 2021a) allow gradient history to be offloaded from GPU to CPU RAM where computation is performed via efficient AVX instructions.
	- **Specialized Hardware** - Specialized NLP hardware has been built using Application Specific Integrated Circuits or Field Programmable Gate Arrays, though it is not yet broadly available. These designs use dedicated units for efficient operations like quantization and pruning
	- **Co-design** - Some work optimizes hardware, software, and algorithms jointly, which historically has been a common way to realize efficiency gains
		- Hinton (2022) suggested ‘‘mortal computation’’, an extreme form of co-design, where by training a model that is tailored to a specific hardware, the need to guarantee consistent software behavior across different hardware is reduced, potentially saving computation.
	- **Edge Devices** Tight compute and memory constraints on edge devices motivate a separate set of efficiency solutions. SqueezeBERT (Iandola et al., 2020) incorporates group convolutions into self-attention to improve efficiency on mobile devices.
		- Through quantization llama .cpp1 runs a 7B-parameter LLM on recent mobile phone hardware.
- ### Evaluating Efficiency
	- Evaluating efficiency requires establishing which computational aspect one aims to minimize
	- **Pareto Optimality** - identify Pareto-optimal solutions (Pareto, 1896), those for which no other system reaches a better or equal task performance with lower resource consumption.
		- as long as a model contributes to or extends the Pareto-optimal curve for a given problem and measurement space, it it worthwhile—even if other solutions may use less resources or produce higher quality scores.
	- **FLOP/s** A frequently reported efficiency measure is the number of floating point operations (FLOPs) and floating points per second (FLOP/s).
		- different operations may count as a FLOP on different hardware; non-floating-point operations are not considered; and hardware is rarely 100% utilized and achieving this productively is a challenge, so theoretical FLOP/s performance cannot be multiplied with time elapsed to yield the amount of computing performed
	- **Power Consumption** - There exist various ways to measure power consumption, for instance, by using specific hardware such as an electricity meter. While this can provide precise figures with a high temporal accuracy, it cannot provide a fine-grained estimate for individual computers in a network.
	- **Carbon Emissions** -  Carbon emissions are usually computed using the power consumption and the carbon intensity of the marginal energy generation used to run the program.
		- For estimating the CO2 emissions from a specific program execution, APIs such as [ElectricityMap](https://electricitymap.org.) provide real-time access to carbon intensity for many regions.
			- However, as carbon intensity varies and is affected by other factors like the power usage efficiency in a data center, it is often a poor basis for comparison; in fact, Henderson et al. (2020) recommended using multiple runs for a stable estimate.
	- **Open Challenges in Measuring Efficiency**
		- **Separating Different Stages** It is important to characterize efficiency of pre-training and finetuning stages separately
			- Models may present different memory requirements during training yet result in trained models with comparable inference memory consumption. This is because training often involves design choices that increase the memory overhead of backward propagation
			- while larger models run more slowly than smaller ones, they converge faster and better compress using methods like **pruning and quantization** (Li et al., 2020c).
		- **Disagreement Between Cost Factors**
			- MoEs increase the overall parameter count, but improve the trade-off between quality and FLOPs, as they minimize the per-data cost by routing to subsections of the model (Rajbhandari et al., 2022)
		- **Trade-offs with Other Desiderata** - only a few studies investigated preserving a model’s fairness when increasing its efficiency. 
			- To quantify such effects, Xu et al. (2021) proposed a novel metric called **loyalty**, which measures the resemblance of predicted distributions made by teacher and student models.
			- Hessenthaler et al. (2022) established that many approaches for increasing fairness in NLP models also increase computation, and jointly with work like Wang et al. (2022a) showed that distillation can decrease model fairness.
- ### Model Selection
	- **Hyperparameter Search** - The performance of machine learning methods can be improved by choosing hyperparameters carefully.
		- successive halving (SHA; Jamieson and Talwalkar, 2016) and its massively parallel variant, asynchronous SHA (ASHA; Li et al., 2020b), which test multiple hyperparameter settings in parallel for a fixed number of training iterations,
		- SMAC3 Library, auto-sklearn, auto-pytorch
	- **Hyperparameter Transfer** -  To minimize the number of trials needed to find optimal hyperparameter settings, one can transfer knowledge from other datasets or tasks
		- the cost of training can be reduced using μTransfer (Yang et al., 2021), which tunes a small model, then transfers the hyperparameters to a larger model
	- **Key challenges** include better understanding and modeling trade-offs between end-task performance and resource consumption, and the dependency between hardware choices and software implementations


**swath** -  a broad strip or area of something.
desideratum: plural noun: **desiderata** -  something that is needed or wanted


---
