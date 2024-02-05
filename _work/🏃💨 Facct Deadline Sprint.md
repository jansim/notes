

## ✨ fairness-datasets
- [x] ✍️ do a second pass of text
- [x] add analysis on usage of sensitive attributes
	- [x] join alessandro's availability data to current data on usage
	- [ ] check all conflicts
		- [ ] some will have to stay e.g German Credit issues
- [x] update sankey diagram to use new data
- [x] finish first pass of annotations
	- [x] review annotations with issues by Aida & Felix
- [x] fix missing annotations
	- [x] Fix 2 annotations that require my Input
	- [x] add missing annotation quality for Bank
		- [x] fix Bank detailed analysis
	- [x] add missing COMPAS prot. attr. info
- [x] add in actual numbers instead of placeholders
- [ ] re-work existing sections
- [x] add abstract
- [x] add first draft of discussion
- [ ] if time permits: add new analysis 
- [ ] add appendix
- [ ] update fig-bar-sensitive-attrs to use new sensitive attribute categories
	- [ ] double check usage of gender??

- [ ] re-view annotations & their quality
- [ ] fix layouting

- [x] Speak w/ Felix
	- [x] Ask felix re Dataset names
	- [x] Ask re INPUT NEEDED papers

## 🌌 fairness-multiverse

- [x] ✍️ revisit / plan new structure 
- [x] ✍️finish first pass of rewriting
- [ ] do a second pass of text
- [ ] Update discussion
- [ ] Update abstract
- [x] add in actual numbers instead of placeholders
- [x] run missing correlations
- [x] finalize plots
- [x] fix layouting


#### Story
- 2 kinds of multiverse analysis
	- TODO: find catchy names 🤔
	- **1.** Design Multiverse Analysis: focus on pre-processing
		- understand variation
		- highlight that these choices matter
			- in good AND bad ways
		- for safe choices: discover which ones to focus on
		- long term: better understand for whole field
		- assess robustness of results (e.g. post-hoc)
	- **2.** Robustness / Evaluation Multiverse Analysis: focus on evaluation
		- prevent fairness-hacking
		- robustness of results


## Feedback Florian

- [ ] Add LMU affiliation

- [x] ⁠when designed wrongly -> suboptimally
- [x] technology (Kapitel) -> Software ( tech ließt sich komisc
- [x] The hacking of … > … or fairness washing (Aviodji)

- [x] Bei HPO würd ich vllt “efficient” erwähnen also quasi maximize or minimize metrics by visiting as few universes as possible.
- [x] Gradient boosted machine gibts glaub ich nicht
- [x] Gradient boosted machines oder gradient boosted decision trees
- [x] Bei stratification muss klar sein: Dass das nicht das Modell verändert sondern nur das Evaluationsprotokokl - D.h. Stratification might uncover biases by enforcing that small groups are always represented in the evaluation data
- [x] Was mir generell auffällt: das paper hat keine einzige Formel
      Nicht sicher ob das gut oder schlecht ist
- [x] Die scaling section ist nicht gut motivierter
      Wir wollen sowas sagen wie: wenn die Anzahl design decisions steigt oder compute Ressourcen knapp sind dann können wir vielleicht nicht das komplette Grid evaluieren
- [x] Besser von anderen, ähnlichen papern abgrenzen
	- [x] Fairness Washing
	- [x] Fairness Hacking
	- [x] -> Parallel Work? Nicht vorgänger; wollen wir immer so nah dran gehen? 🤔
	- [ ] Was macht unsere work so unique, warum gut?
		- [ ] -> Interaktionen finden?
		- [ ] -> Solution?
	- [ ] -> Fairness Comparison paper?
- [ ] Misusing models out of context sollten wir mehr bewerben?

- [ ] Impact etc. statement für Multiverse?