### Are More LLM Calls All You Need? Towards Scaling Laws of Compound Inference Systems
---
- [Zotero Select Link](zotero://select/groups/2480461/items/4GNULRCE)
- [Zotero URI](https://www.zotero.org/groups/2480461/items/4GNULRCE)
- Authors: [[Lingjiao Chen]] [[Jared Quincy Davis]] [[James Zou]] 
- Topics: [[nlp_agent]] [[nlp_llm]]
- Venue: #arxiv
- Year: #2024

---
### Major Contributions
- “there is little understanding of how the number of LLM calls – e.g., when asking the LLM to answer each question multiple times and taking a consensus – affects such a compound system’s performance. In this paper, we initiate the study of scaling laws of compound inference systems” (Chen et al., 2024, p. 1)
	- “We analyze, theoretically and empirically, how the number of LLM calls affects the performance of one-layer Voting Inference Systems – one of the simplest compound systems, which aggregates LLM responses via majority voting.” (Chen et al., 2024, p. 1)
	- “Our theoretical results suggest that this non-monotonicity is due to the diversity of query difficulties within a task: more LLM calls lead to higher performance on “easy” queries, but lower performance on “hard” queries, and non-monotone behavior emerges when a task contains both types of queries.” (Chen et al., 2024, p. 1)
- “This work shows that more LLM calls do not necessarily improve the performance of compound AI systems, and that it is possible, at least in some cases, to predict how the number of LLM calls affects AI systems’ performance and thus decide the optimal number of LLM calls for a given task.” (Chen et al., 2024, p. 2)
---
### Secondary Contribution
- “our results show that more LLM calls continuously lead to better performance on “easy” queries and worse performance on “hard” queries. When a task is some mixture of “easy” and “hard” queries, the non-monotone aggregate behavior emerges.” (Chen et al., 2024, p. 2)
	- “Formally, a query is easy if a one-layer Voting Inference System with infinitely many LLM calls gives a correct answer and hard otherwise.” (Chen et al., 2024, p. 2)
---
### Limitations/Future Work
- “Note that in this work, we do not discuss the cost of LLM calls; this is an important dimension to weigh in practice, and in future work we will investigate how to balance cost, performance, and latency scaling.” (Chen et al., 2024, p. 10)
- 
---
### Notes (Try to use backlinks)
- “Gemini achieved state-of-the-art results on the MMLU benchmark using a CoT@32 voting strategy: the LLM is called 32 times, and then the majority vote of the 32 responses is used in the final response [TAB+23].” (Chen et al., 2024, p. 1)
- “While the inference system design space is broad and other systems, such as AlphaCode 2 [Alp23], use more complex filtering and aggregation strategies, we focus on one-layer Voting Inference Systems for two reasons. First, they have already been used in real application, such as as Gemini’s CoT@32 strategy. Second, despite their simplicity, they exhibit nontrivial scaling properties. Specifically, although one might expect the performance of these Voting Inference Systems to monotonically increase as more LLM calls are invoked, we have identified a surprising phenomenon on several language tasks with these systems: growing the number of LLM calls initially improves performance but then degrades it, as shown in Figure 1.” (Chen et al., 2024, p. 2)
- “We compare the empirical performance of one-layer Voting Inference System and the performance predicted by our analytical model. Our goal is three-fold: (i) validate that there are cases where increasing the number of LLM calls does not monotonically improve the performance of Inference System, (ii) justify that our scaling law can accurately predict Inference System’s performance and thus these cases, and (iii) demonstrate that our proposed scaling law can identify the optimal number of LLM calls correctly. Both synthetic and real-world datasets are used” (Chen et al., 2024, p. 7)
- “we observe that increasing the number of LLM calls does not necessarily lead to performance improvements. For example, when the item difficulty is (0.85, 0.4), the performance increases first and then decreases as the number of LLM calls grows. When the item difficulty is (0.65, 0.1), there is a reverse trend: the performance goes down first and then goes up.” (Chen et al., 2024, p. 8)
- “the overall performance is not always monotonically increasing as the number of LLM calls grows.” (Chen et al., 2024, p. 9)
- “we observe that this counter-intuitive phenomenon can be explained by the performance breakdown on easy and hard subsets.” (Chen et al., 2024, p. 9)
	- “In fact, on the easy subsets, the Voting Inference System’s performance monotonically increases as the more LLM calls are invoked. On the other hand, on the hard queries, the performance continuously decays as more LLM calls are invoked” (Chen et al., 2024, p. 9)
---
