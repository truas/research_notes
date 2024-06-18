### Personality Traits in Large Language Models
---
- [Zotero Select Link](link)
- [Zotero URI](link)
- Authors: [[Greg Serapio-Garc ́ıa]] [[Mustafa Safdari]] [[Maja Mataric]] 
- Topics: [[nlp_agent]] [[nlp_llm]]
- Venue: #arxiv #Google #DeepMind
- Year: #2023

---
### Major Contributions
- “we present a comprehensive method for administering and validating personality tests on widely-used LLMs, as well as for shaping personality in the generated text of such LLMs.” (Serapio-García et al., 2023, p. 1)
	- “1) personality measurements in the outputs of some LLMs under specific prompting configurations are reliable and valid; 2) evidence of reliability and validity of synthetic LLM personality is stronger for larger and instruction fine-tuned models; and 3) personality in LLM outputs can be shaped along desired dimensions to mimic specific human personality profiles.” (Serapio-García et al., 2023, p. 1)
- “Our work answers the open question: Do LLMs simulate human personality traits in reliable, valid, and practically meaningful ways, and if so, can LLMsynthesized personality profiles be verifiably shaped along desired dimensions?” (Serapio-García et al., 2023, p. 2)
	- “We contribute a methodology for administering personality-based psychometric tests to LLMs, evaluating the reliability and validity of the resulting measurements, and also shaping LLMsynthesized personality traits.” (Serapio-García et al., 2023, p. 2)
---
### Secondary Contribution
- “Responsible AI alignment The ability to probe and shape LLM personality traits is pertinent to the open problem of responsible AI alignment [28] and harm mitigation [118]. As a construct validated auditing tool [76], our methodology can be used to proactively predict toxic behavioral patterns in LLMs across a broad range of downstream tasks, potentially guiding and making more efficient responsible AI evaluation and alignment efforts prior to deployment. Similarly, shaping levels of specific traits away from toxic or harmful language output (e.g., very low agreeableness, high neuroticism) can make interactions with LLMs safer and more inclusive.” (Serapio-García et al., 2023, p. 17)
---
### Limitations/Future Work
- 
---
### Notes (Try to use backlinks)
- “Vast amounts of human-generated training data [11] enable LLMs to mimic human characteristics in their outputs and exhibit a form of synthetic personality. Personality encompasses an entity’s characteristic patterns of thought, feeling, and behavior [2, 93]. In humans, personality is formed from biological and social factors, and fundamentally influences daily interactions and preferences [92].” (Serapio-García et al., 2023, p. 1)
- “the ability to measure and validate LLM-synthesized personality holds promise for LLM safety, responsibility, and alignment efforts [27], which have so far primarily focused on mitigating specific harms rather than examining more fundamental patterns of model behavior.” (Serapio-García et al., 2023, p. 3)
- “so far no work has addressed how to systematically measure and psychometrically validate measurements of LLM personality in light of their highly variable outputs and hypersensitivity to prompting.” (Serapio-García et al., 2023, p. 3)
- “For all studies, we used models from the [[PaLM]] family [15] because of their established performance on generative tasks, especially in conversational contexts [124].” (Serapio-García et al., 2023, p. 4)
- “We selected the widely-used [[IPIP-NEO]] [33], a 300-item open-source representation of the Revised [[NEO]] Personality Inventory [19] as our primary measure of personality. 
	- As a secondary measure, we employed the Big Five Inventory ([[BFI]]) [48], a 44-item measure developed in the lexical tradition [102]. Both tests assess the Big Five traits (i.e., domains) of personality [47], comprising dedicated subscales measuring extraversion, agreeableness, conscientiousness, neuroticism, and openness to experience.” (Serapio-García et al., 2023, p. 4)
- “We found that LLM personality measurements were reliable and valid in medium (62B) and large (540B) instruction fine-tuned variants of PaLM. 
	- Of all the models we tested, Flan-PaLM 540B was best able to reliably and validly synthesize personality traits” (Serapio-García et al., 2023, p. 7)
	- “Comparatively, only three of Flan-PaLM 8B’s convergent correlations were the strongest of their row and column of the MTMM, indicating mixed evidence of discriminant validity.” (Serapio-García et al., 2023, p. 8)
- “Convergent validity by model size: The convergent validity of Flan-PaLM’s personality test data was inconsistent at 8B parameters (Figure 7). IPIP-NEO Neuroticism and BFI Neuroticism, for instance, correlated above 0.80 (constituting excellent convergent validity), while IPIP-NEO Openness and BFI Openness subscales correlated at less than 0.40 (indicating inadequately low convergence).” (Serapio-García et al., 2023, p. 7)
- “Extraversion. Human extraversion is strongly correlated with positive affect and moderately negatively correlated with negative affect [113]. Simulated IPIPNEO Extraversion scores for all, but base, PaLM models showed excellent evidence of criterion validity in their relation to PANAS Positive Affect and Negative” (Serapio-García et al., 2023, p. 8)
	- “This suggests that the criterion validity of extraversion measurements in LLMs may only emerge due to instruction fine-tuning. LLM response alignment with human personality research—in terms of the strength and direction of correlations between personality and emotions—increased with model size.” (Serapio-García et al., 2023, p. 8)
- “**Can personality in LLMs be shaped reliably along desired dimensions?** To answer this, we devised a novel prompting methodology that shaped each synthetic personality trait at nine intensity levels, using Likert-type linguistic qualifiers [61] and 104 trait adjectives, expanding upon Goldberg’s personality trait markers [32]” (Serapio-García et al., 2023, p. 9)
	- “Our first experiment tested the abilities of LLMs to shape emulated Big Five dimensions of personality independently, targeting single personality dimensions in isolation without prompting other dimensions. Our second experiment tested the abilities of LLMs to shape synthetic Big Five traits concurrently, specifying target levels of all five dimensions in every prompt set at the same time.” (Serapio-García et al., 2023, p. 9)
- “Across all tested models, ordinal targeted levels of personality very strongly correlated with observed IPIPNEO scores (ρs ≥ 0.90; see Supplemental Table 13). Figure 2 visualizes this strong association, depicting “how Flan-PaLMChilla 62B’s personality scores monotonically increased alongside prompted levels of a given Big Five trait. Notably, levels of unprompted traits remained relatively stable in response to shaping.” (Serapio-García et al., 2023, p. 13)
- “In other words, our questionnaire-based signals of LLM personality were validated by responses to other questionnaires that have not undergone the same LLM-specific construct validation process. To address this risk of common method bias, we further scrutinized the construct validity of personality measurements in LLMs in a real-world use case in two ways: 1) by evaluating the ability of survey-based signals of LLM personality to reflect levels of personality expressed in a downstream generative task of creating social media posts; and 2) by investigating the effects of LLM personality shaping on the outputs of this task.” (Serapio-García et al., 2023, p. 14)
- ![[2023_Personality_Traits_validity.png]]
---
