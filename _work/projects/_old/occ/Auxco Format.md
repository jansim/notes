- src data: separate XML files in a git repo?

# New Export Data Format (i.e. CSVs)

## Changes
- overall
	- [x] There should be no more changes to actual *data* in the occupationMeasurement package (right now there are!!)
		- [x] Add title_kldb_short to auxco categories
	- [x] rename id to auxco_id everywhere
	- [x] use standard csv format (i.e. comma instead of semicolon)
	- [x] consistent naming, `_` instead of  `.` and all in English
	- [ ] option: Translate everything?
	- [ ] option: Codebook, datapackage.json / csvw / Felix???
- **abgrenzungen_sortiert_nach_kldb.csv**
	- [x] rename: "auxco_distinctions"
	- [x] Why by kldb?
	- [x] Maybe clearer types? what is hoch mittel?? auf engl switchen
		- typ => similarity
		- refid => similar_auxco_id
		- refbezeichnung => similar_...
		- kldb_id_efault => default_kldb_id (ans ende)
- **folgefragen_jtl.csv**
	- [x] Delete this?
- **folgefragen.csv**
	- [x] auxco_followup_questions.csv
	- [x] every question has a *unique* `question_id`
		- if there are multiple followup questions, the answer option
	- [x] every answer has a *unique* `answer_id`
		- DISCUSS❗️every answer links to either another `question_id` or an `auxco_id` (maybe kldb/isco ids instead, as is currently the case)... or both??
	- [ ]  *❗️❗️ Handle codings which depend on both followup questions via this data format (!)*
	- [x] followUp => NAs to TRUE
- **hilfskategorien_kldb_mit_id.csv**
	- [x] rename: "auxco_mapping_from_kldb" or "mapping_from_kldb_to_axuco"
	- [x] create the same for ISCO
	- [x] add auxco & kldb bezeichnung columns
- **hilfskategorien_sortiert_nach_id.csv**
	- [x] rename: "auxco_categories"
	- [x] kldb_default / isco_default to default_kldb, default_isco
	- [x] remove kldb/isco_folgefrage columns (this info should be in the mappings)
	- [x] other column renaming
		- taetigkeit => task
		- taetigkeitsbeschreibung => task_description
		- bezeichnung => title

### Current Format
- **abgrenzungen_sortiert_nach_kldb.csv**
  - *kldb_id_default*	11101	11101
  - *id*	1010	1010
  - *bezeichnung*	Acker- und Erntehelfer/in	Acker- und Erntehelfer/in
  - *refid*	1011	1012
  - *refbezeichnung*	Helfer/in - Tierwirtschaft und im Ackerbau	Landwirt/in
  - *typ*	hoch	mittel
- **folgefragen_jtl.csv**
  - *job* title	Musiker/in	Musiker/in
  - *fragetext_1*	Ist eine der folgenden T√§tigkeiten Hauptbestandteil Ihres Berufes?	
  - *antwort.pos_1*		1
  - *antwort.text_1*		Interpretation, Aufnahme und Auff√ºhrung von Instrumentalmusik
  - *antwort.kldb_1*		94114
  - *Anforderungsniveau2*?		
  - *Anforderungsnivau3*		
  - *Anforderungsniveau4*		94114
- **folgefragen.csv**
  - *laufindexFolge*	1	2
  - *id*	1004	1004
  - *questionNumber*	1	1
  - *typ*	anforderungsniveau	
  fragetextAktuellerBeruf	Ist f√ºr Ihre T√§tigkeit in der Regel eine - abgeschlossene Berufsausbildung erforderlich?	
  fragetextVergangenerBeruf	War f√ºr diese T√§tigkeit in der Regel eine - abgeschlossene Berufsausbildung erforderlich?	
  - *antwort.pos*		1
  - *antwort.text*		Ja
  - *antwort.kldb*		51322
  - *antwort.isco*		4412
  - *followUp*		NA
- **hilfskategorien_kldb_mit_id.csv**
  - *id*	9999	9999
  - *kldb*	1402	1302
- **hilfskategorien_sortiert_nach_id.csv**
  - *id*	1000	1001
  - *bezeichnung*	Schalterangestellte/r - Flughafen	Steward/Stewardess (Flugzeug)
  - *kldb_default*	51422	51422
  - *kldb_folgefrage*		
  - *isco_default*	4221	5111
  - *isco_folgefrage*		taetigkeit	Beratung und Betreuung von Flugg√§sten am Flughafen	Betreuung von Passagieren w√§hrend des Fluges
  - *taetigkeitsbeschreibung*	z.B. Ausk√ºnfte erteilen; Flugtickets verkaufen; Check-In der Flugg√§ste	z.B. Flugg√§ste an Bord begr√º√üen; Verhalten in Notf√§llen erkl√§ren; Mahlzeiten und Getr√§nke w√§hrend des Fluges servieren
