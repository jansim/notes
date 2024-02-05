---
creation date: 2023-11-27 10:57
---

## Notes going into
- [ ] Possible new angles
	- [ ] [fairness hacking](https://arxiv.org/abs/2311.06826)
	- [ ] empirical data on how surprising results are?
- [ ] Finalize decisoin for AFT Workshop
	- [ ] 
- [ ] most dramatic presentation of issue?

## Notes during
- 

## Summary / Action Points
- Update the paper to include more prominent reasoning as to "why is this important?"
- Separate preprocessing and evaluation decisions
	1. Preprocessing decisions are fair game and essentially just HPO
	2. evaluation decisions are not ok and correspond to fairness-hacking
- We show two ways of multiverse analysis: one corresponding to (1) and one corresponding to (2)

# 2nd Meeting

### TODO
- [x] add new decisions
	- [x] sub-universe: drop-subgroups in eval (same subgroups as during train) [binary]
	- [x] sub-universe: use a "convenient" subset of the data
		- [x] based on locality -> PUMA? biggest / whitest / all / only certain e.g. urban areas
		- [x] exclude military?
		- [x] exclude non citizens?
- [x] update existing decisions
	- [x] fariness-grouping must only happen during eval -> 
- [x] compute different metrics besides equalized odds
	- [x] most similar metric?
- [ ] re-run analysis
- [ ] update analyses / plots
	- [ ] detailed decision plots for evaluation decisions
		- [ ] highlight a single model within there (maybe the one with the most difference in fairness??)
	- [ ] update existing analyses to still make sense
- [ ] update text
	- [ ] evaluation decisions
		- [ ] fairness-grouping

### Action Plan
- Add new decisions w/ focus on evaluation -> can all be done as sub-decisions
	- binary: drop subgroups in evaluation (vs. in training only)
	- compute different metrics? - maybe similar ones?
	- only evaluate on a "convenient" subset of the data e.g. based on locality
		- `PUMA`
			- biggest
			- whitest (?)
			- complete
			- only urban areas?
		- exclude military
		- citizenship
- look at evaluation decisions completely separately
	- fairness-grouping should only happen on the evaluation side (!)
- 2 parts
	- 1. implicit decisions (should be more explicit) + innocious decisions (surprising)
		> We show that seemingly innocuous decisions made during pre-processing often have surprisingly large effects. Turning such, often implicit decisions into explicit decisions can uncover discrepancies and pave a path towards fairer models.
	- 2. fairness-hacking / same model different fairness values
- evtl. deep-dive for a single model, showing how much you can tweak in there?
- have a plot demonstrating 
- developer perspective in relation to legal frameworks
	- you put yourself at risk of getting sued?
- disconnect development vs usage
	- do I evaluate for the right context?
- Das gleiche Modell in anderen Kontexten verwenden
	- Dann auch andere fairness-metriken relevant?