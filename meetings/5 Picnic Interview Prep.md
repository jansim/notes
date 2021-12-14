## What is Picnic About?
Fresh groceries delivery with 20 min delivery windows.

25€ min; free delivery

## Supply Chain
- Supplier
- Distribution Center
- Fulfilment Center
- Hub
- Customer

Truck delivery schedule gets optimized via e.g. genetic algorithm to reduce the amount of rerouting

## Data
Resides in Data Warehouse as opposed to a data lake (more structured that way). Single source of truth. Warehouse has front-end (analysts) and back-end (only engineers / data scientists).

All analysts use SQL to get data, separate TEMP area in warehouse available (regularly purged!).

- Stack
	- Data Warehouse: Snowflake ❄️
	- ELT: Python 🐍
	- DataViz / Dashboarding: Tableau 📈
	- Orchestration: Argo
	- Event Processing: Snowplow
	- Deployment: Kubernetes
	- Docs / version control: Github
	- 
- ETL (Extract Transform Load):
	- smaller data
	- easier to implement
- ELT (Extract Load Transform):
	- Directly loaded into target system
	- bigger data
	- in cloud

## Process for new features
1. try out with small number of customers => get feedback
2. roll out to bigger subsample => get more feedback
3. full roll out

Example: Presto meal bags

## Internal App Design
- Runner App: Developed with continuous feedback from runners


## Onboarding
Moved to online compared to pretty cool in person

- Improve clarity / documentation
	- Has actually helped in general => taking an outsider's look can open your eyes to potential improvements!
- 6 key principles
	- share the vision: what's next / roadmap for 6 - 12 months?
	- provide the context
	- get personal: get to know people; coffee chats
	- encourage being social
	- streamline / document ways of working
	- overcommunicate => redundant communication