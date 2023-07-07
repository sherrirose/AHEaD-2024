# AHEaD-2023

## Fairness in Decision-Making for Health Equity: Chronic Kidney Disease

*Faculty Mentor*: Sherri Rose, [sherrirose@stanford.edu](mailto:sherrirose@stanford.edu) </br>
*Near-Peer Mentor*: Marika Cusick, [mmcusick@stanford.edu](mailto:mmcusick@stanford.edu)

## Table of contents
- [Week 1](#week-1-june-26---june-30)
- [Week 2](#week-2-july-3---july-7)
- [Week 3](#week-3-july-10---july-14)
- [Week 4](#week-4-july-17---july-21)
- [Week 5](#week-5-july-24---july-28)
- [Week 6](#week-6-july-31---august-4)
- [Week 7](#week-7-august-7---august-11)

## Project description
What constitutes a fair or unfair algorithm is context specific. Metrics for evaluating fairness have been developed, as have methods for prioritizing measures of fairness when building algorithms. However, algorithms are not neutral and optimization choices will reflect a specific value system and the distribution of power to make these decisions. Data also reflect societal bias, such as structural racism. Algorithmic fairness research spans many fields, including sociology, ethics, computer science, statistics, and population health. These concepts are incredibly important given the potential for and actual realized harm to marginalized groups. This summer, students will have an opportunity to learn more about ethical pipelines for algorithms and contribute to an ongoing project in chronic kidney disease clinical decision-making. 

To make treatment decisions regarding chronic kidney disease (CKD), providers are reliant on a clinical algorithm, the estimated glomerular filtration rate (eGFR) formula to gauge severity of CKD. Prior to 2021, different versions of the eGFR formula included a race-based adjustment, which was disproven to have clinical justification and potentially exacerbated racial disparities. 

On December 1st, 2021, Stanford Health Care (SHC) implemented a new version of the eGFR formula (CKD-EPI 2021) that no longer has a race adjustment. During the summer, students will help determine which population groups at SHC were the most impacted by the eGFR formula change. 

## Week 1 (June 26 - June 30)

#### *Literature review: what is the eGFR formula?*

During the first week, youu will read about CKD and how the eGFR formula defines severity of disease. 

**Readings**:
- [Chronic Kidney Disease (CKD)](https://www.kidney.org/atoz/content/about-chronic-kidney-disease)
- [Estimated Glomerular Filtration Rate (eGFR)](https://www.kidney.org/atoz/content/gfr)
- [Assessing Kidney Function - Measured and Estimated Glomerular Filtration Rate](https://www.nejm.org/doi/full/10.1056/nejmra054415)

**Tasks**: 
- Use [PubMed](https://pubmed.ncbi.nlm.nih.gov/) to find a recent relevant article on eGFR formulas and CKD 
- MeSH terms:
    - "Renal Insufficiency, Chronic"[Mesh]
    - "Glomerular Filtration Rate"[Mesh]
    - "Cohort Studies"[Mesh]
- Summarize the article in 3-5 sentences focusing on the goal of the study, how eGFR played a role, and key findings.


## Week 2 (July 3 - July 7)

#### *Literature review: How was the eGFR formula race-adjusted?*

During the second week, students will learn about the eGFR formula race adjustment and the new version of the eGFR formula that no longer relies on the race adjustment.

**Readings**:
- [Hidden in Plain Sight - Reconsidering the Use of Race Correction in Clinical Algorithms](https://www.nejm.org/doi/10.1056/NEJMms2004740)
- [Reconsidering the Consequences of Using Race to Estimate Kidney Function](https://jamanetwork.com/journals/jama/article-abstract/2735726)
- [A New Equation to Estimate Glomerular Filtration Rate ](https://www.acpjournals.org/doi/10.7326/0003-4819-150-9-200905050-00006)
- [New Creatinine and Cystatin-C-Based Equations to Estimate GFR without Race](https://www.nejm.org/doi/full/10.1056/NEJMoa2102953)

**Tasks**: 
- Use [PubMed](https://pubmed.ncbi.nlm.nih.gov/) to find an additional recent relevant article on potential impacts of eGFR formula race adjustment 

- MeSH terms:
    - "Renal Insufficiency, Chronic"[Mesh]
    - "Glomerular Filtration Rate"[Mesh]
    - "Retrospective Studies"[Mesh]
- Summarize the article in 3-5 sentences focusing on the goal of the study and key findings.

## Week 3 (July 10 - July 14)

#### *Data analysis: getting acquainted with the data*

During the third week, students will begin to work with the simulated dataset. They will explore each of the dataset’s columns and provide some summary statistics and data visualization. The dataset is available on our GitHub under the data folder as a csv and excel file. 

The data contains the following columns: 
- patient_id: Unique patient identifier
- Sr_Cr: serum creatinine laboratory value (mg/dL)
- age: patient age
- Asian: dummy variable for patient being documented as Asian (race)
- Other: dummy variable for patient being documented as Other (race)
- Unknown: dummy variable for patient being documented as Unknown (race)
- Native Hawaiian or Other Pacific Islander: dummy variable for patient being documented as Native Hawaiian or Other Pacific Islander (race)
- Black or African American: dummy variable for patient being documented as Black or African American (race)
- American Indian or Alaska Native: dummy variable for patient being documented as American Indian or Alaska Native (race)
- White: dummy variable for patient being documented as White (race)
- ethnicity: documented patient ethnicity
- sex: documented patient sex
- county: patient county
- hypertension: dummy variable for patient documented as having hypertension
- diabetes: dummy variable for patient documented as having diabetes (type II)
- CKD: dummy variable for patient documented as having CKD
- ESRD: dummy variable for patient documented as having end-stage renal disease (ESRD)

For the continuous variables, compute the mean, median, and standard deviation. For the categorical variables, compute counts and percentages. 


## Week 4 (July 17 - July 21)

#### *Data analysis: compute eGFR values*

During the fourth week, students will begin computing eGFR values according to the CKD-EPI 2009 and 2021 eGFR formulas. To calculate eGFR, they will need to use the following variables: serum creatinine, age, sex, and race (Black or African American). They will also classify patients into CKD stages according to their eGFR values.

They will refer to the eGFR formulas here: 
- [CKD-EPI (2009)](http://nephron.com/epi_equation)
- [CKD-EPI (2021)](https://www.kidney.org/content/ckd-epi-creatinine-equation-2021)

They can manually validate their calculation using the calculator on [this website](https://www.mdcalc.com/calc/3939/ckd-epi-equations-glomerular-filtration-rate-gfr).

Stages of CKD are determined by eGFR as per [this website](https://www.kidney.org/atoz/content/gfr).

## Week 5 (July 24 - July 28)

#### *Data analysis: differences by population group*

During the fifth week, students will compare how the eGFR and CKD stage distribution differs when using the CKD-EPI 2009 and CKD-EPI 2021 eGFR formulas. 

They will identify if differences in the distributions are more evident in certain population subgroups, such as racial and ethnic groups (e.g., American Indian or Alaska Native, Asian, Black or African American, Native Hawaiian or Other Pacific Islander, Other, White, Unknown). 

## Week 6 (July 31 - August 4)

#### *Data analysis: wrap up*

During the sixth week, they will continue to work on their data analysis and finalize their results in advance of the final presentations. We will conduct code and results review. 

## Week 7 (August 7 - August 11)

#### *Final presentations*

During the final week of the program, they will prepare their final project presentations. 


