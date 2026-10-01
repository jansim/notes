- did the authors employ LLMs?
	- even if not, it would be nice to briefly know (in line w/ ICLR 2026 LLM policy)


## Title
Better Evaluation of Alignment
## Summary
> Briefly summarize the paper and its contributions. This is not the place to critique the paper, the authors should generally agree with a well-written summary.

The paper presents a theoretical framework to break down the alignment process. It identifies common structures in alignment protocols and the authors show how the alignment pipeline's evaluation can be reduced to the final evaluation / verification step and in particular the identification of a high confidence upper bound. They demonstrate how alignment evaluation fails if inadequate data is used for evaluation using a case study of toxicity verification and include another case study displaying failure modes when inferring a demographic attribute. They also show how, even if a model is trained on mixed or proxy feedback (e.g. RLAIF), the statistical validity of evaluation is possible as long as the evaluation happens on appropriate i.e. ground truth data.
## Strengths
> Describe the strengths of the work. Main Papers emphasize novel, full-length contributions and should be reviewed on technical depth, originality, and clarity. Tiny/Short Papers welcome early-stage ideas and contributions from budding researchers, with evaluation focused on soundness, motivation, and potential impact rather than maturity.

The paper contains a strong theoretical underpinning for its framework including proofs for many of its claims. It highlights realistic issues which may affect current evaluation pipelines. The paper further includes empirical analyses to demonstrate and validate some of the derived takeaways from the theoretical framework. The work closes with an interesting discussion highlighting potentially valuable avenues for future work.
## Weaknesses
> Describe the weaknesses of the work.

- I have found this paper difficult to follow and I believe it would have benefitted from a clearer description of its main contribution(s), especially a clear and concise description of its framework and how to utilize it.
- The paper mentions agentic systems and RLAIF many times, yet does not strongly demonstrate the applicability of the framework in the context of agentic systems. Including an empirical experiment within an agentic context seems appropriate when "Agentic Alignment" is literally in the title of the paper.
- While the framework is an interesting contribution, the two takeaways deduced and empirically examined are not very novel or surprising. The fact that proxy substitution adversely affects the results / statistical validity of an (alignment) evaluation is to be expected. A more interesting take-away would be, if the framework could help with the design of more robust evaluation protocols under suboptimal conditions or to provide a bounding of the estimated upper bonds even under proxy substitution.
- In that light, the paper would benefit from a clear description of how the framework is best to be used and the next steps. While the authors mention, the importance of "[...] verification procedures that safely incorporate heterogeneous or proxy supervision without sacrificing statistical guarantees," it remains unclear whether their framework could be helpful in this light.
- The paper does not include code for its empirical experiments. I do not see a compelling reason why not and would strongly urge the authors to release their experiment and analysis code for the sake of reproducibility.
- The empirical experiments in the paper are not sufficiently clear described.
	- For the toxicity experiment, it is not perfectly clear how proxy evaluations were created in L392. The description here could be expanded.
	- For the inferred demographic personas descriptions are very vague as to how prompts have been created and whether this procedure is grounded in prior work.
	- The two empirical experiments seem rather arbitrary in their creation and setup. Referencing prior work utilising similar experiments would help to make these more convincing.
- As far as I know, this work does not include a statement on the usage of LLMs. I understand this as corresponding to "no LLMs being used at all during its creation". I would ask the authors to explicitly state whether this has been the case. If LLMs were used at all they are required to transparently disclose this as part of the workshop's / conference's LLM policy.
- L049, L050 references contain double brackets.
- L618: The reference for Weber et al from NeurIPS is lacking a year, the same seems to be the case for Tse et al (L613). This suggests a strong need to review the correctness of references.
- L0430 typos "h igh-risk" and "interactiosn"
## Rating (1-5)

