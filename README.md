# Diamond Price Prediction: Regression Analysis in R

**Course:** PSTAT 126 — Regression Analysis, UC Santa Barbara  
**Author:** Ryan Park

---

## Overview

This project analyzes what drives diamond prices using regression modeling on a random sample of 500 diamonds from the Diamonds Prices 2022 dataset. The analysis covers exploratory data analysis, correlation analysis, simple linear regression, and multiple linear regression to identify which physical and quality characteristics best predict a diamond's price.

---

## Dataset

- **Source:** Diamonds Prices 2022 (`Diamonds Prices2022.csv`)
- **Sample:** 500 randomly selected diamonds (seed: 1234567)
- **Variables:** carat, cut, color, clarity, depth, table, price, and physical dimensions (x, y, z)

---

## Analysis

**Part 1: Descriptive Statistics & EDA**
- Histograms for all continuous variables (carat, depth, table, price, x, y, z)
- Bar plots for categorical variables (cut, color, clarity)
- Correlation matrix across numeric predictors
- Multiple linear regression: `price ~ carat + cut + color + clarity + depth + table`

**Part 2: Simple Linear Regression**
- Model: `price ~ carat`
- Scatter plot with fitted regression line
- Residual diagnostics (residuals vs. fitted, Q-Q plot, etc.)
- Confidence intervals for coefficients

---

## Key Findings

- **Carat is the strongest predictor of price** (coefficient ≈ $8,841 per carat, R² = 0.91 for the full model).
- Physical dimensions x, y, and z were excluded due to near-perfect multicollinearity with carat.
- Clarity grade has a large effect on price — IF (Internally Flawless) diamonds command a ~$6,798 premium over the baseline.
- Depth and table percentage are statistically insignificant predictors of price.
- The simple linear regression of price on carat alone achieves R² = 0.836, confirming carat as the dominant driver.

---

## Files

| File | Description |
|------|-------------|
| `Final_Project.pdf` | Full written report with all analysis, plots, and interpretations |
| `Diamonds Prices2022.csv` | Raw dataset used for analysis |

---

## Tools & Libraries

- **Language:** R
- **Libraries:** `ggplot2`, base R (`lm`, `cor`, `hist`, `barplot`)
- **Methods:** EDA, correlation analysis, simple & multiple linear regression, residual diagnostics
