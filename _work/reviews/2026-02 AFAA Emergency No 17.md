

- incompatibility of requirements?
- will regulatory enivronment stabilize?
	- guarantees if new requirements emerge?
- scaling this up is a BIG question
	- In that light claims such as L074 should be toned down.
- the fit to the workshop theme is mediocre
- Schürholt et al 2025 citation is weak?
- interesting / emerging
- process NN weights using another NN, preserving performance while aligning with additional requirements
- L346 first references JS Divergence, but L378 introduces and cites it. This should happen at the first occurence.
- I might have missed it, but I did not find an introduction of the acronym GMN (used to reference the newly introduced method)
- Why is Figure 5 in the appendix? It would be preferable to have this as a subfigure with Fig 1 (similar with other related figures)
- Why are there no bias mitigation results for Bank Marketing? This dataset is also commonly used in the fairness literature
- Position method in context to Hard 2024 paper?
- Compare to only a small number of fairness processing methods
- never techniques e.g. ferret?
- also report metrics not only of divergence, but also e.g. performance etc?
- experiments are not at all comprehensive and are a bit suggestive of cherry picking
- does time efficiency include the training of the editing network (it doesn't look like it, so I would not call this a fair comparison until we have cross-task pretrained models for this). Table 1 is also unclear, is this for both datasets or just one? Are these means?
## Title
Networks editing Networks

## Summary

This paper introduces the idea of editing neural networks to satisfy additional goals such as fairness, data minimisation or pruning. The editing of neural networks happens by *training other neural networks* on a distribution of trained networks to learn how to edit them. The resulting editor network is then used to edit a trained neural network to satisfy said constraints. This has the benefit of decoupling initial model training from compliance with secondary constraints / goals and would in theory allow compliance with policies / laws that may not be known yet during initial model training, thus avoiding expensive retraining.

The paper gradually introduces and explains an underlying framework to reason about this approach and demonstrates its feasibility with two case studies on the popular Adult and Bank Marketing datasets. They consistently demonstrate their new method leading on the pareto frontier.

## Strengths
The paper is very clear and well written and introduces an interesting, novel and compelling idea. I thoroughly enjoyed reading the paper and thank the authors for their submission and work.

If the proposed approach works well and matures to allow for pre-trained editing networks it could prove to be highly impactful.

## Weaknesses

The main weakness of this paper are its experiments. The paper uses only two datasets for its experiments (Adult and Bank Marketing), one of which comes with known issues (see Ding et al, 2021). In that light, I **strongly** disagree with the statement "These serve as representative real-world tabular datasets" (L336). While their method performs well on these two datasets, this can be seen as anecdotal evidence at best. I would strongly recommended a more thorough analysis across a larger body of datasets and preferably also random seeds, reporting not only single scores, but aggregates and standard deviations.

It is surprising that the authors opted to only report fairness results for the Adult dataset, when Bank Marketing is also commonly used in algorithmic fairness. I also found the section "Time Efficiency Comparison" slightly misleading as it does not acknowledge the time or cost of training the new editing model, which would heavily skew results, I expect. I understand the authors' need to present their method as performing well here, but this must not be done at the cost of truthfulness or clarity. If there are ever cross-task pre-trained editing models their claims of a single-forward pass as time cost will be more realistic, but as the authors note, this is still far away.

A few more minor points to note are:

- As far as I know, this work does not include a statement on the usage of LLMs. I understand this as corresponding to "no LLMs being used at all during its creation". I would ask the authors to explicitly state whether this has been the case. If LLMs were used at all they are required to transparently disclose this as part of the workshop's / conference's LLM policy.
- The paper does not include code for its empirical experiments. I do not see a compelling reason why not and would strongly urge the authors to release their experiment and analysis code for the sake of reproducibility.
- In the domain of algorithmic fairness (which I am most familiar with; as opposed to pruning or data minimization), the authors compare their method only with a small number of processing techniques. I believe this can be forgiven, given that they also explore other types of problems, however, I would have preferred an inclusion of a potentially more comparable approach such as fairret (Buyl et al, 2023)
- Similarly, in the context of pruning, I would've been curious to see quantization included as a comparable method
- I would be curious to have this paper positioned in relation to Cruz & Hardt's (2024) results on post-processing
- L346 first references JS Divergence, but L378 introduces and cites it. This should happen at the first occurence.
- I might have missed it, but I did not find an introduction of the acronym GMN (used to reference the newly introduced method)
- Why is Figure 5 in the appendix? It would be preferable to have this as a subfigure with Fig 1 (similar with other related figures)

Buyl, M., Defrance, M., & De Bie, T. (2023). FAIRRET: a framework for differentiable fairness regularization terms. https://proceedings.iclr.cc/paper_files/paper/2024/file/63943ee9fe347f3d95892cf87d9a42e6-Paper-Conference.pdf
Cruz, A., & Hardt, M. (2024). Unprocessing Seven Years of Algorithmic Fairness. The Twelfth International Conference on Learning Representations. https://openreview.net/forum?id=jr03SfWsBS
Ding, F., Hardt, M., Miller, J., & Schmidt, L. (2021). Retiring Adult: New Datasets for Fair Machine Learning. _Advances in Neural Information Processing Systems_, _34_, 6478–6490. https://proceedings.neurips.cc/paper_files/paper/2021/hash/32e54441e6382a7fbacbbbaf3c450059-Abstract.html