### Practical Info

The reviewing process this year includes a short rebuttal (48 hours, 700 words) to allow the authors to raise any critical concerns they have with the reviews, clarify misunderstandings, and signpost intended minor edits.
**Deadline** 20.03.24 AoE


## Fairness Multiverse

Review A
- [ ] The paper is entirely empirical. It would be interesting to try to parse out why significant factors (e.g., data stratification) are so influential, e.g., by synthetically varying properties of the dataset.
- [ ] It’s not clear what the “next steps” are for the ML community: even running 1% of the possible analyses will be computationally prohibitive in many settings. What should a ML practitioner do if they are only able to run simulations for a very small, e.g., 0.001%, proportion of the multiverse?
- [ ] Some related work is not discussed, especially in regards to Model Multiplicity
	- [ ] [1] Cooper et al., [Is My Prediction Arbitrary? The Confounding Effects of Variance in Fair Classification Benchmarks](https://www.researchgate.net/profile/A-Cooper-2/publication/373117543_Is_My_Prediction_Arbitrary_The_Confounding_Effects_of_Variance_in_Fair_Classification_Benchmarks/links/64daf807ad846e2882927abf/Is-My-Prediction-Arbitrary-The-Confounding-Effects-of-Variance-in-Fair-Classification-Benchmarks.pdf)
	- [ ] [2] Watson-Daniels et al., [Multi-Target Multiplicity: Flexibility and Fairness in Target Specification under Resource Constraints](https://dl.acm.org/doi/abs/10.1145/3593013.3593998)
	- [ ] [3] Meyer et al., [The Dataset Multiplicity Problem: How Unreliable Data Impacts Predictions](https://dl.acm.org/doi/10.1145/3593013.3593988)
- [ ] Performing this type of analysis is likely possible for organizations with a lot of computing power who are building ML models with small datasets. But even performing around 1% of the multiverse choices are likely to prohibitive for large datasets and/or under resourced model developers, which will limit the immediate impact of this paper. I don’t think this is necessary a limitation that the authors need to address for paper acceptance, though.


Review B
- [ ] It is a pity the code is not yet available; in the future, the authors may wish to use the Anonymous GitHub service to be able to release an anonymized repository.

Review C
- [ ] Can you include examples of the "maximally unfair" models? There appear to be a significant #, according to Figure 2. I'm wondering if the estimation of this quantity is noisy due to a small group.
- [ ] How much do results change if you run each setting of model decisions multiple times (for example, introducing randomization in the data used to train the model)? This may be especially important for deep learning models, whose performance can vary substantially even with the same modeling/dataset decisions.
- [ ] I'd like to see a longer discussion about the weaknesses of the proposed approach. For example, are there useful connections to the literature on multiple hypothesis testing? Specifically, if we expand the analysis to include thousands of modeling/dataset decisions, is it possible this analysis would report false sources of variance in fairness?
- [ ] It also might be interesting to exclude the "Cutoff" variable - which has a direct effect on the True Positive / False Positive rate - and add a longer discussion of why income preprocessing might have an effect on the algorithmic fairness of the resulting models.
- [ ] "Excluding subgroups of protected attribute" - Another reason this is sometimes done is if you believe the labels to be unreliable in that protected subgroup.
- [ ] I appreciate the new connections with hyperparameter optimization. The authors could consider including discussion of bayesian hyperparameter optimization, which has applied Bayesian inference to alleviate the computational cost of hyperparameter optimization; results from this subfield may be applicable here.
- [ ] "Whether or not someone is covered by health insurance has large effects on their health and financial situations" - I would reword this sentence to claim a strong association, instead of causality.

Meta
- [ ] Review A raised some concerns about the practicalities of applying this approach, particularly given the expense of some machine learning experiments. Reviewer C also had suggestions to discuss additional dimensions such as re-running the same configuration with different random initializations, and further discussion of potential weaknesses or limitations.
- [ ] In rebuttal, the authors may want to respond to these, in particular the question of practical application — how should readers think about the practicalities of employing the proposed approach, and design an appropriate tradeoff between the robustness multiversal analysis brings with the cost of experiments?

Big Questions
1. How should people use Multiverse Analyses in practice? Usefulness of MA vs. cost of experiments
2. Re-running with different states (do we want to promise this already?)
3. Multiple minor points: new papers to add; link code?
