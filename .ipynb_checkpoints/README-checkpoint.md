# Age Data Explorer

Exploratory analysis of the scikit-learn diabetes dataset (442 patients), looking at which clinical features track one-year disease progression.

## The data
Source: scikit-learn's `load_diabetes` (originally Efron et al., 2004, *Annals of Statistics*).
442 patients; 10 standardized features (age, sex, BMI, blood pressure, 6 serum measures) and a `target` = disease progression one year after baseline.
The data loads directly from scikit-learn (`load_diabetes(as_frame=True)`).

## Key findings
  - BMI and s5 were the most heavily correlated with disease progression
  - the mean progression for those with high-BMI was ~191 vs ~113 for low_BMI
  - age was weakly correlated to progression and sex was essentially uncorrelated
  - sexes were not labeled in the data so only the difference between them could be determined

![Feature correlations with disease progression](figures/features_correlation.png)

## How to run it
```bash
git clone https://github.com/EzraParsons1/age-data-explorer.git
cd age-data-explorer
mamba env create -f environment.yml
mamba activate pydata
jupyter lab   # then open and run eda.ipynb top to bottom
```