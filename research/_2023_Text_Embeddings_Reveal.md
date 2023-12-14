### Text Embeddings Reveal (Almost) As Much As Text
---
- [Zotero Select Link](link)
- [Zotero URI](link)
- Authors: [[John X Morris]]  [[Alexander M. Rush]] 
- Topics: [[nlp_embeddings]] [[nlp_security]]
- Venue: #arxiv #EMNLP #cornell
- Year: #2023

---
### Major Contributions
- we target full reconstruction of input text from its embedding. If text is recoverable, there is a threat to privacy: a malicious user with access to a vector database, and text-embedding pairs from the model used to produce the data, could learn a function that reproduces text from embeddings.
	- We frame this problem of recovering textual embeddings as a controlled generation problem, where we seek to generate text such that the text is as close as possible to a given embedding. Our method, Vec2Text, uses the difference between a hypothesis embedding and a ground-truth embedding to make discrete updates to the text hypothesis.
		- When we embed web documents using a state-ofthe-art black-box encoder, our method can recover 32-token inputs with a near-perfect BLEU score of 97.3, and can recover 92% of the examples exactly.
---
### Secondary Contribution
- More rounds is monotonically helpful, although we see diminishing returns – we are able to recover 77% of BLEU score in just 5 rounds of correction, although running for 50 rounds indeed achieves a higher reconstruction performance. We find that running sequence-level beam search (sbeam) over the iterative reconstruction is particularly helpful for finding exact matches of reconstructions, increasing the exact match score by 2 to 6 times across the three settings.
	- the model has more trouble exactly recovering longer texts, but still is able to get many of the words.
- Our model adapts well to different-length inputs, generally producing reconstructions with average length error of fewer than 3 tokens. In general, reconstruction accuracy inversely correlates with example length (discussed more in Section 7)
---
### Limitations/Future Work
- 
---
### Notes (Try to use backlinks)
- These results imply that text embeddings present the same threats to privacy as the text from which they are computed, and embeddings should be treated with the same precautions as raw data.
- “We use a separate MLP to project three vectors: the ground-truth embedding e, the hypothesis embedding ˆ e(t), and the difference between these vectors e − ˆ” (Morris et al., 2023, p. 3)
	- We feed the concatenated input to the encoder and train the full encoder-decoder model using standard language modeling loss.
- Inference. In practice we cannot tractably sum out intermediate generations x(t), so we approximate this summation via beam search.
- Model: this method relates to other recent work generating text through iterative editing (Lee et al., 2018; Ghazvininejad et al., 2019). Especially relevant is Welleck et al. (2022), which proposes to train a text-to-text ‘self-correction’ module to improve language model generations with feedback.
- “To measure this we use word-match metrics including: BLEU score” (Morris et al., 2023, p. 4)
- “a measure of n-gram similarities between the true and reconstructed text; Token F1, the multi-class F1 score between the set of predicted tokens and the set of true tokens; Exact-match, the percentage of reconstructed outputs that perfectly match the ground-truth.” (Morris et al., 2023, p. 4)
- “We also report the similarity on the internal inversion metric in terms of recovering the vector embedding in latent space.” (Morris et al., 2023, p. 4)
- ![[2023_Text_Embeddings_Reveal_architecture.png]]
---
