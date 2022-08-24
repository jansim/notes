
## Meeting
- [x] Ask re taking time off in Septembe
	- [ ] Plan exact time
- [x] progress update
- [ ] Check in with Malte on big picture plan / setting specific goals
	- [ ] -> Writing a paper
	- [ ] -> Presenting at a conference
- [ ] Writing things up
	- [ ] Describe the main ideas of what's in the software and how ppl can use this
- [ ] Conference presentation
	- [ ] ESRA?
- [ ] Set time aside to discuss auxco format

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

## Qs Malte
- [ ] Meet Malte next week to Discsuss Auxco data format
- [ ] Put package on github (privately)? (so we can keep the history from now on)
- [ ] Authorship of R package?
- [x] Do we really want to join in the alphabetical coding index?
	- [x] AW: Nein
- [x] Determine a (semi-) final package name?
- [x] Finalize: What do we want to return when no results?
- [x] Finalize: **Suggestions** or predictions?!
- [x] How best to do encryption
	1. Transparent Encryption: Only on Disk in DB
		- little effort
		- no protection if DB access exists
	2. Custom Value Encryption
		- currently implemented
		- harder to maintain
		- no protection if App access exists
	3. Split Private & Public keys
	- Muss es auf computer speichern können
		- CSV oder SQLite
	- Wollen es irgendwo anders speichern
- [x] Maybe: occupationCoding vs the package, which does what are the interoperable?
	- [x] Function to generate training data / probabilities, copy over from occupationCoding
- [x] DTM only used for word names?!
- [x] Merge w/ default app settings

## ToDo
- [x] Remove alphabetical coding index
- [x] New col format: `P_beruf_taetigkeit_text_Q_default_R_text`
- [ ] Determine journal (and figure out requirements)
- [x] Add data reshaping function
- [ ] Fix shiny test timing
- [ ] Suggestions
	- [ ] Split up suggestion generation from joining in auxco or kldb info
		- [ ] Also make both somehow passable / overwritable??
	- [x] Separate training data files / pre-trained models
	- [ ] add kldb3 support (just grouping stuff and joining in things!)
- [ ] Move "machen sie etwas anderes" text field to separate page
- [ ] Auto-Render buttons (use session history to hide prev., not sure what about next??)
- [ ] Add even more tests
- [ ] Use updated Auxco data format
	- [ ] And skip followup questions if possible
	- [ ] Re: API maybe provide followup answers as key value lists
- [ ] Final Polishing 💅
	- [ ] Document Datasets
		- [ ] TODO: Check on this with Malte? (At least for auxco we need to!)
	- [ ] Add pkgname.Rmd vignette (= Getting Started)
	- [ ] Update README
	- [ ] Create a nice hex logo
- [ ] Translations / Other formats
- [x] Nicer data reshaping (what about extra columns? check whether db can handled that...)
- [ ] Better container documentation
- [x] Improve tests & test coverage
	- [x] Can we improve e2e shiny tests?
- [ ] Go through `R CMD CHECK` output
- [x] Add final loading function
	- [x] Add function to get final ISCO / KldB codes
- [x] Add data saving tests
- [x] Write SQL vignette
- [ ] Switch to S3??
- [x] document pages
- [x] Deal with warnings in test-data-transformation
- [x] Replace all follow_up with followup
- [x] Add package website
- [x] Add API
- [x] Rename predictions to suggestions
- [x] Read dissertation on actual algo used in the app
	- [x] read summary
	- [ ] read more detailed info
- [x] Rename sessionId to session_id
- [x] Add support for general purpose pages
	- [x] revamp / abstract page data handling
	- [x] pages
		- [x] radio buttons
		- [x] text input
		- [ ] ? checklist
- [x] Re-Add Missing 2nd freetext!!
- [x] Rewrite make_predictions, make it ready for export
	- [x] Support a list of predictors/algorithms, abstract that away
	- [ ] Add predictor/algorithm to suggestions i.e. why is this predicted?
	- [x] Turn into one function
	- [x] Also export 
	- [ ] Add dictionary based coding?
- [x] Automatically set status = new
	- [x] Use freetext for 
- [x] Add support for second free text page (when needed)
	- [x] Show if all suggestions are below threshold
- [ ] Add function for easy data_loading
	- [x] Revamp DB / data saving code?
		- [x] Automatically save page data
		- [x] Add test case for saved data
		- [x] Rename
		- [x] Make more flexible
	- [ ] Combine all response files
- [x] Focus on data coming into the package
	- [x] rename datasets / columns for consistency (and make them replacable!)
	- [x] load kldb from url
	- [x] Add ESCO for ISCO
- [x] Abstract away questionnaire building => support a demo questionnaire as well as a default one
- [x] make R package for easy installation
	- [x] Add abstracted function to call app while providing settings
	- [x] Can also explicitly handle data & preprossing via https://r-pkgs.org/data.html
- [x] Re-organize functions to separate out data processing
- [ ] Abstract away the most important steps
- [x] Variables in ENV
- [ ] Add API support via plumber
	- [ ] Session management via https://www.rplumber.io/reference/pr_cookie.html
- [x] Abstract away settings from the query?
	- [x] Turn them into a list or so, for consistency with API
- [ ] deployment via docker container
- [ ] psychTestR ??
- [ ] Submit on enter
- [x] Get rid of exprs / eval 
	- [x] replace via R6 classes? (might improve debugging)
- [ ] Add training data agnostic support
	- [ ] only via a search / text distance over the available options
		- [ ] support all 3 coding systems and disambiguate between output and matching
		- [ ] use the detailed descriptions / tasks in ESCO, possibly support 

### Ideas
- Packages as application
	- similar to JASP / Jamovi??
	- https://www.travishinkelman.com/deploy-shiny-electron/
		- https://github.com/wleepang/DesktopDeployR (most likely option)
		- https://chasemc.github.io/electricShine/
- Python or R??
- Encodings
	- ISCO - International Coding
	- Kldb - German coding
		- basis of current training data
	- AuxCo - made by malte, has mappigns to ISCO & Kldb, has follow up questions (currently used as outcome)
	- ESCO (european coding, more specific version adding extra numbers to ISCO)
		- translated into all sorts of languages
		- might want to switch to this, to allow international coding out-of-the-box
- https://towardsdatascience.com/string-matching-with-bert-tf-idf-and-more-274bb3a95136
- Privacy of free text training data?!




## Prev. Meetings
- cloud storage ordner
- Seit April ist Olga mit Dabei
- Demoversion
	- zum vorführen der aktuellen version
- Termine

- Aktuelle Software zu verbessern
- unter open source veröffentlichen
- Im Gespräch mit forsa Institut
	- 100k interviews
- Api version?
	- Fragen / Antworten
	- JSON
- Aktuell R / shiny

- Auf github
	- Verlgeich von different algorithmen was ist der beste?
	- Dann noch daten dazu, oh wir können auch vorhersagen
	- Das 2. wie sehen antwortoptionen aus?
		- Was sollen die leute auswählen können?
	- 3. Projekt auf gitlab: quasi UI / shiny app

