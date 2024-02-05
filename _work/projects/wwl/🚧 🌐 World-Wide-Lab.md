- Find a name?! Describe in 2 - 3 sentences then ask for name in #general?
- viral, game, citizen science
- extra resiliency features?
	- e.g. send data multiple times

- npm init @world-wide-lab
- New Use case: Active Learning?
	- https://docs.argilla.io/en/latest/reference/webapp/pages.html
		- JS / TS version incoming
- On attracting traction: https://plane.so/blog/how-we-got-to-20k-github-stars
- 

- [x] Should it be possible to have runs without a participant?

- Download link via github: `https://github.com/USER/PROJECT/releases/latest/download/package.zip`
- https://docs.github.com/en/repositories/releasing-projects-on-github/linking-to-releases

- interactive API docs?: https://github.com/scalar/scalar

## Questions Sam
- [x] do we need started for runs?

## ToDo
- Playwright for Admin UI / Electron tests??

wwl.ai (80$/yr)
wwl.academy ??
world-wide-lab.org (10$)
world-wide-lab.com (10$)

- experiment version

- [x] extraInfo
- [x] publicInfo
	- [x] GET participant/:something/publicInfo
- completedStudies
- Count
- [x] sequential Response Ids

- [ ] add table and column comments


Provide data in study/finish.??

- [x] Fix test cases timing out
- [ ] ? Read up on latest [pushkin docs](https://languagelearninglab.gitbook.io/pushkin/)
- [ ] ? Other interesting implementation https://github.com/lookit/lookit-api
- [x] Fix weird issues in admin UI?!
- [x] Settings / Configuration => Unified parsing of ENV variabels
- [ ]  Features
	- [x] Proper logging with streams and to files
		- [x] winston
	- [ ] Code styling & Linting
		- [ ] prettier
	- [x] Example Data
	- [x] Building
	- [x] Authentication
		-  Should be optional / configurable => i.e. not present in Electron
		-  Different levels: 1) just one default hard-coded user 2) fine-grained access controls
	- [x] PostGres support
	- [x] Counts
		- [x] /study/countRuns?finished=true
		- [x] /study/:study/countRuns?finished=true
	- [x] Data export
		- [x] /study/data
		- [x] Authentication for API.. move into admin router??
			- [x] Use ApiKey via authorization: bearer header
		- [x] Re-Shaped data exports
			- [ ] Make efficient via https://www.npmjs.com/package/pg-copy-streams
	- [ ] Plugins
	- [ ] Proper Testing
		- [x] for validation of responses & nice error handling
			- [x] Proper responses for PUT
		- [x] for Admin UI
		- [x] for postgres
	- [ ] Hosting support
		- [ ] Upload of files / binary things as data into database
		- [ ] `StudyFiles`, return via express (potentially add caching?) `res.type` in electron for mimetypes
	- [x] Electron -> use separate directory
	- [ ] Protect / disable certain endpoints via settings
	- [ ] OSF as data storage
	- [x] @world-wide-lab/jsPsych integration
	- [ ] @world-wide-lab/labjs integration
	- [ ] Meta-Data package @world-wide-lab/meta
		- [ ] detect automated translations
		- [ ] UA
		- [ ] IP based stuff??
	- [x] Dashboard
		- [x] Runs over time
		- [ ] Total number of runs, finished runs & participants
		- [x] Number of Studies
	- [ ] Warnings
		- [ ] For unsecured admin UI when not in electron
	- [ ] Onboarding
	- [x] API Package
		- [x] @world-wide-lab/api; fetch based api
		- [x] participant.get() 
		- [x] run = participant.startRun()
		- [x] run.sendResponse()
		- [x] run.finish()
- [ ] DB
	- [x] Info => Meta?
		- [ ] Validation that JS object!
	- [ ] Tags => via array
	- [x] Migrations!! (How to deal with different database engines)
- [ ] Tests
	- [x] PostGres tests
	- [x] Electron App tests
	- [x] Docker Container Tests
		- [x] => via docker-compose run tests
- [ ] Electron App
	- [x] fix file path with space
	- [ ] add tests
	- [ ] add QoL menuitems e.g. open data base location
		- [ ] https://stackoverflow.com/questions/43991267/electron-open-file-directory-in-specific-application
		- [ ] https://www.electronjs.org/docs/latest/api/menu
- [ ] Documentation: vuepress?
- [ ] Landing Page: whole site via vuepress?? incl. documentation
	- [ ] atroposjs for landing page effect?
- [ ] Docker Container
	- [ ] https://docs.github.com/en/actions/publishing-packages/publishing-docker-images#publishing-images-to-github-packages
- [ ] Deployment
	- [ ] of docker compose
	- [ ] terraform??
- [ ] Am Ende noch kompletten Datensatz anschauen??
- [ ] Make database url configurable in electron
	- [ ] Be able to use one database for multiple computers
- [ ] Long term
	- [ ] Multi-User-Studies / Participant Management
	- [ ] Push Notifications
	- [ ] Multiple users & permissions in admin UI
	- [ ] Assign different versions of a study (based on sth in the backend?)
	- [ ] Stimulus management
	- [ ] support binary formats / upload of data
		- [ ] support digital trace data / highly flexible formats?
		- [ ] support mouse tracking data (large JSON blobs)
	- [ ] Extensible: Custom API endpoints via directories??
	- [ ] Enrich data based on IP adresses
		- [ ] ipapi.is (provides data for downloading, license would need checking)
		- [ ] https://ipapi.is/geolocation.html
		- [ ] https://ipapi.is/asn.html
		- [ ] https://ipapi.is/about.html
		- [ ] https://www.npmjs.com/package/geoip-lite
		- [ ] https://dev.maxmind.com/geoip/geolite2-free-geolocation-data

- [ ] Plugin: Access Control
- [ ] Plugin: Different Versions of Studies
	- [ ] For different participants
	- [ ] Visibility of studies??


Plugin Use Case
- Stimulus management
- Hooks for api paths
- Plugins via WASM??
- Stimulus Sets?
- Link Responses to Stimuli?? Maybe column hidden in UI??

- OSF Backend?
- Unterschiedliche File-Provider?


- Alternativen
	- cognition run
	- JATOS
	- Data Donation:
		- [Port](https://github.com/eyra/port) built by https://eyra.co/ (Company doing RSE)
		- DataDonationModule https://github.com/uzh/ddm by Uni Zürich


## Requirements
- **primary**
	- saving / writing data
		- privacy-aware
		- reliable
			- make sure data arrives, retry if not (!)
		- flexible
			- support arbitrary JSON (as main Payload)
			- support binary formats / upload of data
			- support digital trace data / data donation => processing in front-end via Pyodide??
		- outputs
			- to Database
			- to File (maybe just SQLite)
			- to OSF
	- reading data
		- in a clean format
		- in a privacy-aware manner
	- scalability
		- freely scalable
	- ease-of-use
		- easy to implement
		- easy to understand -> simplicity
		- easy to set up
	- open-source / self-hostable
	- support for common psych libraries
		- jsPsych / lab.js
		- maybe others?
		- make the API simple enough to work w/ anything
- GDPR compliance
- **secondary**
	- embeddable experiments into a website
	- hosting experiments (optional)
	- localization

## Tutorial
1. setting up site / platform
2. adding an experiment

## UI ???

## Possible Implementation / Stack
- "Cloud-native"
- Serverless
	- AWS Lambda for API
	- [DynamoDB](https://aws.amazon.com/dynamodb/) or [Aurora Serverless](https://aws.amazon.com/rds/aurora/serverless/) for DB
		- Check pricing
		- Check for open source alternatives
		- Maybe also MamoeryDB??
	- PostgreSQL DB maybe also SQLite
	- Language
		- JS / TS
			- Prisma for DB
			- Sequelize
			- Plugins like Obsidian? https://github.com/obsidianmd/obsidian-sample-plugin
				- https://css-tricks.com/designing-a-javascript-plugin-system/
			- + Same as front-end language, electron support, familiar, good for JSON
			- - Not that great SQL support
		- Python
			- SQLAlchemy
			- https://github.com/tiangolo/sqlmodel (simpler sql interface designed to work w/ fastApi)
			- https://github.com/jordaneremieff/mangum (fastApi) or https://github.com/zappa/Zappa (flask) 
	- Local serverless setup
		- https://github.com/localstack/localstack
		- https://github.com/openfaas/faas
		- Knative
- Full Stack??
	- https://github.com/t3-oss/create-t3-app

## Inspiration
- pushkin
- themusiclab.org
- Similar
	- [https://open-lab.online/](https://open-lab.online/)
	- Pavlovia
	- Gorrilas (??, ask Felix)
	-  [https://www.jatos.org/](https://www.jatos.org/)
	-  [https://expfactory.github.io/builder/experiments](https://expfactory.github.io/builder/experiments)
- 