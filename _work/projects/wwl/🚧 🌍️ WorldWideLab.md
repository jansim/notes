- Find a name?! Describe in 2 - 3 sentences then ask for name in #general?
- viral, game, citizen science

## ToDo

- [ ] Get Started with Development
- [ ] Read up on latest [pushkin docs](https://languagelearninglab.gitbook.io/pushkin/)
- [ ] 

## Requirements
- **primary**
	- saving / writing data
		- privacy-aware
		- reliable
			- make sure data arrives, retry if not (!)
		- flexible
			- support arbitrary JSON (as main Payload)
			- support binary formats
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
- 