
## Qs Malte
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
	- 
- [ ] Maybe: occupationCoding vs the package, which does what are the interoperable?
	- [ ] Function to generate training data / probabilities, copy over from occupationCoding
- [x] DTM only used for word names?!
- [x] Merge w/ default app settings

## ToDo
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
	- [ ] Revamp DB / data saving code?
		- [x] Automatically save page data
		- [ ] Add test case for saved data
		- [x] Rename
		- [ ] Make more flexible
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

