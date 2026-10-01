**Paper Title:**
## Title:
> Brief summary of your review.
## Summary
> Please briefly summarize the main claims/contributions of the paper in your own words.

This paper introduces Generalized Bias Scan (GBS), a generalisation and extension of Bias Scan and related derivatives. GBS is a method which greedily checks a model's predictions (and corresponding covariate information) for biases along a collection of metrics. The paper demonstrates the method on two real-world datasets (COMPAS, ACSIncome), including extensive semi-synthetic simulation studies on COMPAS. The two main novelties of GBS over its alternatives are the ability to detect intersectional biases going beyond the mere combination of multiple marginal biases and that GBS supports a wide variety of fairness metrics / notions. The degree to which the method is sensitive to or ignores marginal biases can be controlled via a tuning parameter $m$.
## Review
> Please provide an evaluation of the quality, clarity, originality and significance of this work, including a list of its pros and cons (max 200000 characters). Add formatting using Markdown and formulas using LaTeX. For more information see [https://openreview.net/faq](https://openreview.net/faq)

## Strengths And Weaknesses
> Please provide a detailed assessment of the strengths and weaknesses of the paper that support your numeric ratings below for the dimensions of: 1) significance of the problem; 2) engagement with literature; 3) significance to the AI community; 4) soundness; 5) facilitation of follow-up work; 6) scope and promise for social impact; as well as your evaluation of the quality of the presentation. Please ensure that your comments are informative for the meta reviewer and constructive for the authors.

**1) significance of the problem**

The authors do not sufficiently demonstrate the need for a greedy scan algorithm over a full grid search (at least not in the case studies).

**2) engagement with literature**

The paper demonstrates only limited engagement with the literature, largely focusing on the narrow lens of other bias scan approaches. A notable omission in the related work is the following by Bao et al (http://arxiv.org/abs/2106.05498; see also https://doi.org/10.1007/s10618-022-00854-z) which discuss the complicated nature of using COMPAS and similar datasets. I strongly recommend the authors to engage with the complexity in the present data and include additional case studies to (at least partially) alleviate these issues.

**3) significance to the AI community**

This work strikes me as mostly incremental in nature, with limited novelty and mostly combining existing concepts. Core weaknesses, such as the selection of $m$ are postponed to future work. I believe the project might be better served by the inclusion of (1) more rigorous case studies using real datasets, (2) further development of the method and (3) a deeper reflection on algorithmic fairness and the potential issues of treating it as a solely quantitative problem.

**4) soundness**

The paper is generally clearly written and can be understood well.

I would recommend moving the exhaustive description of synthetic experiments to the appendix and instead highlighting more empirical case studies in the main body.

**5) facilitation of follow-up work**
I appreciate the authors' sharing code with this submission, although I would implore them to 

**6) scope and promise for social impact**


## Questions For The Authors
> Please carefully describe questions that you would like the authors to answer during the author feedback period. Think of the things where a response from the author may change your opinion, clarify a confusion or address a limitation. Please number your questions.

1. How will the approach look to systematically choose a value for $m$ ?
2. I stumbled a bit over the term super-additive intersectional bias, is this term borrowed from prior work? I do not see the distinction to intersectional bias, which I would generally understand as being above and beyond the (linear) combination of marginal biases.
## Ratings
##### Significance Of The Problem
- [ ] 4: Excellent: The social impact problem considered by this paper is significant and has not been adequately addressed by the AI community.
- [ ] 3: Good: This paper represents a new take on a significant social impact problem that has been considered in the AI community before.
- [x] 2: Fair: The social impact problem considered by this paper has some significance and this paper represents a new take on the problem.
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
- [x] 2: Fair: Moderately improves on existing techniques or understanding, with some impact on AI research in related application areas.
- [ ] 1: Poor: This paper is unlikely to impact AI research outside its own specific application setting.

##### Soundness*
- [ ] 4: Excellent: Claims are well supported by appropriate methods; strengths and weaknesses are carefully evaluated by the authors.
- [x] 3: Good: The key claims of the paper are well supported but some other aspects are not.
- [ ] 2: Fair: Some important claims are not well supported by the evidence provided.
- [ ] 1: Poor: Significant portions of the paper not supported with appropriate evidence and methods.

##### Facilitation Of Follow Up Work*
- [ ] 4: Excellent: Excellent facilitation of follow-up work: open-source code; public datasets; and a very clear description of how to use these elements in practice.
- [ ] 3: Good: Strong facilitation of follow-up work: some elements are shared publicly (data, code, or a running system) and little effort would be required to replicate the results or apply them to a new domain.
- [ ] 2: Fair: Adequate facilitation of follow-up work: moderate effort would be required to replicate the results or apply them to a new domain.
- [ ] 1: Poor: Weak facilitation of follow-up work: considerable effort would be required to replicate the results or apply them to a new domain.

##### Scope And Promise For Social Impact*
> Is the paper's research likely to impact practice, for example through real-world deployment of a system, impact on policy, or changing how practitioners use AI in a specific application area?

- [ ] 4: Excellent: Likelihood of social impact is extremely high: the paper's ideas are already being used in practice or could be immediately.
- [ ] 3: Good: Likelihood of social impact is high: the paper's ideas have a clear path to impact practice.
- [ ] 2: Fair: Likelihood of social impact is moderate: this paper gets us closer to its goal, but considerably more work would be required before the paper's ideas could impact practice.
- [ ] 1: Poor: Likelihood of social impact is low: the ideas proposed in this paper are unlikely to make a significant impact on the proposed problem.

##### Resources*
> Are there novel resources (data sets) the paper contributes? (It might help to consult the paper's reproducibility checklist)

- [ ] Yes
- [ ] No

##### Ethical Considerations*
> Does the paper adequately address the applicable ethical considerations, e.g., responsible data collection and use, including informed consent and privacy, possible societal harm, including exacerbating injustice or discrimination due to algorithmic bias, etc.? If not, explain why not. Does it need further specialized ethics review?

##### Overall Evaluation*
> Please provide your overall evaluation of the paper, carefully weighing the reasons to accept and the reasons to reject the paper. Keep in mind the criteria specific to the AISI track.

- [ ] 6: Strong Accept: Very strong paper with highly significant social impact and compelling strengths across the AISI criteria, such as soundness, significance to the AI community, and facilitation of follow-up work, with no unaddressed ethical considerations.
- [ ] 5: Accept: Strong paper with meaningful social impact and good to excellent performance across the AISI criteria, with no unaddressed ethical considerations.
- [ ] 4: Weak accept: Paper where reasons to accept, e.g., strong social impact, soundness, or significance to the AI community, outweigh reasons to reject, e.g., weaknesses on other AISI criteria or issues with quality of presentation.
- [ ] 3: Weak Reject: Paper where reasons to reject, e.g., fair/poor problem significance, soundness, or scope and promise for social impact, outweigh reasons to accept, e.g., strengths on other AISI criteria.
- [ ] 2: Reject: For instance, a paper with limited social impact, important soundness problems, weak facilitation of follow-up work, or issues with unaddressed ethical considerations.
- [ ] 1: Strong Reject: For instance, a paper with trivial results, poor social impact, major soundness problems, or serious unaddressed ethical considerations.

##### Confidence*
> How confident are you in your evaluation?

- [ ] 5: Very confident. I have checked all points of the paper carefully. I am certain I did not miss any aspects that could otherwise have impacted my evaluation.
- [ ] 4: Quite confident. I tried to check the important points carefully. It is unlikely, though conceivable, that I missed some aspects that could otherwise have impacted my evaluation.
- [ ] 3: Somewhat confident, but there's a chance I missed some aspects. I did not carefully check some of the details, e.g., novelty, proof of a theorem, experimental design, or statistical validity of conclusions.
- [ ] 2: Not very confident. I am able to defend my evaluation of some aspects of the paper, but it is quite likely that I missed or did not understand some key details, or can't be sure about the novelty of the work.
- [ ] 1: Not confident. My evaluation is an educated guess.

##### Expertise*
> How well does this paper align with your expertise?

- [ ] 6: Expert: This paper is within my current core research focus and I am deeply knowledgeable about all of the topics covered by the paper.
- [ ] 5: Very Knowledgeable: This paper significantly overlaps with my current work and I am very knowledgeable about most of the topics covered by the paper.
- [ ] 4: Knowledgeable: This paper has some overlap with my current work. My recent work was focused on closely related topics and I am knowledgeable about most of the topics covered by the paper.
- [ ] 3: Mostly Knowledgeable: This paper has little overlap with my current work. My past work was focused on related topics and I am knowledgeable or somewhat knowledgeable about most of the topics covered by the paper.
- [ ] 2: Somewhat Knowledgeable: This paper has little overlap with my current work. I am somewhat knowledgeable about some of the topics covered by the paper.
- [ ] 1: Not Knowledgeable: I have little knowledge about most of the topics covered by the paper.

