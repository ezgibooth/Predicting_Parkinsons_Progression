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
## UPDRS classification
The below UPDRS classification was used for analysis:

<p align="center">
<img src="https://github.com/ezgibooth/Predicting_Parkinsons_Progression/assets/118090932/b4d23890-1f4d-436b-b559-c59c1f979b55" width="600" height="400">
</p>

## Analysis Results

* UPDRS Score distribution of patients on medication vs. not on medication show that UPDRS scores are higher for patients not on medication:
<p align="center">
<img src="https://github.com/ezgibooth/Predicting_Parkinsons_Progression/assets/118090932/366fe008-65c4-4c99-a632-84bfedbe8fbc" width="800" height="600">
</p>

* Below shows the median UPDRS scores over time. The analysis indicates UPDRS 4 score only increases after mnonth 4 and is not a good indicator for early disease progression analysis
<p align="center">
<img src="https://github.com/ezgibooth/Predicting_Parkinsons_Progression/assets/118090932/ed39c45f-fa7f-41be-a878-fb9b28399269" width="600" height="400">
</p>

* Based on k-means analysis, proteins were clustered into four distinct groups:
<p align="center">
<img src="https://github.com/ezgibooth/Predicting_Parkinsons_Progression/assets/118090932/5d27ae68-f30c-494d-ae81-eff1d10b4b6c" width="700" height="400">
</p>

* We decided to focus on clusters 0, 2, 3 to get a better understanding of the protein levels over time, as shown below. While proteins in cluster 0 did not change much over time, protein levels in clusters 2 and 3 showed a greater variance over time, indicating they might be better candidates for using as biomarkers:
<p align="center">
<img src="https://github.com/ezgibooth/Predicting_Parkinsons_Progression/assets/118090932/0239d42f-500d-43dd-b73f-e5aaa57ee614" width="700" height="400">
</p>

* The below table the biological relevance of proteins found in each cluster. Since PD is a neurological disease, it is exciting to find proteins that are involved in brain and neuron related functions. Additionally, the two proteins, Prostaglandin and Serotransferin levels are significantly different in patients with low PD scores compared to those with high PD socres:
<p align="center">
<img src="https://github.com/ezgibooth/Predicting_Parkinsons_Progression/assets/118090932/abf18924-d603-47e7-8c20-a48bc579834d" width="700" height="400">
</p>

* Using the protein levels from the two above mentioned proteins we were able to create a neural network model that was able to predict PD progression with 0.77 accuracy.
<p align="center">
<img src="https://github.com/ezgibooth/Predicting_Parkinsons_Progression/assets/118090932/8bba257a-ede1-4c45-aaf9-bca191240352" width="700" height="350">
</p>
