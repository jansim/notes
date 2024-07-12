## IAB Workshop

- Extended Abstract (max 500W)
- IAB.PHD-WORKSHOP@iab.de
- Format: lastname_firstname_paper.pdf
- Up to Five Keywords at the beginning

## v4 Jan (extended)
There are a multitude of different ways to earn a living hence people’s occupations are almost as diverse as people themselves. Therefore, one of the classic issues one encounters when working with occupational data is the vast heterogeneity of people’s occupations. To address this problem, a variety of different classifications have been developed, such as the International Standard Classification of Occupations (ISCO) or the German Klassifikation der Berufe (KldB). These narrow down the number of occupation categories into much more manageable hundreds or low thousands.

The coding of occupations into these standardized categories is a time-intensive process plagued by reliability issues, however. To date the standard approach to code occupations is by collecting free text responses and having someone manually sit down with a guide, possibly assisted by computer software, to assign each category by hand post-hoc. Since coding typically occurs after data collection and with limited information, the assignment of categories can be quite ambiguous and unreliable. It is therefore common to have codings done at least twice to increase reliability further increasing costs.

Here we present a new instrument which implements a faster and more convenient, interactive occupation coding workflow where interviewees are included in the coding process. This instrument uses the best performing algorithm from a comparison of supervised and unsupervised machine learning models to generate a list of suggested occupation categories to be selected by the interviewee. Issues of ambiguity within occupational categories are handled by asking clarifying follow-up questions to the interviewee. The instrument is implemented as part of a flexible and holistic toolbox, covering the whole process from data collection and questionnaire design to the final coding of occupation into KldB and ISCO. Standard workflows are provided for common interview scenarios, with the option to extend workflows for more complex and non-standard use-cases. Anonymized training data from German surveys and pre-trained machine-learning models for Germany are provided as part of the toolbox.

The toolbox is implemented as an open-source package for the R programming language and will be made available at [https://github.com/occupationMeasurement/occupationMeasurement](https://github.com/occupationMeasurement/occupationMeasurement) including extensive documentation.

## v3 Jan
The coding of occupations into standardised categories such as the International Standard Classification of Occupations (ISCO) or German Klassifikation der Berufe (KldB) is a time-intensive process plagued by reliability issues. To date the standard approach to code occupations is by collecting free text responses and having someone manually sit down with a guide, possibly assisted by computer software, to assign each category by hand post-hoc.
Here we present a new instrument which implements a faster and more convenient, interactive occupation coding workflow where interviewees are part of the coding process. This workflow uses supervised machine learning and is implemented as part of a flexible toolbox for data collection, covering the whole process of occupation coding. The toolbox comes with pre-trained machine-learning models for the KldB and anonymized training data from German surveys.

## v2 Malte
### Intro
Jan Simson and Malte Schierholz from my lab have been developing an open-source R package to help with the interactive coding of people’s occupations and were thinking of submitting it to the Journal of Statistical Software. As the current instrument is limited to data collection in German-language surveys we wanted to check how well it fits the scope of JSS?

### Quick Abstract  
The coding of occupations into standardised categories such as the International Standard Classification of Occupations (ISCO) or German Klassifikation der Berufe (KldB) is a time-intensive process plagued by reliability issues. To date the standard approach to code occupations is by collecting free text responses and having someone manually sit down with a guide, possibly assisted by computer software, to assign each category by hand post-hoc. Here we present a new instrument which implements a faster and more convenient, interactive occupation coding workflow where interviewees are part of the coding process. The instrument uses supervised machine learning, and comes with anonymized training data from German surveys. We describe possible steps how the instrument can be implemented in a questionnaire and discuss the design decisions to be made.

## v1 Jan
### Intro
Some of the people in my lab have been developing an open-source R package to help with the interactive coding of people's occupations and were thinking of submitting it to the Journal of Statistical Software. As the project is of a more applied nature and focused on the German market we wanted to check how well it fits the scope of JSS or whether a different outlet might be more suitable?

### Quick Abstract
The coding of occupations into standardised categories such as the International Standard Classification of Occupations (ISCO) or German Klassifikation der Berufe (KldB) is a time-intesive process plagued by reliability issues. To date the standard approach to code occupations is by collecting free text responses and having someone manually sit down with a guide to assign each category by hand post-hoc. Here we present a new tool which implements the best performing machine-learning algorithm from a previous comparison by Schierzholz et. al. to create a faster and more convenient, interactive occupation coding workflow where interviewees are part of the coding process.