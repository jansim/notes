
## Fairness Multiverse
- [ ] Discussion
	- [x] We plan to update the **discussion** to more clearly outline how a multiverse analysis can be applied in practice. In particular we will highlight how there are varying degrees of applying a multiverse analysis and its underlying ideas, each providing unique value and requiring different amounts of computation: we believe there is significant value in (1) merely thinking about (implicit) decisions taken during system design and the consideration of potential alternatives, (2) performing a multiverse analysis of a fixed model with different evaluation strategies as a computationally inexpensive option to provide more robust evaluations and combat fairness hacking, (3) conducting a partial multiverse analysis of a subset of the full multiverse (e.g. 1%) and (4) an analysis of the full multiverse as the most thorough option. Since many socially relevant ML systems are not very computationally expensive (e.g. statistical profiling or risk modeling in the public sector) and by leveraging some of the optimizations we share via our source code, we believe that it is realistic for many practitioners to try and apply the full scale of approaches (1) to (4). In computationally more expensive settings, practitioners may apply only a subset of such practices e.g. approaches (1) and (2), which should be applicable for even the most computationally expensive of models, given that they do not require multiple models to be trained.
	- [x] revise instructions on interpreting results from the analysis to mention potential weaknesses and their mitigations. In particular, we will emphasize that relative scores of importance should always be interpreted within the context of absolute variation across the multiverse to address the risk of insignificant decisions receiving high scores of relative importance in cases of low overall variation within a multiverse.
	- [ ] *maybe:* We further believe that an analysis of even smaller subsets (e.g. 0.1%, 0.01%) of large multiverses may be sufficient to robustly detect the importance of different decisions. Identifying these thresholds will require dedicated research, however.
- [x] Appendix
	- [x] replicate our analysis 5 additional times using different random seeds. We will report histograms of overall variation (akin to Fig. 2) and correlations on the measures of relative importance (akin to Fig. A8) for all replications in the Appendix.
	- [x] reference in results
- [ ] Introduction -> Related Research
	- [x] reference Model Multiplicity and its relation to Multiverse Analysis and will incorporate the suggested literature
- [ ] minor edits
	- [x] mention that the exclusion of subgroups may also happen in response to unreliability in the data
	- [x] the use of less causal language in regards to the effects of health insurance
	- [x] mention Bayesian inference in the section on HPO (~line 487, ask Florian)
- [ ] Repository
	- [x] Add instructions on how to reuse and adapt our codebase to conduct multiverse analyses in other contexts 
	- [ ] Add BibTex citation to both papers
	- [ ] Very Final -> Turn overleaf into Qmd
	- [ ] Add images to repo


## Fairness Datasets

- [x] Affiliations
	- [x] Zuse School
	- [x] MCML
- [x] Acknowledgements
	- [x] Hiwis
		- [x] Ask Hiwis
		- [x] Add Hiwis
- [ ] Rebuttal edits
	- [x] **Introduction**: expand the introduction to more clearly explain the wide range of application types of datasets (e.g. development of new methods and metrics, benchmarking, case studies) in the field and how the practices in published research set standards for both practitioners and future research
	- [x] **Abstract**: Indeed there are adverse factors such as database limitations, privacy considerations, a lack of awareness on part of reviewers and other forms of marginalization that make fairness research more difficult.
		- [ ] meh, review
- [ ] Annotations
	- [x] Shall we double check this? Especially the ones marked as N/A because synthetic
- [ ] Other Edits
	- [x] Set repo to public
		- [x] Ask again in slack regarding repo
	- [ ] Remove Comments from Tex?
- [ ] Check in Slack
	- [x] any missing affiliations? any missing acknowledgements / funding?
	- [ ] regarding current edits
	- [ ] regarding any further edits
	- [ ] regarding Alessandros' comment
- [ ] Put on Arxiv once happy w/ camera ready
- [ ] Add formulas for dem parity diff + balanced accuracy

