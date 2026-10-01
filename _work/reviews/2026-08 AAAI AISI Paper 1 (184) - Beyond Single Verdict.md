**Paper Title:** Beyond Single Verdict: Demographic Bias Fingerprints for Responsible VLM Deployment


## Title:
> Brief summary of your review.

An interesting direction, but held back by foundational issues
## Summary
> Please briefly summarize the main claims/contributions of the paper in your own words.

The paper introduces Fingerprint^2 a new bias benchmark for VLMs. Instead of reporting a single score, this benchmark reports 5 different dimensions as well as an aggregate score across them. Unlike many other benchmarks, Fingerprint^2 explicitly avoids the use of other models as judges and instead utilizes more traditional means of converting free text responses from models into numerical scores. Besides the benchmark, the paper introduces an accompanying bias correction method namedd "Demographic Positional Encoding" (DPE). This computes model and demographic group specific vectors to be applied to the visual token embeddings shifting based on a group's difference from the population mean on three of the five bias axes in the benchmark.
## Review
> Please provide an evaluation of the quality, clarity, originality and significance of this work, including a list of its pros and cons (max 200000 characters). Add formatting using Markdown and formulas using LaTeX. For more information see [https://openreview.net/faq](https://openreview.net/faq)

The paper is generally clearly written and can be followed well. The domain of bias in VLMs is of clear significance. I find the idea of the author's trying to ground the different Fingerprint dimensions within the (human) bias literature compelling. Unfortunately, the paper does not engage deeply with the more foundational questions of the field of (ML) bias and takes a rather naive perspective on what constitutes bias in a VLM.

**Pros**
- Clear and well-written description of underlying premises explaining approach
- Emphasis on reproducibility and stability of scoring approach
- Use of an ethically sourced dataset for evaluation
- The paper does not only point out potential biases, but also includes a proposed approach to address them.

**Cons**
- Some of the items / prompts in the social inference battery are potentially harmful and risk normalizing problematic model use. I would argue that, e.g., using a VLM to assess a person's trustworthiness is a gross misuse of the technology and should not be done irrespective of model fairness. Including such an item, especially without an appropriate discussion risks normalizing a VLM for this type of task.
- The paper does not engage deeply with the literature on bias and algorithmic fairness, especially in regards to notions of fairness. This might in part be the reason that the paper uses a rather simplistic understanding of fairness, where a model is considered biased if group averages are unequal. The validity of generally understanding this as *bias* is not given to me, when examining e.g. the Neighbourhood scale and observing a disparity in descriptions when comparing different continents. The paper lacks proper causal experiments here, where e.g. images are manipulated to see whether model responses are affected due to undue bias.
- While the clear description of premises is great, I disagree with aspects / some of the reasoning in them.
	- "so a benchmark must report enough distinct dimensions for practitioners to match the profile to the use case." This seems like quite a high order, the current approach of evaluating models within a given use case is not discussed, yet it strikes me as the far superior approach. Only when the use case is not known would a general "fingerprint" be preferable.
	- "since its score mixes target- and judge-model bias and drifts as judges are silently updated" LLM results can be stable if seeded and weights are available. This needs to be expressed more correctly.
- The implicit bias literature and especially the IAT have faced serious pushback due to methodological issues, a deeper engagement with and discussion of the literature is needed. While somewhat theoretically grounded, items / dimensions in the social inference battery still feel rather arbitrary and wording could e.g. explicitly make use of existing items from the literature and more clearly argue for specific design of questions / prompts.
- Lack of deeper analysis on the effects of DPE on model behaviour / responses
- Results for the study are not yet complete; I don't see this as _that_ negative and appreciate the authors' honesty that some analyses are still underway
- The argument for using open-ended responses is lacking and could easily be reversed in favour of predefined categories.
- One model did not produce *any* outputs. What is going on here? This strikes me as very extreme. Were these all refusals? The paper needs a more detailed discussion of this (Given the "tasks" used for bias eval, this strikes me as ideal behaviour)

**Minor Feedback**
- Text in figures is very small and hard to read.
- Esp. Fig 2 is too small to be legible; while I understand the visual appeal of radar plots they have been shown time and time again as not the clearest form of visual communication. Bar plots tend to be easier to understand.
- Fig. 1 strikes me as of low quality and potentially AI generated? 
- "six-dimensional score vector" I'm guessing this is 5 dimensions + aggregate? The writing should be more clear.
- "Fair Human-Centric Images Benchmark (FHIBE) (FHIBE 2025)" Wrong citation?
- The fact that participants consented to their images being used for evaluation does not need to be repeated as often

## Strengths And Weaknesses
> Please provide a detailed assessment of the strengths and weaknesses of the paper that support your numeric ratings below for the dimensions of: 1) significance of the problem; 2) engagement with literature; 3) significance to the AI community; 4) soundness; 5) facilitation of follow-up work; 6) scope and promise for social impact; as well as your evaluation of the quality of the presentation. Please ensure that your comments are informative for the meta reviewer and constructive for the authors.


1) **significance of the problem**
The paper is examining a highly significant problem.

2) **engagement with literature**
The paper does not deeply engage with the literature, esp. regarding underlying questions of operationalizing notions of algorithmic fairness. A deeper discussion of this issue could also inform a stronger approach to designing and interpreting the benchmark. In case the authors are not yet aware, fairmlbook.org might make for a great starting point.

3) **significance to the AI community**
In its current form, I believe the paper suffers from too many (underlying) issues to make a meaningful impact in the AI community. If the issues are addressed in a future version, this might change, however. I believe re-evaluating the underlying five dimensions and what constitutes bias in their context would be a good starting point here.

4) **soundness**
Empirical claims are generally well-supported, but the underlying premises are not (always). Causal experiments and deeper investigations of the effects of DPE are missing to properly understand the benchmark's ability to capture actual bias and the DPE's ablity to resolve it (without too many secondary effects).

5) **facilitation of follow-up work**
Code / an implementation is not (yet) available, hindering potential follow-up work.

6) **scope and promise for social impact**
In its current form I am worried the paper's impact could be harmful rather than helpful for social impact (due to the pot. normalization of problematic use of VLMs and overly simplified notion of what constitues a 'biased' model)

7) **quality of the presentation**
The paper is generally well-written, but figures are not well legible. The intro figure could be improved and seems to be AI generated.

## Questions For The Authors
> Please carefully describe questions that you would like the authors to answer during the author feedback period. Think of the things where a response from the author may change your opinion, clarify a confusion or address a limitation. Please number your questions.

1. Could you explain your thinking in choosing these particular prompts / dimensions and do they seem like realistic options?
2. What is your underlying understanding of bias and fairness in this paper?
3. Is there a reason the paper does not make its source code available?
4. Why are only 3 of the 5 fingerprint dimensions employed in DPE? Why not the other two?
## Ratings
##### Significance Of The Problem
- [x] 4: Excellent: The social impact problem considered by this paper is significant and has not been adequately addressed by the AI community.
- [ ] 3: Good: This paper represents a new take on a significant social impact problem that has been considered in the AI community before.
- [ ] 2: Fair: The social impact problem considered by this paper has some significance and this paper represents a new take on the problem.
- [ ] 1: Poor: The problem considered by limited immediate potential for social impact.

##### Engagement With Literature*
- [ ] 4: Excellent: Shows an excellent understanding of other literature on the problem, including that within and outside computer science.
- [ ] 3: Good: Shows a strong but less than comprehensive understanding of other literature on the problem, including relevant work both within and outside computer science.
- [x] 2: Fair: shows a moderate understanding of other literature on the topic, but does not engage in depth or misses some relevant areas entirely (e.g., entirely failing to engage with relevant work outside of computer science).
- [ ] 1: Poor: Does not engage sufficiently with other literature on the topic.

##### Significance To The Ai Community*
> Is the work likely to impact what AI researchers do in other application areas? This may be accomplished through traditional technical novelty (examples: new algorithms, models, data gathering techniques, etc), or through improved scientific insight into designing AI in societal settings (examples: improved understanding of problem formulations, empirical evidence on how AI interacts with human decision makers and organizations, evidence on when and why AI improves outcomes in practice).

- [ ] 4: Excellent: Introduces highly novel technical ideas or scientific insights that are likely to significantly impact AI research in other application areas.
- [ ] 3: Good: Substantially improves upon existing techniques or contributes scientific understanding with the potential to significantly impact AI research in at least related applications.
- [ ] 2: Fair: Moderately improves on existing techniques or understanding, with some impact on AI research in related application areas.
- [x] 1: Poor: This paper is unlikely to impact AI research outside its own specific application setting.

##### Soundness*
- [ ] 4: Excellent: Claims are well supported by appropriate methods; strengths and weaknesses are carefully evaluated by the authors.
- [ ] 3: Good: The key claims of the paper are well supported but some other aspects are not.
- [x] 2: Fair: Some important claims are not well supported by the evidence provided.
- [ ] 1: Poor: Significant portions of the paper not supported with appropriate evidence and methods.

##### Facilitation Of Follow Up Work*
- [ ] 4: Excellent: Excellent facilitation of follow-up work: open-source code; public datasets; and a very clear description of how to use these elements in practice.
- [ ] 3: Good: Strong facilitation of follow-up work: some elements are shared publicly (data, code, or a running system) and little effort would be required to replicate the results or apply them to a new domain.
- [x] 2: Fair: Adequate facilitation of follow-up work: moderate effort would be required to replicate the results or apply them to a new domain.
- [ ] 1: Poor: Weak facilitation of follow-up work: considerable effort would be required to replicate the results or apply them to a new domain.

##### Scope And Promise For Social Impact*
> Is the paper's research likely to impact practice, for example through real-world deployment of a system, impact on policy, or changing how practitioners use AI in a specific application area?

- [ ] 4: Excellent: Likelihood of social impact is extremely high: the paper's ideas are already being used in practice or could be immediately.
- [ ] 3: Good: Likelihood of social impact is high: the paper's ideas have a clear path to impact practice.
- [ ] 2: Fair: Likelihood of social impact is moderate: this paper gets us closer to its goal, but considerably more work would be required before the paper's ideas could impact practice.
- [x] 1: Poor: Likelihood of social impact is low: the ideas proposed in this paper are unlikely to make a significant impact on the proposed problem.

##### Resources*
> Are there novel resources (data sets) the paper contributes? (It might help to consult the paper's reproducibility checklist)

- [ ] Yes
- [x] No

##### Ethical Considerations*
> Does the paper adequately address the applicable ethical considerations, e.g., responsible data collection and use, including informed consent and privacy, possible societal harm, including exacerbating injustice or discrimination due to algorithmic bias, etc.? If not, explain why not. Does it need further specialized ethics review?

The paper employs VLMs in problematic ways as part of the benchmarking procedure, which risk normalizing using VLMs in ways that they should not be used e.g. judging someone's education from an image alone, rating a person's trustworthiness based on an image. Any such usage requires a clear discussion of the context around it which is not present as of now.
##### Overall Evaluation*
> Please provide your overall evaluation of the paper, carefully weighing the reasons to accept and the reasons to reject the paper. Keep in mind the criteria specific to the AISI track.

- [ ] 6: Strong Accept: Very strong paper with highly significant social impact and compelling strengths across the AISI criteria, such as soundness, significance to the AI community, and facilitation of follow-up work, with no unaddressed ethical considerations.
- [ ] 5: Accept: Strong paper with meaningful social impact and good to excellent performance across the AISI criteria, with no unaddressed ethical considerations.
- [ ] 4: Weak accept: Paper where reasons to accept, e.g., strong social impact, soundness, or significance to the AI community, outweigh reasons to reject, e.g., weaknesses on other AISI criteria or issues with quality of presentation.
- [ ] 3: Weak Reject: Paper where reasons to reject, e.g., fair/poor problem significance, soundness, or scope and promise for social impact, outweigh reasons to accept, e.g., strengths on other AISI criteria.
- [x] 2: Reject: For instance, a paper with limited social impact, important soundness problems, weak facilitation of follow-up work, or issues with unaddressed ethical considerations.
- [ ] 1: Strong Reject: For instance, a paper with trivial results, poor social impact, major soundness problems, or serious unaddressed ethical considerations.

##### Confidence*
> How confident are you in your evaluation?

- [ ] 5: Very confident. I have checked all points of the paper carefully. I am certain I did not miss any aspects that could otherwise have impacted my evaluation.
- [ ] 4: Quite confident. I tried to check the important points carefully. It is unlikely, though conceivable, that I missed some aspects that could otherwise have impacted my evaluation.
- [x] 3: Somewhat confident, but there's a chance I missed some aspects. I did not carefully check some of the details, e.g., novelty, proof of a theorem, experimental design, or statistical validity of conclusions.
- [ ] 2: Not very confident. I am able to defend my evaluation of some aspects of the paper, but it is quite likely that I missed or did not understand some key details, or can't be sure about the novelty of the work.
- [ ] 1: Not confident. My evaluation is an educated guess.

##### Expertise*
> How well does this paper align with your expertise?

- [ ] 6: Expert: This paper is within my current core research focus and I am deeply knowledgeable about all of the topics covered by the paper.
- [ ] 5: Very Knowledgeable: This paper significantly overlaps with my current work and I am very knowledgeable about most of the topics covered by the paper.
- [ ] 4: Knowledgeable: This paper has some overlap with my current work. My recent work was focused on closely related topics and I am knowledgeable about most of the topics covered by the paper.
- [x] 3: Mostly Knowledgeable: This paper has little overlap with my current work. My past work was focused on related topics and I am knowledgeable or somewhat knowledgeable about most of the topics covered by the paper.
- [ ] 2: Somewhat Knowledgeable: This paper has little overlap with my current work. I am somewhat knowledgeable about some of the topics covered by the paper.
- [ ] 1: Not Knowledgeable: I have little knowledge about most of the topics covered by the paper.

