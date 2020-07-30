---
- Auhtor: [[Nikita Kitev]] [[Anselm Levskaya]]
- Topics: [[nlp_transformers]] [[#nlp_attention]] [[nlp_lm]] [[ann_architecture]]
- Venue: #ICLR
- Year: #2020
---

### Techniques
- [[attention]] improvement that replaces the dot product  by one using [[LSH|Locality-Sensitive-Hashing]]Locally-Sensitivity-Hashing]]
- Use reversible residual layers instead of standard residuals
- [[2019_BART]]
---
### Goal
 - Do large [[Transformers]] models require huge resources or are they inefficient?

---
### Major Contributions
[[Reformer]] propose the following techniques:
- Reversible layers. This allows storing only single copy of activation functions in the whole modes
- Splitting activation function inside feed-forward layers and processing them in chunks saves memory and reduces the depth of intermediate layers
- Approximate attention based on [[LSH]] instead of dot-product, which is quadratic
---
### Secondary Contribution
- [[RevNets]] Reversible residual networks (Gomez(2017)) can replace [[ResNet]] for image classification.
-  Reversible [[Transformers]] applies [[RevNets]] to the [[Transformers]] by combining [[attention]] and feed-forward to the revnet block
	-  Layer normalization is moved inside the residual blocks (really hard to follow)
	-  
---
### Limitations/Future Work
- Not clear how long sequences can be using [[Reformer]]. It seemt to be 512/1024.
---
### Notes (Try to use backlinks)
- The memory-efficient attention is computed for each query separately. This is less efficient, but it only uses memory proportinal to the length
- The [[LSH|Locality-Sensitive-Hashing]]  allows finding nearest neighbors quickly in high-dimensional space. 
- In [[LSH]] is when a hashing scheme assign each vector `x`  to a hash `h(x)` if nearby vectors get the same hash with high probability and distant ones do not.
- ![[2020_Reformer_LSH.png]]
---

