---
creation date: 2021-12-05 21:17
---
# 2021-12-06: Picnic 2nd Round Interview


## Notes going into

#### Scale-Up HR Challenges
- onboarding
- finding skilled labour
- quick change also within organization
	- can be challenging for employees => may increase turnover
	- change within team structure and management
- clash between start-up culture (rapid change, wider roles, jack-of-all-trades) and more established business culture (more specific / narrow roles, expertise and skills) => soliution: empathy
- covid makes (almost) all of these challenges harder

#### People
- Hanneke Swart: Director of People
- Willem-Joost Walch: Growth? in France?

## Notes during
- last time I had to convince someone
	- Prepared the facts
	- Tried to see their perspective
- 

## Summary / Action Points

## Questions
- What tasks would I typically be doing?
	- processes / systems development; mistake free way of working => formalizing
	- learning & development => pretty good learning programs => not aligned with review system
	- reviews =of people>  no centra lcalbiration; no consitency on review
	- research on what other companies are doing; what are we doing; how can we improve? ==> more thinking solution than data based one
- Learning / personal growth track?
- Career opportunities? (prob. nice in scale-up?)
	- classic trajectory: become more senior; 
- Flexible Home office / work office setup? Yes
- Read about the overall data tech stack on medium, anything that's different in the HR team?
- Tech Setup
	- Mac / Windows?

# More
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


# Notes from some Meeting @Picnic
# The Role

- Different than other analyst positions
- Deveopment of everyone in central team (eeryone not in operations)
  - ~600 ppl
- Tracking engagement, health
- Improve learning
- Centralized review system
- People partners do day-to-day support, salary etc.
- Pushing the improvement side of things
- Focusing on improvements
- 1st analysing the data, what do we need; how do we solve it; implement solution

## Systems

- a lot of google sheets
- migrating to workday
- Greenhouse
- office vibe





