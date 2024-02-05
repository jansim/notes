---
creation date: 2023-07-05 10:11
event: "OSC Sensitivity Analysis Workshop"
speaker: "Angelika Stefan"
---

## Notes 
- methodological flexibility; researcher degrees of freedom
- Sensitivity Analysis: What **statistical outputs** are sensitive to which **inputs**?
![[Screenshot 2023-07-05 at 10.22.19.png]]

- No matter what you do, your outputs will always change
	- Are the changes *relevant* / do they meaningfully change?
- Multiverse Analysis
	- Extreme Version of Sensitivity Analysis
	- Try to map out *all* the decisions that there are, whereas sensitivity analyses are typically smaller

Possible visualization (s):
![[Screenshot 2023-07-05 at 10.49.07.png]]

![[Screenshot 2023-07-05 at 10.59.23.png]]

The decisions / settings you look at are still arbitrary.

Terminology
- robustness checks
- robustness analysis

### Challenges
- What to do with the results?
- Computational cost
	- depending on runtime
- Can basically be a fancy version of p-hacking -> always report complete results

- search more for multiverse analysis for nice viz

- in sociology:
	- robustness
		- what you can modify
	- sensitivity
		- how big would it (heterogeneity) have to be?

## Questions
- Specification Curve Analysis
- How does sensitivity analysis fare with more options?
- Are there guidelines on which settings to include? Or how to construct a list?
	- discrete vs continuous
		- if continuous: equal distances or log steps; going through there as efficiently as possible
- are there ways to automate these analyses?
- Is there a specific origin of sensitivity analysis?


- multiverse package
	- build on a pipeline step like {targets} or python equivalent
- 