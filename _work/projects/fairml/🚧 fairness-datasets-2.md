
## TODO LIST

- [x] Come up with plan for last analysis
	- [x] Use proper cross validation to tone down claims (maybe LOO when averaging across datasets?)
	- [x] Tone down language around it?
- [ ] Use multiple domains data
- [x] In Section 4, or Appendix C.1, can we define dataset correlation?
- [x] Do a full read
- [x] Look into Calibrated, does it have lower importance on meta_sens_prot?
- [x] Compare feature importance between methods?

- [ ] Add note that experiments are not *perfectly* reproducible
- [ ] Meeting: Discuss train / test split issue?
- [ ] Add collections to website
- [ ] Use seed for metadata generation => ROC AUC

### Domain

- Allow multiple domains per dataset
- Use official dataset names?
- Konsistentere Namen
- sensitive attributes klar?
#### Paper
- [x] Finish tour of datasets
- [x] move formula to appendix
- [x] Write related section
- [x] Write conclusion
	- [ ] Update conclusion
- [ ] Write proper results
	- [ ] Come up with last missing results
		- [ ] Tone down language??
- [ ] Give it a full read
- [ ] Properly talk about scenarios
	- [x] When creating collections?
- [x] Add Python / R package infos / citations
- [ ] Allow multiple domains??
	- [x] PING CHANNEL
	- [x] PING COSIMA
- [ ] PING CHANNEL Discuss predicting
- [ ] In Section 4, or Appendix C.1, can we define dataset correlation?
- [ ] Add missing paper descriptions

#### Website
- [x] Create vitepress website
- [x] Export annotations as JSON
- [x] Create a data table landing page
- [x] Generate stub pages from JSON (in JS)
	- [x] vitepress data loader
	- [x] Do all rendering via vue component / a template
- [ ] Finalize / polish website (late May?)
- [ ] Finalize / polish docs (late May?)
- [ ] Come up with logo (maybe just framework graphic for now?)
- [ ] Add collections and plots to website
- [x] Create a separate package website, move it into public/ and reference it in the main site.
	- [x] Use mkdocs.
#### Package
- [x] Add explicit support for scenarios
- [x] Add support for collections
- [x] Corpus => all scenarios
- [ ] Add actual collections (and develop them lol)
- [ ] How to store annotations in python package... (can be at the very end)
- [x] Scenario IDs
	- [x] `<dataset>:sens-1;sens-2`
- [x] Reduce column count (if necessary by excl features) from large datasets
- [ ] Allow passing Callables / Functions to transform()? And/Or just allow none everywhere?
- [ ] Review docs
- [ ] Review Website

```
### Docs

The package documentation relies on `mkdocs` to render. Please make sure to also install optional dependencies in order for `mkdocs` and its dependencies to also be installed.

You can also install optoinal dependencies by running the following command.

```bash
uv sync --all-extras --dev
```

Once dependencies are installed, the documentation can be rendered with the following command. The resulting files will be written to the `site/` directory.

```bash
uv run -m mkdocs build --site-dir site
```

Please note that the documentation is expected to be served from a webserver and may not render correctly when viewed via the `file://` protocol.
```
### Analyses
- [x] Determine default scenarios
	- [x] Just use the decorrelated ones
- [ ] Generate final metadata
	- [ ] Rename to descriptives?
- [x] Create final collections
	- [x] Just decorrelated within (A) different countries
	- [x] and (B) all open licensed?
- [ ] Add renv


- Website
	- Inspiration: https://www.dataprovenance.org/
	- Vitepress?
	- Landing page + explorer?
## TODOs

- [x] Double check / fix classification task detection e.g. ricci (?)
- [x] Code new / prev. missing datasets
- [ ] Write annotations into Python code?
- [x] Use dataset names as IDs
- [x] Add support for (stratified) fixed train test splits
	- [x] Support custom implementation in datasets?
	- [x] Also support this for AIF360 datasets with train test handled by us
- [x] Add seeds

## Comments

#### Alessenadro re Annotations

Motivate quantitative as features that describe underrepresentation, label bias, and proxies citing papers on data bias: - Sorelle A. Friedler, Carlos Scheidegger, and Suresh Venkatasubramanian. 2021. The (Im)possibility of fairness: different value systems require different mechanisms for fair decision making. Commun. ACM 64, 4 (2021), 136–143. https://doi.org/10.1145/3433949 - Ninareh Mehrabi, Fred Morstatter, Nripsuta Saxena, Kristina Lerman, and Aram Galstyan. 2022. A Survey on Bias and Fairness in Machine Learning. ACM Comput. Surv. 54, 6 (2022), 115:1–115:35. https://doi.org/10.1145/3457607 - Eirini Ntoutsi, Pavlos Fafalios, Ujwal Gadiraju, Vasileios Iosifidis, Wolfgang Nejdl, Maria-Esther Vidal, Salvatore Ruggieri, Franco Turini, Symeon Papadopoulos, Emmanouil Krasanakis, Ioannis Kompatsiaris, Katharina Kinder-Kurlanda, Claudia Wagner, Fariba Karimi, Miriam Fernández, Harith Alani, Bettina Berendt, Tina Kruegel, Christian Heinze, Klaus Broelemann, Gjergji Kasneci, Thanassis Tiropanis, and Steffen Staab. 2020. Bias in data- driven artificial intelligence systems - An introductory survey. WIREs Data Mining Knowl. Discov. 10, 3 (2020). https://doi.org/10.1002/WIDM.1356

Motivate qualitative by citing prior work: - Alessandro Fabris, Stefano Messina, Gianmaria Silvello, and Gian Antonio Susto. 2022. Algorithmic fairness datasets: the story so far. Data Min. Knowl. Discov. 36, 6 (2022), 2074–2152. https://doi.org/10.1007/S10618-022-00854-Z - Le Quy, Tai, et al. "A survey on datasets for fairness‐aware machine learning." Wiley Interdisciplinary Reviews: Data Mining and Knowledge Discovery 12.3 (2022): e1452.

## followup
- AI based annotation
- docling
- tools / inspirations
	- elicit
	- consensus
	- connected papers
	- citation gecko
	- scite
	- answerthis
	- atlas.ti
- 

## prev
- [x] Check out models used in AIF360
- [x] Add multiverse set-up
- [x] Add support for ML tasks
- [x] Create actual case study




- [x] Make export robust enough to run through
- [ ] Finalize pre-processing function
	- [ ] Imputation??
	- [x] Deal with new information -> favorable label = 1
	- [ ] Only apply pre-processing if necessary (by default)
- [x] Add COMPAS preprocessing
- [x] Go with Cosima over annotation problems
- [x] Compute delta to baseline and start looking at that!
- [x] Run case study
- [x] Debug issues in case study
- [x] Support feature selection
- [ ] Support multiple protected classes
	- [ ] Each as a different scenario
	- [ ] Including intersection
	- [ ] => How to do this well in code???
- [ ] Updated metadata calculation
	- [ ] Calculate metadata on processed data?
- [ ] Double check with cosima on "-" and protected cols i.e. does "-" mean that we also use prot. attr. as a feature?

**New TODO**
- [ ] Compute Cosima's metrics after preprocessing
- [ ] Add support for iterating over multiple protected attributes & combinations -> protected configuration? (Default to intersectional??)
	- [ ] This info should be added as new dimensions?? (multiversum: Add additional ad-hoc dimensions / prespecify via empty value?)
- [ ] Fit one model per method, predicting how well this method will perform on a given datasset
- [ ] Add feature importance values
	- [ ] Maybe average these out across models?

## Next Steps
- [ ] Calculate final metrics
- [ ] Add extra processing techniques
- [ ] Add support for less-processed datasets


## ToDo
- [ ] TODO: Add filtering for Adult
- [ ] Ensure train test splits always work the same
	- [ ] Add into package?

