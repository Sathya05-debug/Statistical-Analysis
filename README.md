# 🚗 Used Car Sales – Hypothesis Testing & Statistical Analysis

This repository contains statistical analysis performed on a cleaned dataset of used car sales, with a focus on applying **hypothesis testing techniques** to draw actionable insights about the automotive resale market.

---

## 📁 Dataset

- **`car_sales_cleaned.csv`**: Contains detailed records of used cars including:
  - `make` (car brand)
  - `sellingprice` (resale price)
  - `body` (body type)
  - `transmission` (manual/automatic)
  - `color`, `year`, `condition`, `state`, etc.

---

## 🎯 Objectives

### 1️⃣ One-Sample t-Test
> **Hypothesis**: The average resale price of Toyota cars is ₹12,400.
- Method: One-sample t-test
- Tool: `scipy.stats.ttest_1samp`
- Result: Determines whether the observed Toyota resale prices significantly differ from the expected market average.

### 2️⃣ Two-Way ANOVA
> **Goal**: Analyze the impact of `body type`, `transmission`, and their interaction on black car resale prices.
- Method: Two-Way ANOVA
- Tool: `statsmodels.formula.api.ols`
- Sample: Random sample of 5000 black-colored cars
- Preprocessing: Rare body types grouped as 'Other'; filtered combinations with < 10 entries.

### 3️⃣ Chi-Square Test of Independence
> **Question**: Is the color distribution of Toyota cars significantly different from that of all cars?
- Method: Chi-square test
- Tool: `scipy.stats.chi2_contingency`
- Approach: Builds a contingency table between `color` and `make`

---

## 🛠 Tools & Libraries

- **Python 3.8+**
- [Pandas](https://pandas.pydata.org/) – Data handling
- [SciPy](https://scipy.org/) – Statistical tests
- [Statsmodels](https://www.statsmodels.org/) – ANOVA modeling
- (Optional) [Matplotlib/Seaborn](https://seaborn.pydata.org/) – Visualization

---

## 📊 Results Summary

| Test                     | Outcome                                                                 |
|--------------------------|-------------------------------------------------------------------------|
| One-Sample t-Test        | ✅ Toyota resale price is significantly different from ₹12,400          |
| Two-Way ANOVA            | ✅ Body type and transmission affect resale price of black cars         |
| Chi-Square Test          | ✅ Toyota's color distribution significantly differs from overall market |

---

## 📌 Usage

### ▶️ Run the script
Make sure to install dependencies:
```bash
pip install pandas scipy statsmodels

