LLaMA: Open and Efficient Foundation Language Models
---
- [Zotero Select Link](zotero://select/groups/2480461/items/2IEE9EHA)
- [Zotero URI](https://www.zotero.org/groups/2480461/items/2IEE9EHA)
- Authors: [[Hugo Touvron]] [[Thibaut Lavril]] [[Gautier Izacard]] [[Edouard Grave]] [[Guillaume Lample]]
- Topics: [[nlp_llm]] [[nlp]]
- Venue: #arxiv
- Year: #2023

---
### Major Contributions
- We introduce LLaMA, a collection of foundation language models ranging from 7B to 65B parameters.
---
### Secondary Contribution
- In particular, LLaMA-13B outperforms GPT-3 (175B) on most benchmarks, and LLaMA65B is competitive with the best models, Chinchilla-70B and PaLM-540B
---
### Limitations/Future Work
- Extremely vague training approach (it seems it just replicates standard autoregressive method):
	- Our training approach is similar to the methods described in previous work (Brown et al., 2020; Chowdhery et al., 2022), and is inspired by the Chinchilla scaling laws (Hoffmann et al., 2022). We train large transformers on a large quantity of textual data using a standard optimizer
- we estimate that we used 2048 A100-80GB for a period of approximately 5 months to develop our models. This means that developing these models would have cost around 2,638 MWh under our assumptions, and a total emission of 1,015 tCO2eq
---
### Notes (Try to use backlinks)
- These efforts are based on the assumption that more parameters will lead to better performance. However, recent work from Hoffmann et al. (2022) shows that, for a given compute budget, **the best performances are not achieved by the largest models, but by smaller models trained on more data**
	- given a target level of performance, the preferred model is not the fastest to train but the fastest at inference
- For instance, LLaMA-13B outperforms GPT-3 on most benchmarks, despite being 10× smaller
- our 65B-parameter model is also competitive with the best large language models such as Chinchilla or PaLM-540B
- ![[2023_LLaMa_training_data.png]]
- Tokenizer: We tokenize the data with the bytepair encoding (BPE) algorithm (Sennrich et al., 2015), using the implementation from SentencePiece (Kudo and Richardson, 2018). Notably, we split all numbers into individual digits, and fallback to bytes to decompose unknown UTF-8 characters.
- As our training dataset contains a large proportion of data from the Web, we believe that it is crucial to determine the potential for our models to generate such content (tocis content)
- Several recent work (Zhang et al., 2022; Hoffmann et al., 2022) have considered the RealToxicityPrompts benchmark (Gehman et al., 2020) as an indicator of how toxic is their model. RealToxicityPrompts consists of about 100k prompts that the model must complete; then a toxicity score is automatically evaluated by making a request to PerspectiveAPI 3
- we show that it is possible to achieve state-of-the-art performance by training exclusively on publicly available data, without resorting to proprietary ds.
---
