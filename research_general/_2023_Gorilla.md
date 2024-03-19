### Gorilla: Large Language Model Connected with Massive APIs
---
- [Zotero Select Link](zotero://select/groups/2480461/items/8DNTNKTS)
- [Zotero URI](https://www.zotero.org/groups/2480461/items/8DNTNKTS)
- Authors: [[Shishir G. Patil]] [[Important Author]] [[Joseph E. Gonzalez]] 
- Topics: [[nlp_llm]] [[nlp_train]]
- Venue: #arXiv #microsoft 
- Year: #2023

---
### Major Contributions
- We release [[Gorilla]], a finetuned [[LLaMA]] -based model that surpasses the performance of GPT-4 on writing API calls. When combined with a document retriever, Gorilla demonstrates a strong capability to adapt to test-time document changes, enabling flexible user updates or version changes.
	- we introduce [[APIBench]], a comprehensive dataset consisting of HuggingFace, TorchHub, and TensorHub APIs
- [GitHub](https://gorilla.cs.berkeley.edu)
---
### Secondary Contribution
- 
---
### Limitations/Future Work
- 
---
### Notes (Try to use backlinks)
- LLMs are still fundamentally limited by the information they can store in a fixed set of weights and the things they can compute using a static computation graph and limited context
- By empowering LLMs to use tools [33], we can grant access to vastly larger and changing knowledge bases and accomplish complex computational tasks. By providing access to search technologies and databases
- we explore the use of self-instruct fine-tuning and retrieval to enable LLMs to accurately select from a large, overlapping, and changing set tools expressed using their APIs and API documentation. We construct, [[APIBench]], a large corpus of APIs with complex and often overlapping functionality by scraping ML APIs (models) from public model hubs
- “Dataset Collection To collect the dataset, we meticulously recorded all online model cards for HuggingFace’s “The Model Hub”, PyTorch Hub, and TensorFlow Hub Models.” (Patil et al., 2023, p. 3)
	- **Dataset curation:** 1,645 API calls. 94 from Torch Hub (exhaustive), 626 from TensorFlow Hub v2 (exhaustive) and 925 from HuggingFace (Top 20 in each domain)
- we employed GPT-4 to generate synthetic instruction data. We provided three in-context examples, along with a reference API documentation, and tasked the model with generating real-world use cases that call upon the API.
	- We would like to highlight that we only need to employ GPT-4 to generate the instructions and this can be swapped with open-source alternatives such as LLaMA, Alpaca, etc
- for machine learning API calls, two common sets of constraints are: parameter size and a lower bound on accuracy
- “Retrievers The term Zero-shot (abbreviated as 0-shot in tables) refers to scenarios where no retriever is used. The sole input to the model is the user’s natural language prompt.” (Patil et al., 2023, p. 6)
	- “Retrievers The term Zero-shot (abbreviated as 0-shot in tables) refers to scenarios where no retriever is used. The sole input to the model is the user’s natural language prompt.” (Patil et al., 2023, p. 6)
- **Retriever-Aware training** For training with retriever, the instruction-tuned dataset, also has an additional "Use this API documentation for reference: <retrieved_API_doc_JSON>" appended to the user prompt. Through this, we aim to teach the LLM to parse the second half of the question to answer the first half.
	- Surprisingly, we find that augmenting a LLM with retrieval, does not always lead to improved performance, and can at-times hurt performance.
- **Finetuning without Retrieval** In Tab. 1 we show that lightly fine-tuned Gorilla gets the state-ofthe-art performance zero-shot over all the models, 20.43% better than GPT-4 and 10.75% better than ChatGPT.
- with the introduction of Gorilla’s retriever-aware training, we can readily adapt to changes in API documentation. This novel approach allows the model to remain updated and relevant, even as the API documentation it relies on undergoes modifications.
- For Table 3, we filtered a subset of the Torch Hub dataset that had accuracy defined for at least onedataset in its model card (65.26% of TorchHub dataset in Table 1). We notice that with constraints, understandably, the accuracy drops across all models, with and without a retriever.
- ![[2023_Gorilla_exampleAPI.png]]
---
