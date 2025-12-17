# Behavioral risk factors for non-prescription tranquilizer use

This project analyzes the behavioral and social determinants of non-prescription anxiolytic consumption in Argentina. The study utilizes data from the 2022 National Survey on Consumption and Care Practices (ENCoPraC) to identify risk profiles associated with the unsupervised use of psychotropic drugs.
This analysis examines lifetime prevalence to maximize statistical power and compare experimental users against the general population.

> **Note:** The source code (`.Rmd`) and the full academic report (`.pdf`) contained in this repository are in Spanish, as they were originally submitted as a final project for the National University of Córdoba (UNC). This README provides an English summary of the methodology and results.

## Methodology
The analysis was conducted using R. The workflow included data cleaning, exploratory data analysis (EDA), and multivariate modeling.
The source of the data is a representative sample of 11,206 valid cases from the ENCoPraC 2022 dataset. A Binomial Logistic Regression (GLM) was fitted to predict the probability of lifetime consumption, controlling for sociodemographic and behavioral variables simultaneously. Key libraries were used, like `tidyverse` for data manipulation, `gtsummary` for statistical tables, `broom` for model tidying, and `kableExtra` for reporting.

## Results
The multivariate analysis indicated that sociodemographic variables (age, sex, and socioeconomic status) were not statistically significant predictors when controlling for behavioral factors. The consumption of tranquilizers without a prescription is primarily driven by risk perception and prior self-medication habits.

### Risk perception as a protective factor
A strong inverse relationship was identified between perceived risk and consumption behavior. Individuals who perceive a "Great Risk" associated with tranquilizer use are 77% less likely to have consumed them without a prescription (OR = 0.23; p < 0.001). Even a perception of "Slight Risk" significantly reduces the probability of consumption (OR = 0.51).

### Mental health consultation and unsupervised use
A positive correlation was found between formal mental health consultation and unsupervised consumption. Individuals who have consulted a professional for anxiety or depression show an 82% increase in the probability of using non-prescription tranquilizers (OR = 1.82; p < 0.001). This suggests that formal treatment does not necessarily replace informal use; rather, they may coexist as complementary coping strategies.

### The role of self-medication habits
General behavior regarding medication use is a strong predictor. A tendency to self-medicate for other physical ailments (e.g., pain relief) nearly doubles the risk of consuming psychotropic drugs without a prescription (OR = 1.72).

## Repository Structure
* **analysis_encoprac.Rmd**: Source code containing the data processing pipeline and model specification.
* **encopracfinal-Carbajal.pdf**: The full rendered report, including detailed descriptive tables and theoretical discussion (in Spanish).
* **base_usuario_encoprac2022.txt**: The raw dataset used for the analysis.

## Usage Instructions
To reproduce the analysis:
1.  Clone this repository.
2.  Open the project in RStudio.
3.  Ensure the dataset file (`base_usuario_encoprac2022.txt`) is located in the root directory.
4.  Render the `.Rmd` file using `knitr`.

---
By **Juana Luz Carbajal** 

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-blue?style=flat&logo=linkedin)](https://www.linkedin.com/in/juanaluz/)
