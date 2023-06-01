## Notes
- 

## Journal Article
Two journals I have in mind: [https://www.jstatsoft.org/index](https://www.jstatsoft.org/index) and [https://journal.r-project.org/](https://journal.r-project.org/) I wonder what are the requirements to get published there? Publish on CRAN? Other possible journals: [https://www.software.ac.uk/which-journals-should-i-publish-my-software](https://www.software.ac.uk/which-journals-should-i-publish-my-software)

- Journal of Statistical Software
	- https://www.jstatsoft.org/about/submissions
	- https://www.jstatsoft.org/authors
	- Requirements
		- Specific PDF style
		- Open Source Code (?), Replication Script for all results mentioned
		- Clear License and GPL or GPL-compatible
	- If possible should be on CRAN
	- Paper as vignette is encouraged, R class system should be used
- Journal of Open Source Software
	- https://joss.readthedocs.io/en/latest/submitting.html
	- https://joss.readthedocs.io/en/latest/review_criteria.html
	- [OSI compatible License](https://opensource.org/licenses)
	- software must have **obvious** research application
	- paper must **not** focus on new results accomplished with said software
	- Paper.md must be in git
	- Git repo must be publicly browsable and ppl need to be able to submit issues
	- Substantial scholarly effort
	- Feature complete, according to standards of packaging
	- Co-publications of a more applied paper should be indicated
		- Automated Test Suite
	- Paper requirements themselves pretty straightforward
		- Short (max 1k words)
		- Mainly giving context, describing the need for the package
		- API itself should be documented within the package, not the paper
- Also: CRAN?
	- `R CMD CHECK` has to pass (easier via devtools::check)
	- Source code for everything has to be provided (i.e. also PDFs etc.), dependencies also have to be availabe
	- 5MB max size (!) (option to split into separate packages)
	- Don't write to filesystem w/o permission (tough one for cache? maybe write to R user dir??)
	- Must have one of these license: https://svn.r-project.org/R/trunk/share/licenses/license.db
	- Alternative to CRAN: https://r-universe.dev/search/

# Contents

## Title
Developing a Holistic Toolbox for Interactive Occupation Coding
occupationMeasurement: A Holistic Toolbox for Interactive Occupation Coding

## Outline (needs to be different for JOSS)

Introduction

- Problem: Occupation Coding is a mess
	- even classifications messy -> AuxCo
- Assistive Tools
	- SoCCer, other stuff
- Still: Lack of Open Source solutions, nothing yet for Germany
- Our solution
	- Based on ML comparison by Malte
	- Interactive Tool
		- Focus: Ease of use
		- R package
		- Shiny Interview Questionnaires
		- JSON API
		- Shiny & JSON will be available as Docker containers; no coding knowledge necessary

Methodology

- Developed using R, shiny, 
- Evaluation ongoing

Discussion

- Will be made public on github
- Updates to work with more versions of current systems
- Translation to other coding systems / languages

## References

