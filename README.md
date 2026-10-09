# Derivable Judgement: A Statistical Decision-Making Model

## GitHub Repository Description
A Python-based statistical analysis project using a synthetic public-health dataset to demonstrate inferential statistics, hypothesis testing, confidence intervals, z-test, Welch's t-test, chi-square test, ANOVA, covariance, correlation, and data visualization.

## Overview
This project applies statistical methods to simulated health records to explore relationships between demographic and lifestyle factors and health outcomes such as diabetes and hypertension. The notebook includes data generation, data-quality checks, exploratory analysis, hypothesis tests, visualizations, and a consolidated results table.

> **Important:** The dataset is synthetic and created for educational demonstration only. It does not contain real patient records and must not be used for medical decisions or interpreted as evidence of real-world causation.

## Project Objectives
- Generate a reproducible dataset containing 1,000 synthetic health records.
- Inspect data types, missing values, duplicate rows, and duplicate record IDs.
- Summarize numerical variables and disease prevalence.
- Calculate a 95% confidence interval for mean age.
- Compare BMI between records with and without diabetes using Welch's independent-samples t-test.
- Test the association between smoking status and diabetes using a chi-square test.
- Demonstrate one-way ANOVA across age groups for a binary diabetes outcome.
- Demonstrate a z-test comparing the sample glucose mean with an explicitly assumed reference mean.
- Calculate covariance and Pearson correlation between age and BMI.
- Create clear plots and a consolidated results table.

## Dataset
The notebook generates the dataset programmatically with 1,000 rows and 15 fields:

| Field | Description |
|---|---|
| `record_id` | Unique synthetic record identifier |
| `age_group` | Age category |
| `age` | Age in years |
| `weight` | Simulated weight |
| `gender` | Gender category |
| `region` | Geographic region category |
| `smoking_status` | Smoking category |
| `exercise_frequency` | Exercise frequency category |
| `bmi` | Simulated body mass index |
| `blood_pressure` | Simulated systolic blood pressure |
| `diabetes` | Boolean diabetes outcome |
| `hypertension` | Boolean hypertension outcome |
| `cholesterol_level` | Simulated cholesterol level |
| `glucose_level` | Simulated glucose level |
| `visit_date` | Simulated visit date |

All records and outcomes are generated for this project; they are not real clinical data.

## Statistical Methods
1. **Confidence interval:** 95% t-based confidence interval for mean age.
2. **Welch's t-test:** Compares average BMI for records with and without diabetes.
3. **Chi-square test of independence:** Tests association between smoking category and diabetes status.
4. **One-way ANOVA:** Classroom demonstration comparing 0/1 diabetes outcomes across age groups.
5. **Z-test demonstration:** Compares sample mean glucose with an assumed reference mean of 100 mg/dL.
6. **Covariance and Pearson correlation:** Examines joint variation and linear association between age and BMI.

### Interpretation rules
- Significance level: `alpha = 0.05`.
- If `p-value < 0.05`, reject the relevant null hypothesis, subject to test assumptions.
- If `p-value >= 0.05`, fail to reject the null hypothesis; this does not prove the null hypothesis is true.
- Statistical association does not establish causation.

### Methodological notes
- The z-test uses the sample standard deviation as an estimate and is included for learning; a one-sample t-test is often preferable when the population standard deviation is unknown.
- Classical ANOVA assumptions are not ideal for a binary outcome such as diabetes. The ANOVA section is included to meet the educational exercise; a chi-square test or logistic regression is generally more appropriate for formal inference about a binary outcome.
- The glucose reference mean of 100 mg/dL is an assumed demonstration value, not a threshold supplied by the project brief or a diagnostic recommendation.

## Tools and Libraries
- Python 3
- Jupyter Notebook
- NumPy
- Pandas
- SciPy
- Matplotlib
- Seaborn

## How to Run
### Option 1: Google Colab
1. Download `Pr.2_Derivable_Judgement.ipynb` from this repository.
2. Open [Google Colab](https://colab.research.google.com/).
3. Choose **File → Upload notebook** and upload the notebook.
4. Run the cells from top to bottom using **Runtime → Run all**.
5. Review the printed statistics, charts, and final results table.

### Option 2: Local Jupyter environment
1. Install Python 3 and Jupyter Notebook or JupyterLab.
2. Install the dependencies:
   ```bash
   pip install numpy pandas scipy matplotlib seaborn
   ```
3. Open the notebook and run all cells from top to bottom.

The notebook's final cell exports:
- `health_dataset.csv`
- `statistical_test_results.csv`

## Repository Structure
```text
Derivable-Judgement-Project/
├── Pr.2_Derivable_Judgement.ipynb
├── README.md
├── health_dataset.csv                 # Generated after running the notebook
└── statistical_test_results.csv       # Generated after running the notebook
```

You can also add a `Theory_Notes.pdf` file if your assignment submission requires a separate PDF containing the Part A definitions.

## Expected Outputs
- Dataset preview and data-quality report
- Descriptive statistics and disease prevalence
- Confidence interval and hypothesis-test results
- Critical values, p-values, and decisions
- Visualizations for diabetes prevalence, smoking status, age, BMI, and glucose
- Consolidated statistical results table
- CSV exports of the generated dataset and results

## Limitations
- Data are synthetic and do not represent real people.
- Generated patterns depend on assumptions written into the data-generation code.
- Results are intended for learning and demonstration only.
- Findings must not be used for medical diagnosis, treatment, or real-world public-health decisions.

## Author
Add your name here.

## License
Add a license if you intend to make the repository reusable by others. If you do not choose a license, normal copyright rules apply.


