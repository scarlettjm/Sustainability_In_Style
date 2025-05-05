# Sustainability in Style: Analyzing the Influence of Environmental Ethics on Gen Z Consumers

This project explores the relationship between environmental values and consumer purchasing habits among Generation Z, particularly within the fashion industry. Using a dataset from the National Institute of Health (NIH), we investigate how sustainability-focused attitudes—such as trend sensitivity, eco-consciousness, and corporate responsibility—impact buying behaviors.

## Research Question

**How do sustainability-related values influence Gen Z consumers' clothing purchasing behavior?**  
We examine whether ethical production, environmental respect, and fashion trends predict behavioral patterns such as buying eco-labeled products and avoiding unsustainable brands.

## Files

| File Name | Description |
|-----------|-------------|
| `fashion2.csv` | Cleaned subset of survey data with Gen Z respondents |
| `genz_fashion_analysis.R` | Full R script including cleaning, visualization, and correlation testing |
| `Sustainability_in_Style_Case_Study.pdf` | In-depth writeup of the project, methodology, and results |

## Dataset

- **Source**: NIH dataset (via Colasante & D’Adamo)
- **Participants**: 402 total; filtered to Gen Z respondents (age ≤ 26)
- **Features used**:
  - `i_clothes_fashion` – Trend importance
  - `i_clothes_environment` – Environmental value
  - `pro_bio2_clothes` – Eco-labeled purchase frequency
  - `pro_brown_firms` – Avoidance of unsustainable brands
  - Demographics: age, education, income, gender

## Workflow Overview

### 1. Cleaning
- Removed irrelevant columns and non-Gen Z rows
- Assigned numeric values to Likert-scale responses
- Filtered to essential features

### 2. EDA
- Created histograms to explore value frequency distributions
- Calculated means and frequencies for all key variables

### 3. Correlation Testing
- Created 4 pairs of variable subsets
- Used both **Pearson** and **Spearman** correlations
- Tested for normality with Q-Q plots and Shapiro-Wilk tests

### 4. Visualization
- Histograms and scatterplots using `ggplot2`, `PerformanceAnalytics`, `corrplot`, and `GGally`

## 📈 Key Results

| Test | Variables | Pearson r | Spearman ρ |
|------|-----------|-----------|-------------|
| 1 | Eco purchase × Environmental value | 0.46 | 0.44 |
| 2 | Eco purchase × Trend value | 0.19 | 0.17 |
| 3 | Avoid unsustainable × Environmental value | 0.36 | 0.34 |
| 4 | Avoid unsustainable × Trend value | 0.13 | 0.17 |

- Gen Z showed stronger alignment with **environmental values** than with trend-following.
- Moderate correlation exists between **values** and **behavior**, but aesthetic appeal still matters.
- Clear opportunity for brands to merge **style** and **sustainability**.

## 🔍 Tools Used

- **R (RStudio)**: `tidyverse`, `ggplot2`, `car`, `PerformanceAnalytics`, `broom`, `caret`, `corrplot`
- **Excel**: Data preprocessing and manual recoding

## Citation

Dataset Source:  
> Colasante, A., & D’Adamo, I. (2022). NIH Sustainability Survey Dataset. [Zenodo]

Case Study PDF: `Sustainability_in_Style_Case_Study.pdf`

## Future Work

- Apply regression modeling to test causal relationships
- Expand dataset beyond Gen Z for generational comparisons
- Integrate survey-based intention vs. behavior analysis
