Dear Sophia,

Thank you for the helpful reply and please excuse the delay due to some internal planning on which options of using the data would make the most sense.

Please find an abstract for our research project below, followed by the answers to your questions.

**Abstract**

> There are a multitude of different ways to earn a living which is why people’s occupations are almost as diverse as people themselves. Therefore, one of the classic issues one encounters when working with occupational data is the vast heterogeneity of occupations people have. To address this problem, a variety of different classifications have been developed, such as the International Standard Classification of Occupations (ISCO) or the German Klassifikation der Berufe (KldB), narrowing down the number of occupation categories into more manageable numbers.
>
> This leads to a different problem, however: The coding of occupations into standardized categories is a time-intensive process plagued by reliability issues. To date the standard approach to code occupations is by collecting free text responses and having specifically trained personnel sit down with the classification manual, possibly assisted by computer software, to assign each category by hand post-hoc. Since coding typically occurs after data collection and with limited information, the assignment of categories is often ambiguous and unreliable.
>
> Here we present a new instrument which implements a faster, more convenient and interactive occupation coding workflow where interviewees are included in the coding process. Using the best performing algorithm from a previous comparison of machine learning models, a list of suggested occupation categories is generated to be selected by the interviewee. Issues of ambiguity within occupational categories are addressed with clarifying follow-up questions. The instrument is implemented as part of a flexible toolbox, covering the whole process from data collection and questionnaire design to the final coding of occupations into KldB and ISCO. Anonymized training data from German surveys and pre-trained machine-learning models for Germany are provided as part of the toolbox.

There are mainly two use-cases where data from the EWCS could be useful:

1. We would be interested in checking how well our algorithm would perform for languages other than German. To do this, we would like to train our algorithm on e.g. English data from the EWCS and check its performance compared to an algorithm trained on German data from the EWCS.
2. If performance is adequate, we would also be interested in using the resulting machine learning model to generate occupation coding suggestions for use in an online survey setting, with which we could then collect further and new training data. With this additional training data we could then improve model performance and eventually build a new model to release.

Data would be stored on work laptops issued by the LMU University of Munich for analyses and possibly on a local network drive controlled by the Leibniz-Rechenzentrum (LRZ) of the Bavarian Academy of Sciences for sharing within the project group (the drive does need a login for usage). For more demanding analyses we might also load the data into instances onto a University affiliated computing cluster, most likely the LRZ research cluster. We will not share data with anyone outside of the group working on this project.

Regarding the retention period, we would aim to conclude analyses with the data within a period of 12 - 24 months after receiving it, after which we would delete the data from all said locations. If possible, we would like to retain the resulting machine learning model for a longer period of time. Since the model does contain information about the underlying data, we would not share any model trained directly on this data.

Due to the relatively small number of observations for each country we would be most interested in the combined list of EWCS surveys from 1991 - 2015 (and if already possible even 2021), similar to http://doi.org/10.5255/UKDA-SN-7363-8. In terms of items, we only need the full ISCO coded occupation categories, the free text responses to the occupation questions (Q5, Q6 in the 2015 survey) and the associated language / country if that is possible?

I was also wondering whether there is some documentation on how exactly the coding into the ISCO was done (e.g. was it one person sitting down with a manual or were some answers coded by multiple people)?

I hope this answers all your questions and want to thank you again for your help. We are looking forward to your response!

Best Regards,
Jan Simson