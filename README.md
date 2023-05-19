# Project 4: Predicting Parkinsons Progression

## Background
Parkinson's disease (PD) is a debilitating neurological condition that impairs movement, cognition, sleep, and various normal bodily functions. Unfortunately, there is currently no cure available, and the disease progressively worsens over time. It is projected that by 2037, approximately 1.6 million individuals in the United States will be affected by Parkinson's disease, resulting in an economic burden approaching $80 billion. Scientific research suggests that abnormalities in certain proteins or peptides play a significant role in the onset and progression of this disease. By gaining a better understanding of these mechanisms, aided by the field of data science, crucial insights could be obtained to facilitate the development of new pharmacological treatments that could either slow down the advancement of Parkinson's disease or even provide a cure.
Present efforts have led to the compilation of extensive clinical and neurobiological data from more than 10,000 subjects, with the aim of sharing this comprehensive information with the wider research community. While numerous important discoveries have been made using this data, the identification of clear biomarkers or effective treatments for Parkinson's disease is still lacking.
The Accelerating Medicines Partnership® Parkinson's Disease (AMP®PD), the organizer of the competition, is a collaborative initiative involving government entities, industry representatives, and nonprofit organizations. Managed through the Foundation of the National Institutes of Health (FNIH), this partnership has established the AMP PD Knowledge Platform. This platform incorporates in-depth molecular characterization and longitudinal clinical profiling of individuals with Parkinson's disease, with the primary objective of identifying and validating diagnostic, prognostic, and disease progression biomarkers for this condition.
## Motivation
The goal of this project is to predict MDS-UPDRS scores, which measure progression in patients with Parkinson's disease. The Movement Disorder Society-Sponsored Revision of the Unified Parkinson's Disease Rating Scale (MDS-UPDRS) is a comprehensive assessment of both motor and non-motor symptoms associated with Parkinson's. We hope to develop a model trained on data of protein and peptide levels over time in subjects with Parkinson’s disease versus normal age-matched control subjects. This model can help shed light into which molecules change as Parkinson’s disease progresses.
## Tools/Modules
D3.js
Plotly
MatPlotLib
Sklearn
Tensorflow
numpy
Pandas
Peptides.py
PyBiomed
PyProtein
Flask
SQL Alchemy
