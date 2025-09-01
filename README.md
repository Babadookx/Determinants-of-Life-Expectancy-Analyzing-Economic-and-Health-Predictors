# Determinants of Life Expectancy: Analyzing Economic and Health Predictors

**Author:** Jinyi Xue  
**Date:** September 2025  

---

## 📘 Overview
This project explores **global life expectancy patterns** using World Health Organization (WHO) data.  
We evaluate both **economic** (GDP, income composition, schooling) and **health factors** (HIV/AIDS prevalence, child mortality, immunization coverage, etc.) to identify key predictors of life expectancy.  

The workflow combines **exploratory data analysis (EDA)**, **tree classification**, and **Partial Least Squares (PLS) regression** to understand complex variable relationships and improve prediction accuracy.

---

## 🔍 Key Highlights
- **Data-driven classification:** Tree model splits life expectancy into four quantile-based groups (Low, Below Average, Average, High).  
- **Key predictors:**  
  - HIV/AIDS prevalence, income composition of resources, and adult mortality are strong differentiators.  
- **PLS Regression:**  
  - Separate models for economic vs. disease-related factors.  
  - Disease-factor model slightly outperforms economic model (RMSE ≈ 4.6 vs. 4.9 years).  
- **Interpretation:** Socioeconomic development and disease control are both critical to extending life expectancy globally.

---

## 📂 Repository Files

Determinants-of-Life-Expectancy-Analyzing-Economic-and-Health  
`Life_Expectancy_Analysis.Rmd`: Main R Markdown analysis script  
`Life_Expectancy_Analysis.html`: Rendered HTML report  
`train.csv`: Training dataset  
`test.csv`: Test dataset  
`final_poster.pdf` *(optional)*: If you create a summary poster later  
`outputs/`: Optional folder for plots/tables  
`data/`: Optional folder for raw/processed data  

---

## 🧪 Methods
- **Exploratory Data Analysis:**  
  - Scatterplots, correlation matrices, boxplots by continent and development status.  
  - Quantile-based life expectancy grouping for clearer comparisons.
- **Tree Classification:**  
  - Built with `rpart` and `rpart.plot` for interpretability.  
  - Accuracy ≈ 78.5% on test data.
- **PLS Regression Models:**  
  - Economic factors vs. disease-related factors modeled separately.  
  - Cross-validation used to select optimal components.  
  - Visualizations show clustering and prediction fit.
- **Visualization Libraries:** `ggplot2`, `ggcorrplot`, `kableExtra`.

---

## 🚀 Reproducibility
1. Clone or download this repository:
   ```bash
   git clone git@github.com:Babadookx/Determinants-of-Life-Expectancy-Analyzing-Economic-and-Health.git
   ```
2. Open Life_Expectancy_Analysis.Rmd in RStudio.
3. Install required packages:
   ```Terminal
   install.packages(c("tidyverse", "tableone", "rpart", "rpart.plot", "pls", "ggcorrplot", "kableExtra", "broom", "caret"))
   ```
4. Knit to HTML or PDF:
  ```Terminal
  rmarkdown::render("Life_Expectancy_Analysis.Rmd")
  ```

