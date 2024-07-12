#fairness-multiverse 

## Repository Preparation
- [ ] Move over code changes
- [ ] Add support for custom seeds
- [ ] Create Dockerfile
- [ ] Move over reproducible manuscript and other R code
- [ ] Push changes to public github


### Package
- https://snakemake.github.io/
- https://github.com/amakelov/mandala


## FK2RG
- **Our goal w/ paper:** Often many ad-hoc decisions, make these more explicit and raise awareness. Use multiverse analysis to deal with these in a sturcuted way
- First: Big thank you, awesome feedback already!

- Is there anything major missing in the paper that you'd like to be there? (despite the discussion 😄)
- Other good examples of unfair ADM besides the dutch childcare benefits?
- Are you convinced by the decisions we included?
	- Are any missing?
- Would you expect any additional statistical tests?
- Pearson correlation for non-normal distributed data?
- Should we also report information re performance / overall classifications or sth? Maybe baseline frequency of 1 labels in the dataset?


- HPO: multi dimensional optimization
- Explain some terminology
	- Maybe focus on Psych??
- Some parts lengthy others very short
- More verbal description of results
- Show more that there needs to be a reflection of what you're actually after
	- Political embededness 

- use result to get back to stakeholders to talk with them about results
- raise awareness for future design
- look at decision with more focus

- List of choices
	- more structuring to the list
	- State as limitation
	- Be more clear about this

- clearer relationship to psych multiverse analysis
- senstivity analysis?


- A pot. entscheidungen aufzeigen
- B highlighten was wichtig is
	- hier müssen techn. & inhaltliche zsm kommen
	- 

## Notes
- 


- Sofia
	- #2 Examples of tailored advertiesments? https://signal.org/blog/the-instagram-ads-you-will-never-see/
	- Degrees of tailoring in ads?
	- #7 maybe split; #8 and #9 could be combined?
	- #10 Unwilling to make setting

- Jake
	- Archival paper at ESRA? 👀
	- Ensemble models


## EAAMO Paper

- Specification Curve?
- 


## Next Meeting
- [x] Ask Florian: ElasticNet w or w/o regularization?
	- [ ] Just used ElasticNetCv 🤔

- [ ] Run 2 fanovas for sett_fairness_grouping
- [ ] Fanova w/o fitting a tree?
- [x] Visualisierung in einem plot?
	- [x] Auch gesplittet nach grouping
- [x] sett_fairness_grouping klarer gegenüberstellen

### Pitch
Oft schon Entscheidungen vor Fairness überhaupt -> man denkt nicht dass es was ausmacht, tut es aber 
Übrigens -> Interkationen sind auch wichtig teilw bei manuellem tuning immer nur one at a time

- Examples: https://ipsoeu.github.io/ips-explorer/case/
	- i.e. 170 for "predict"


## reading list!!
	According to US law, if disparate impact is less than 0.8, there is discrimination on a protected attribute [24].
Nakao et al., “Towards Involving End-Users in Interactive Human-in-the-Loop AI Fairness.”

Nripsuta Ani Saxena, Karen Huang, Evan DeFilippis, Goran Radanovic, David C. Parkes, and Yang Liu. 2019. How Do
Fairness Definitions Fare? Examining Public Attitudes Towards Algorithmic Definitions of Fairness. In Proceedings of
the 2019 AAAI/ACM Conference on AI, Ethics, and Society (Honolulu, HI, USA) (AIES ’19). Association for Computing
Machinery, New York, NY, USA, 99–106. https://doi.org/10.1145/3306618.3314248

# outline 

- Intro
	- What is fairness?
		- Nakao et al., “Towards Involving End-Users in Interactive Human-in-the-Loop AI Fairness.”
	- What is multiverse analysis 

# Points

### Poster

### ToDos
- [ ] Medicare nachlesen
- [ ] 2 fold approach
	- [x] variieren preprocessing / model etc.
	- [ ] variieren metrik
		- [x] 1. welche metrik
		- [x] 2. welches grouping
			- [x] bei N > 2 grps max difference ✅
		- [x] 3. excluding any subgroups?
- [ ] Add https://github.com/Kanaries/pygwalker
- [ ] Parallelize? https://joblib.readthedocs.io/en/latest/parallel.html
- [ ] 

Functional ANOVA

