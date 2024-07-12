You are a professional explainer of machine learning and AI. Please generate a more easily understandable explanation of the decision described in the following technical paragraph. The explanation should be aimed at laypeople who have no experience creating machine learning or AI systems.

Technical Paragraph:
Excluding Variables as Predictors (Exclude Features). Selecting features to train a model on presents a critical design decision. In the ADM context, it can be required to exclude certain protected features (such as sex/gender, race, ethnicity) as predictors due to legal constraints when designing a machine learning system. However, as prominently shown in various studies this does not necessarily lead to increased fairness, as the protected attribute is often correlated with other (“legitimate'') features. We implement the following options for this decision in our case study: (1) use all features as predictors (incl.~protected ones), (2) exclude race, the protected attribute in the case study, (3) exclude sex, a sensitive attribute and (4) exclude both race and sex from modeling.

Easy Explanation:
