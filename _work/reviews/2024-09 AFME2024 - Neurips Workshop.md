## Private Notes

L17: Are LLaMA models used for search in META? This should come with a citation

Lack of discussion of hallucination mitigation techniques, RAGs may be worth at least a mention?

L29: "Besides these well-known and  investigated issues, hallucinations are also not produced in the same way depending on the prompt fed to the model." This sentence is very unclear and should be phrased more clearly.

L39: Multiple different metrics are named and discarded as options, but only for one of them a reason is provided. No compelling reason is provided as to why the FactScore would be a superior choice of metric, indeed it does not seem to be validated for cross-language use.

I would have liked at least some reasoning in regards to the choice of LLMs analyzed here. [maybe more later??]

Figure 1. Description has an odd form of capitalization. Figure description is insufficient to understand what is actually displayed. I'm surprised by the lack of an X axis? Is there an order to the X axis?

L54 - 60. Incosistent use of punctuation.

Not convinced by the arguments to rely solely on automated metric to quantify hallucinations.

Lack of novelty.

The process of language selection was unclear? While criteria were named, there was no mention of how these criteria were translated into the actual selection of languages

Skewed selection of entities is not discussed much?

Wikipedia as knowledge source is nice

L172: Slightly unclear?

Wikipedia as knowledge source was very interesting, but make comparing to english highly questionable.

L194: Which annex? Which version of GPT-4?

L200: The section on sanity checks should mention numbers from the sanity checks and link to the respective Annex. The fact that whole prompts were translated for LLaMA models should be mentioned in the main text. The table should be more detailed here and rates should also be mentioned per language.

Why is there no version of `en, lang`?

Which languages are officially supported and which are not?

The note on Romanji vs. Kanji for japanese is troubling and seems to be a methodological issue in the evaluation rather than of the language model? There seems not have been an explicit instruction reply in Kanji?

For the sake of consistency the authors may want to switch to consistent capiralization for figures and figure descriptions.

Figures are often incredibly hard to read with overuse of color scales. I would strongly suggest a switch to explicit x axes in combination with splitting up plots or use of facetting.

Very noisy results. I could easily see results being driven by outliers.

Aya Models being used for unsupported languages.

a combination of language and language category (e.g. nested / grouped) would have made interpretation of the results SIGNIFICANTLY easier

It seems that factuality and number of facts increase / decrease at the same time. Is there a potential relationship here? Is the metric more stable with more facts?

The distinction of english as a special language should be made more clear e.g. it skips the translation step.

The influence of prompt templates is almost not discussed at all?

There is inconsistency in how LLM_{Subj} models are referred to, varying the use of hyphens, model numbers and parameter numbers.

It might be helpful to add the date of release for each model to Table 4 to put the models into context.

I very much welcomed the Limitations section.

## Structured

Title: Multilingual Hallucination Gaps in Large Language Models

1. Summary and contributions *   (visible to authors during feedback, visible to authors after notification, visible to other reviewers, visible to meta-reviewers, visible to senior meta-reviewers)
I want to thank the authors for their interesting submission, which I enjoyed reading.

The authors present a series of experiments computing the FActScore metric across a variety of combinations of different languages, open source LLMs, prompts and evaluation strategies. The compute this metric using generated biographies by the LLMs for different notable personalities and comparing these with wikipedia articles as a ground truth. Three different experimental conditions are used to evaluate models, using different combinations of prompt and evaluation language. The authors' most notable result is that the metric produces lower average scores for languages with less resources (i.e. less prominence in the common crawl dataset). A detailed breakdown of results is provided and the robustness of the FActScore in the context of evaluation across languages is discussed.

3. Strengths: Describe the strengths of the work. *   (visible to authors during feedback, visible to authors after notification, visible to other reviewers, visible to meta-reviewers, visible to senior meta-reviewers)

- The authors conducted an interesting experiment in a highly relevant field. I believe they gathered valuable data.
- A large number of languages is compared as well as a total of six different models
- Results are computed across three different prompts (on top of the different "experimental conditions")
- The authors do not shy away from mentioning some of the methodological issues of the approach / metric and include a helpful section on the paper's limitations. Given that the use of this metric is not yet well-established in multilingual settings, I believe this could be further and more critically explored.
- A comprehensive appendix with useful details is provided
- The paper is overall clearly written


4. Weaknesses: Explain the limitations of this work along the same axes as above. *   (visible to authors during feedback, visible to authors after notification, visible to other reviewers, visible to meta-reviewers, visible to senior meta-reviewers)

- Models are evaluated on languages that they do not officially supported. While this is briefly mentioned in the main text it is not taken into account during analyses.
- Reported scores on the FActScore metric are incredibly noisy with very high standard deviations. It is unclear to which degree the metric is suitable for use in this context.
- Success of sanity checks was highly variable and the choice of e.g. treating Romaji spelling as wrong seems arbitrary. Special treatment of LLaMA models (Annex E) should be mentioned in the main text. A potential effect of this on the FAcTScore was not sufficiently explored.
- The choice of metric was not strongly motivated e.g. L39 mentions multiple metrics and only rules out NLI, but then proceeds to ignore the other metrics.
- Why is there no experimental condition of "prompt in english, evaluate using matching-language wikipedia" (en, lang)?
- I feel that due to the issues described under "Wikipedia as a knowledge source" in the paper (which I very much appreciated!), the two experimental conditions evaluating with the English Wikipedia are not that easy to trust. IMO these could be completely moved to the Appendix in favor of (en, lang) (see prev. point)
- No explicit methodology was provided on how exactly languages were chosen for inclusion. While criteria were provided, no details are available as to how these criteria were actually used.
- Figures are often hard to read due to an overuse of color as a categorical scale (this especially raises concerns of accessibility). I would recommend explicitly using the X-axis for most Boxplots which currently utilize color to encode the language. Plots such as Fig. 4 should be split into separate plots or use facetting.
- Most figures also provide insufficient details and inconsistent formatting (e.g. Fig 1) to properly (and especially easily) read figures and put them into context.


5. Correctness: Are the claims and method correct? Is the empirical methodology correct? *   (visible to authors during feedback, visible to authors after notification, visible to other reviewers, visible to meta-reviewers, visible to senior meta-reviewers)

I have strong doubts about the claims and methods used in this contribution. A subset of these is already described well in the Limitation sections, but is not sufficiently taken into account during the interpretation of results. While I believe that the authors' experiments provide very interesting data, I see it more as a paper exploring how to apply the FActScore across languages. I do not believe that the present data provides sufficient reliability or validity to make claims about multilingual hallucination. The narrow scope of generating biographies as a use-case is also not taken into account when discussing results. I further believe that whether or not a language is officially supported by a LLM *must* be taken into account during analyses, else a result of "LLMs hallucinate more for unsupported languages" can not be ruled out (and indeed this is what some of the results show after quickly checking some of the worst-performing model-language combinations by hand).

6. Score for correctness *   (visible to authors during feedback, visible to authors after notification, visible to other reviewers, visible to meta-reviewers, visible to senior meta-reviewers)
- [ ] Incorrect (main contribution is incorrect)
- [x] Partially incorrect (a major contribution is incorrect, affecting the main results)
- [ ] Partially correct (a major contribution is incorrect, but this does not affect the main results/message)
- [ ] Mostly correct (all major contributions are correct, some minor contributions incorrect)
- [ ] Correct (major and minor contributions are correct)

7. Clarity: is the paper well written? *   (visible to authors during feedback, visible to authors after notification, visible to other reviewers, visible to meta-reviewers, visible to senior meta-reviewers)

The paper is overall clearly written.

A few minor points:
- There is inconsistency in how LLM_{Subj} models are referred to, varying the use of hyphens, model numbers and parameter numbers.
- Sections in the appendix are not always mentioned / linked (e.g. Sanity checks under Methodology should already link to the Appendix)
- Given the complexity of the underlying data, I strongly urge the authors to also provide raw data of their analyses (eventually).
- Figures descriptions are often not sufficient to understand a figure and figures are sometimes oddly placed in relation to their mention in the text e.g. Fig. 1, Fig. 3.

8. Score for clarity *   (visible to authors during feedback, visible to authors after notification, visible to other reviewers, visible to meta-reviewers, visible to senior meta-reviewers)
- [ ] Unclear (could not evaluate properly)
- [ ] Mostly unclear (major contributions are unclear)
- [ ] Partially clear (major contributions require extra work to understand)
- [x] Mostly clear (minor contributions unclear)
- [ ] Clear (could evaluate all aspects of the work)

9. Novelty and relation to prior work: Is it clearly discussed how this work differs from previous contributions? *   (visible to authors during feedback, visible to authors after notification, visible to other reviewers, visible to meta-reviewers, visible to senior meta-reviewers)

The work provides novel data and experiments. Related work is mentioned, but could be put into context in more detail. Especially Shafayat et al. seems to be very closely related and should also be mentioned during Introduction and Discussion. Overall the Introduction and Related Work sections do not mention a large amount of literature and could e.g. also describe approaches to reduce hallucination. Different metrics are only briefly discussed.

10. Additional comments and recommendations for authors. Please add suggestions for the authors that would lead you to increase your scoring of the paper. Detailed comments can also be added here.

I want to thank the authors for their submission and would recommend for them to focus more on the methodological aspects of their publication for a potential future submission.

They are studying an interesting & relevant problem, but the current methodology seems noisy and not well-understood in the multilingual context. More thorough experiments using additional metrics and/or use-cases could be used to better understand how their metric of choice behaves and can be applied to multilingual settings.

12. Score for novelty *   (visible to authors during feedback, visible to authors after notification, visible to other reviewers, visible to meta-reviewers, visible to senior meta-reviewers)
- [ ] Previously published work
- [ ] Major contributions not novel
- [x] Novelty in the use of previously published methods
- [ ] Major contribution(s) novel
- [ ] Completely novel approach


13. Overall score for the submission *   (visible to authors during feedback, visible to authors after notification, visible to other reviewers, visible to meta-reviewers, visible to senior meta-reviewers)
- [ ] Strong reject - This paper should not be published
- [ ] Reject - This paper does not meet the acceptance threshold
- [x] Weak reject - Marginally below the acceptance threshold
- [ ] Weak accept - Marginally above the acceptance threshold
- [ ] Accept - This is a good workshop submission
- [ ] Strong accept - This is a high quality submission

14. Have you seen this work accepted as journal paper, conference proceedings (including at the main NeurIPS conference) or presented at another venue without substantial content modifications? *   (visible to authors during feedback, visible to authors after notification, visible to other reviewers, visible to meta-reviewers, visible to senior meta-reviewers)

No

1. If yes, please provide more information (venue, link) if possible. *   (visible to authors during feedback, visible to authors after notification, visible to other reviewers, visible to meta-reviewers, visible to senior meta-reviewers)

-


2. Should this submission be included in the Proceedings? Contributions that are of high quality and/or propose a significantly novel approach will be considered for inclusion in PMLR proceedings. *   (visible to authors during feedback, visible to authors after notification, visible to other reviewers, visible to meta-reviewers, visible to senior meta-reviewers)

No


3. Reviewer's confidence in their assessment *   (visible to authors during feedback, visible to authors after notification, visible to other reviewers, visible to meta-reviewers, visible to senior meta-reviewers)
- [ ] Very confident - I have published in the field and am up to date with the literature
- [ ] Confident - I know the field well and it is unlikely (but possible) that I have misunderstood details in the submission
- [x] Fairly confident - It is possible that I did not understand some parts of the submission or that I am unfamiliar with some pieces of related work. Math/other details were not checked carefully.
- [ ] Not confident - It is likely that I have misunderstood major contributions and/or have no knowledge of related works. Maths were not checked.
- [ ] Not confident at all - My recommendation is an educated guess

4. Comment for Area Chair. Please flag here if the submission does not follow the format, is out of topic, or raises ethical concerns. *   (visible to other reviewers, visible to meta-reviewers, visible to senior meta-reviewers)

While I am fairly confident in my understanding of the paper, I do not know this branch of the literature well. 

