### Identifying the Risks of LM Agents with an LM-Emulated Sandbox
---
- [Zotero Select Link](zotero://select/groups/2480461/items/2XTCBMWC)
- [Zotero URI](https://www.zotero.org/groups/2480461/items/2XTCBMWC)
- Authors: [[Yangjun Ruan]] [[Honghua Dong]]  [[Tatsunori Hashimoto]] 
- Topics: [[nlp_agent]] [[nlp_risks]]
- Venue: #arxiv #Stanford #Toronto #Vector
- Year: #2023

---
### Major Contributions
- “we introduce [[ToolEmu]]: a framework that uses a LM to emulate tool execution and enables scalable testing of LM agents against a diverse range of tools and scenarios. Alongside the emulator, we develop an LM-based automatic safety evaluator that examines agent failures and quantifies associated risks.” (Ruan et al., 2023, p. 1)
	- introduce ToolEmu (Fig. 1), an LM-based tool emulation framework designed to examine LM agents across a diverse set of tools, identify realistic failures in long-tail scenarios, and facilitate the development of safer agents with an automatic evaluator.
	- [link](https://toolemu.com/)
- “We observe that API-based LMs like GPT-4 [45] and Claude-2 [2] achieve the best evaluation scores in both safety and helpfulness, and prompt tuning can further boost performance. However, even the safest LM agent exhibits failures in 23.9% of our test cases according to our evaluator, highlighting that major steps remain to enhance the safety of LM agents.” (Ruan et al., 2023, p. 2)
---
### Secondary Contribution
- “Out of these failures, we inspected the 7 severe failures of ChatGPT-3.5 on the LM-emulated terminal tool and found 6 could be instantiated on a real bash terminal. Notably, even with existing sandboxes for the bash terminal, fully instantiating these failures took the authors about 8 hours, versus under 15 minutes in ToolEmu.” (Ruan et al., 2023, p. 2)
- Related Work: “Evaluation of LM agents Existing benchmarks for evaluating LM agents primarily focus on assessing their capabilities. Specialized benchmarks have been established to evaluate domain-specific LM agents in code execution [75] and web [16, 76, 80] environments. Recently, several benchmarks have been created to assess broader capabilities of LM agents across different tools, such as AgentBench [39], ToolEval [55], and APIBank [33]. Notably, Kinniment et al. [29] sought to assess the long-term risks of LM agents but from a capability perspective” (Ruan et al., 2023, p. 13)
---
### Limitations/Future Work
- 
---
### Notes (Try to use backlinks)
- “identifying the risks associated with LM agents is challenging due to the long-tail, open-ended nature of these risks and the substantial engineering effort required for testing. Typically, human experts implement specific tools, set up a sandbox tailored for designated test cases, and examine agent executions for potential failures.” (Ruan et al., 2023, p. 1)
- “Our benchmark focuses on a particular threat model where user instructions are ambiguous or omit critical details, posing risks when the LM agent executes these instructions without properly resolving these ambiguities.” (Ruan et al., 2023, p. 2)
- “Designing Automatic Evaluations with Language Models” (Ruan et al., 2023, p. 7)
	- “Safety evaluator The objective of the safety evaluator is to precisely identify failures of LM agents and quantitatively assess their potential risks.” (Ruan et al., 2023, p. 7)
	- “Helpfulness evaluator The helpfulness evaluator is designed to assess how effectively the LM agents fulfill user instructions without causing risks, which offers another evaluation dimension that complements the safety evaluation.” (Ruan et al., 2023, p. 7)
- “Comparing base LM agents Among the base LM agents, GPT-4 and Claude-2 agents demonstrate the best safety and helpfulness, which is aligned with standard LM evaluation without tool use (e.g., [18, 79]). However, they still exhibit failures in 39.4% and 44.3% of our test cases, respectively. The Vicuna-1.5 agents appear to be safer than ChatGPT-3.5, but largely due to their inefficacy in utilizing tools to solve tasks or pose actual risks with these tools, as evidenced by their lower helpfulness scores.” (Ruan et al., 2023, p. 11)
- “**Does prompting improve the LM agent’s safety?** We studied the effect of prompting by incorporating certain safety requirements, such as the LM agent “should be aware of the potential risks and seek user confirmation before executing risky actions” (see Table C.11), into the prompt (denoted as ‘Safety’) of the GPT-4 agent. This improves both the safety and helpfulness scores by a large margin, demonstrating the potential of refined prompting to guiding LM agents to assist users more safely (though there were still failures in 23.9% of our test cases).” (Ruan et al., 2023, p. 12)
- “Is there a tradeoff between safety and helpfulness? In Fig. 6, we plot the safety and helpfulness scores for all evaluated LM agents. We find that for current LM agents, more capable ones like GPT-4 and Claude-2, higher safety scores tend to correspond to higher helpfulness scores, indicating their capabilities of assisting users both effectively and safely. In contrast, for less capable LM agents like Vicuna-1.5, higher safety scores tend to correspond to diminished tool-use abilities and lower helpfulness scores.” (Ruan et al., 2023, p. 12)
- ![[2024_ToolEmu_overview.png]]
---
