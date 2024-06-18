# AHEaDb 2024

## Fairness in Decision-Making for Health Equity: Chronic Kidney Disease

*Faculty Mentor*: Sherri Rose, [sherrirose@stanford.edu](mailto:sherrirose@stanford.edu) </br>
*Near-Peer Mentor*: Catherine Duarte, [catherine_duarte@stanford.edu](mailto:catherine_duarte@stanford.edu)

## Table of contents
- [Week 1](#week-1-june-24---june-28)
- [Week 2](#week-2-july-1---july-5)
- [Week 3](#week-3-july-8---july-12)
- [Week 4](#week-4-july-15---july-19)
- [Week 5](#week-5-july-22---july-26)
- [Week 6](#week-6-july-29---august-2)
- [Week 7](#week-7-august-5---august-9)

## Project description
What constitutes a fair or unfair algorithm is context specific. Metrics for evaluating fairness have been developed, as have methods for prioritizing measures of fairness when building algorithms. However, algorithms are not neutral and optimization choices will reflect a specific value system and the distribution of power to make these decisions. Data also reflect societal bias, such as structural racism. Algorithmic fairness research spans many fields, including sociology, ethics, computer science, statistics, and population health. These concepts are incredibly important given the potential for and actual realized harm to marginalized groups. This summer, students will have an opportunity to learn more about ethical pipelines for algorithms and participate in a project in chronic kidney disease clinical decision-making. 

To make treatment decisions regarding chronic kidney disease (CKD), providers are reliant on a clinical algorithm, the estimated glomerular filtration rate (eGFR) formula to gauge severity of CKD. Prior to 2021, different versions of the eGFR formula included a race-based adjustment, which was disproven to have clinical justification and potentially exacerbated racial disparities. 

On December 1st, 2021, Stanford Health Care (SHC) implemented a new version of the eGFR formula (CKD-EPI 2021) that no longer has a race adjustment. During the summer, students will help determine which population groups at SHC may have been impacted by the eGFR formula change. 

## Week 1 (June 24 - June 28)

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


## Week 2 (July 1 - July 5)

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

## Week 3 (July 8 - July 12)

#### *Data analysis: Getting acquainted with the data*

During the third week, students will begin to work with the simulated dataset. They will explore each of the dataset’s columns and provide some summary statistics and data visualization. The dataset is available on our GitHub under the data folder as a csv and excel file. 

The data contains the following columns: 
- patient_id: Unique patient identifier
- Sr_Cr: serum creatinine laboratory value (mg/dL)
- age: patient age
- Asian: indicator variable for patient being documented as Asian (race)
- Other: indicator variable for patient being documented as an additional race group (race)
- Unknown: indicator variable for patient being documented as Unknown (race)
- Native Hawaiian or Other Pacific Islander: indicator variable for patient being documented as Native Hawaiian or Other Pacific Islander (race)
- Black or African American: indicator variable for patient being documented as Black or African American (race)
- American Indian or Alaska Native: indicator variable for patient being documented as American Indian or Alaska Native (race)
- White: indicator variable for patient being documented as white (race)
- ethnicity: documented patient ethnicity
- sex: documented patient sex
- county: patient county
- hypertension: indicator variable for patient documented as having hypertension
- diabetes: indicator variable for patient documented as having diabetes (type II)
- CKD: indicator variable for patient documented as having CKD
- ESRD: indicator variable for patient documented as having end-stage renal disease (ESRD)

Create and share a google doc with the following: 
- For the continuous variables, compute the mean, median, and standard deviation.
- For the categorical variables, compute counts and percentages.
- Play around with data visualization.
- Comment on any "data discoveries." Did you notice anything "weird" about the data?
- Summarize the most important findings in 3-4 sentences. How might you visualize the key findings? (e.g. visualization is extra, but this could be useful to have in your final presentation. 

## Week 4 (July 15 - July 19)

#### *Data analysis: compute eGFR values*

During the fourth week, students will begin computing eGFR values according to the CKD-EPI 2009 and 2021 eGFR formulas. To calculate eGFR, they will need to use the following variables: serum creatinine, age, sex, and race (Black or African American). They will also classify patients into CKD stages according to their eGFR values.

They will refer to the eGFR formulas here: 
- [CKD-EPI (2009)](http://nephron.com/epi_equation)
- [CKD-EPI (2021)](https://www.kidney.org/content/ckd-epi-creatinine-equation-2021)

They can manually validate their calculation using the calculator on [this website](https://www.mdcalc.com/calc/3939/ckd-epi-equations-glomerular-filtration-rate-gfr).

Stages of CKD are determined by eGFR as per [this website](https://www.kidney.org/atoz/content/gfr).

## Week 5 (July 22 - July 26)

#### *Data analysis: Differences by group*

During the fifth week, students will compare how the eGFR and CKD stage distribution differs when using the CKD-EPI 2009 and CKD-EPI 2021 eGFR formulas among patients with different characteristics. For example, they will identify if differences in the distributions are more evident in certain subgroups, such as racial and ethnic groups (e.g., American Indian or Alaska Native, Asian, Black or African American, Native Hawaiian or Other Pacific Islander, Other, White, Unknown). 

After computing the eGFR value and stages for each individual patient, we can identify the following two outcomes: 
1) Binary outcome for whether or not the patient has a different stage according to CKD-EPI 2009 and CKD-EPI 2021
2) Percent change between the CKD-EPI 2009 and CKD-EPI 2021 values

First, fit a logistic regression with patient characteristics as the dependent variables and the binary outcome for switching stages (outcome 1) as the independent variable. Interpret the coefficients of the patient characteristics thinking about the following questions: 
- Are patients of a particular trait more or less likely to have switched stages?
- What is the increase/decrease in the likelihood of switching stages?
- Are the results statistically significant?

***If there is time! (We can always defer this to next week!)***

Next, fit a linear regression with patient characteristics as the dependent variables and percent change between CKD-EPI 2009 and CKD-EPI 2021 value (outcome 2) as the independent variable. Interpret the coefficients of the patient characteristics thinking about the following questions: 
- Are patients of a particular trait more likely to have larger percent changes?
- For a given patient characteristic, what is the expected change in the outcome?
- Are the results statistically significant?

## Week 6 (July 29 - August 2)

#### *Data analysis: wrap up*

During the sixth week, they will continue to work on their data analysis and finalize their results in advance of the final presentations. We will conduct code and results review. 

## Week 7 (August 5 - August 9)

#### *Final presentations*

During the final week of the program, they will prepare their final project presentations. 


