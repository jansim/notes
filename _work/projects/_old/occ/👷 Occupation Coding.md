#occ 

- save time on the introduction
	- people know about occupation coding already
- present main results from the tool in more detail
- Talk duration
	- 12-15 minute talk
	- 5-3 minute discussion / questions

- What kind of results?
> Also, after reading what our friend Bernhard wrote about identification of leadership positions when using our tool (that the tool might be not performing the best when it aims to identify abteilungleiter and jobs like that), I looked at the survey data.  
> What we have there is the following:  
if we have 3 first digits correct, and the 4th digit is wrong (tool doesn’t match with manual coding), the digit 9 (management) and digit 1 (i don’t remember)  are the most frequent reasons for mismatch.  
If we assume the manual coding is correct, then occupations with the fourth digit 9 (as given by manual coding) are most likely to be not identified by the tool at all (25% of cases). For other fourth digits auxco isn’t providing suggestions in 10-15% of cases.  
But if the first four digits are correct (aka manual matches the tool), with the fourth digit being 9, then the fifth digit will also be correct in 38 out of 50 cases we have in the sample. So Malte you were right, that the fifth digit is not that much of a problem for the tool and respondents, but the fourth digit might be.

## Future Ideas

- Occupation Coding Group 14.07.23
	- FastTest for embedding with NN behind the scenes for classifications
	- Include Bigrams for better perf
- 

## ESRA Presentation
- Meeting on Monday to go over slides in detail
- Drop the difficulties of occupation coding or just skip in talk
- Merge 3 & 4??
	- Occupation coding is hard / issues
- 10 slides maximum
- Crowd: More occupation coding, less ML
- Skip #8 (the algorithm)
- Could skip #9 (our method) -- if too many slides
- Make demonstration a priority
- Merge following sldies into #15 (what's in the toolbox)
	- make it a fast one
	- mention that it's on CRAN?
- Use Schierholz 2021 numbers in earlier performacne slide (red ones)


## Next Meeting

- [ ] EWCS results
	- [ ] missing data
	- [ ] pretty comparable performance (though still weird!)
	- [ ] ➡️ Should we smoothen the process of re-training the tool?
	- [ ] Malte will take another look at HTML
- [x] Forsa Data
	- [ ] Send analysis HTML
- [ ] Submit to CRAN
	- [ ] Yes
- [x] Paper: What about English?
- [ ] Paper: Design a Figure?
	- [ ] Yes
- [x] Put EWCS project into shared folder


Turtle Data
	occupationMeasurement/background/Schierhalt et al 2016/

- Ans1: First answer
- Ans2: Second answer
- Ans4: Third answer on alternative
- KldBinfratest: Coding 1
- kldbstringcoding: Coding 2

- Handle uncodable cases like Rentner as special case (via prediction)

## TODO


- [x] Updated Response
- [x] IAB Workshop
	- [x] Need to accept
- [ ] ESRA Abstracts
-  Informational
	- [ ] New standardized isco format is in
		- [ ] Only needing to update API (WIP)
	- [ ] Currently busy fixing test cases

- [x] Standardized answer levels in API?

- [x] Mikrozensus Meeting
	- [ ] Model Re-Training
	- [ ] Evaluating model performance?
- [ ] Ask Malte re documentation on (re-)training the ML model
	- [ ] Evaluating?
- [ ] Respond to EWCS surcey
- [ ] Ask Julia Lane re non-German occupational data?
- [x] What kind of ESRA Abstract? What kind of paper?! (300W)
	- [x] Similar for IAB Workshop?!
- [x] Authorship
- [x] Api Design
	- [x] Wie standardized answer levels kommunizieren?
	- [ ] Named lists sind nicht wirklich supported
- [ ] Wie sollen wir Daten abspeichern?
	- [ ] append_tables für occupations_suggested?
	- [x] append_tables für toggleSubmitted?
	- [ ] Immer ein CSV per respondent (i.e. mehrere) oder nur einer overall?

## ToDo

- [x] Write EWCS response draft
- [x] Add Studentische Hilfskraft as Option
	- [x] Add kldb_title_short to hiwi
- [x] **Save session information in on SessionEnded**
- [x] Wait for Malte's input on standardized answer levels API
- [x] Send info on Logging for review
- [ ] Review API docs

- [ ] Add documentation on included data? training data?
	- [ ] Add function for preprocessing training data
- [ ] Add suggestion_type in /get_suggestions
	- [ ] Maybe update vignette to show different flow for kldb-only?
- [ ] Add support for different models e.g. BERT based?
- [x] Keine codes direkt mitgeben
- [x] Final_question schon bei /suggestions
- [x] Fix @seealso links
- [x] IAB Abstract
- [ ] Check weird case of Koch
	- [ ] Fast food via 2 ways
- [x] Tests for edge cases of: `Zeitarbeit`  oder `studentische Hilfskraft` , `FSJ` 
	- [x] Arbeiter?
- [x] ? New function: add_non_kldb_occupations in load_auxco
- [x] Documentation on Data Saved in the App
	- [x] What is saved? (rework, based on DB vignette)
		- [x] toggle_submitted as well
	- [x] Where is it saved?
- [x] User more specific / versioned namings for suggestion type
	- [x] kldb-2010
	- [x] auxco-1.2.x
- [x] In der Funktion `get_followup_questions`  kann ich mir bei API-Anwendungen Situationen vorstellen, wo man auch das `corresponding_answer_level`  in der answers-Tabelle nützlich finden kann. Da spricht doch nichts dagegen, diese Spalte auch noch mit auszugeben?
- [x] Support standardized / corresponding_answer_levels in get_final_codes??
	- [ ] Add them to API as well?
- [x] Session settings via app_settings??
- [x] Track long description expansion (within page itself) - [Msg](https://fk2rg.slack.com/archives/D032PBSG5FG/p1664631949609809)
- [ ] Save data upon session closure?
- [x] Update auxco to handle the new weird special cases
	- [x] Add a corresponding test case: get_final_codes("4038", followup_answers = list("Q4038_1" = 2, "Q4038_2" = 1))
- [x] "Build your own page" documentation - [Msg](https://fk2rg.slack.com/archives/D032PBSG5FG/p1664632658260519)
- [x] Add tests via gh action??
- [x] API Vignette? More Info regarding the flow of the package???
- [ ] ISCO as output type?
- [ ] Re-Train via EWCS
- [ ] Shiny Docker: Generate default questionnaire shiny endpoints in docker container???
- [ ] Add READMEs for docker images
- [ ] Malte: Documentation on re-training
	- [ ] Evaluation? Should we provide our own?
- [ ] Release
	- [ ] turn GH public
	- [ ] Add pkgdown website
	- [ ] Add docker containers
	
- [x] Build different questionnaires
	- [x] web-survey
	- [x] guided-interview
	- [x] app-demo
		- [x] remove demo_app()?
- [ ] Dokumentation
	- [x] Getting Started
		- [x] quasi more in-depth readme
	- [x] Building your own Questionnaire
	- [x] Deployment
		- [x] e.g. shiny server, docker, etc.
		- [x] Update docker API commands to use volumes
- [x] Support to overwrite datasets
	- [x] Add function to load auxco from csvs / zip
- [x] Enable passing of custom datasets everywhere (!)
	- [x] Function to load / mix custom with packaged datasets
- [x] Support to pass custom model via app_settings
- [ ] Ask Malte to write README re model building?
	- [ ] And review documentation on function to train models?
- [x] Fix rest of R CMD CHECK issues
	
- [ ] Research surveycodings.org
- [ ] Where to find pre-coded ESCO data??
- [ ] Update final_codes to support the new answer levels
	- [ ] What if answers are all isco_skill_level_3 but answer is isc_level_2
	- [ ] Maybe add commentary?

- [ ] Determine journal (and figure out requirements)

- [ ] Add support for english / localization in general
- [ ] Suggestions
	- [ ] Maybe move the join into another funciotn


- [x] Final Polishing 💅
	- [x] Document Datasets

- [x] Add function for easy data_loading
	- [x] Combine all response files
- [ ] Submit on enter

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

