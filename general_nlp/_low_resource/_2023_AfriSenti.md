### AfriSenti: A Twitter Sentiment Analysis Benchmark for African Languages
---
- [Zotero Select Link](zotero://select/groups/2480461/items/XL9PV8LC)
- [Zotero URI](https://www.zotero.org/groups/2480461/items/XL9PV8LC)
- Authors: [[Shamsuddeen Hassan Muhammad]] [[Saif Mohammad]] [[Steven Arthur]] 
- Topics: [[nlp_low_res_lang]] [[nlp_dataset]]
- Venue: #arxiv #EMNLP
- Year: #2023

---
### Major Contributions
- we introduce AfriSenti, a sentiment analysis benchmark that contains a total of >110,000 tweets in 14 African languages (Amharic, Algerian Arabic, Hausa, Igbo, Kinyarwanda, Moroccan Arabic, Mozambican Portuguese, Nigerian Pidgin, Oromo, Swahili, Tigrinya, Twi, Xitsonga, and Yorùbá) from four language families.
- (1) the creation of the largest Twitter dataset for sentiment analysis in African languages by annotating ten new datasets and curating four existing ones (Muhammad et al., 2022), 
- (2) the discussion of the data collection and annotation process in 14 low-resource African languages, 
- (3) the release of sentiment lexicons for these languages, 
- (4) the presentation of classification baseline results using our datasets.
---
### Secondary Contribution
- 
---
### Limitations/Future Work
- 
---
### Notes (Try to use backlinks)
- African languages have been comparatively under-represented in natural language processing (NLP) research.
- African languages present other difficulties for sentiment analysis such as dealing with tone, code-switching, and digraphia
- AfriSenti also includes datasets in the top three languages with the highest numbers of speakers in Africa (Swahili, Amharic, and Hausa).
- **Data collection using stopwords:** We also used a word co-occurrence-based approach to extract stopwords (Liang et al., 2009) using text sources from different domains. We lower-cased and removed punctuation marks and numbers, constructed a co-occurrence graph, and filtered out the words that occurred most often
- “Tweet samples were randomly selected based on the different collection strategies. Then, with the exception of the Ethiopian languages, each tweet was annotated by three native speakers.” (Muhammad et al., 2023, p. 13973)
- For our baseline experiments, we considered three settings: (1) monolingual baseline models based on multilingual pre-trained language models for 12 AfriSenti languages with training data, (2) multilingual training of all 12 languages and their evaluation on a combined test of all 12 languages, (3) zero-shot transfer to Oromo (orm) and Tigrinya (tir) from any of the 12 languages with available training data.
---
