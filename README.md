# World Happiness Report Analysis

## 📊 High-Level Overview

This dataset contains information about various countries and metrics that contribute to the happiness of their citizens. It includes variables such as GDP, life expectancy, freedom, generosity, and more. One unique feature is the **Dystopia Residual**, which compares each country to a hypothetical dystopia—the least happy country possible.

Importantly, there are **no null values** in the dataset, and all values appear to be legitimate.

## 📦 Data Quality and Initial Observations

- No missing values.
- Extreme values like 0 in variables such as Freedom and Generosity appear valid.
- No pre-processing is necessary beyond potential optional transformations (e.g., adjusting the Dystopia Residual).

Boxplots and initial visualizations show that:
- **Economy** and **Health** have the strongest linear relationships with Happiness Score.
- **Freedom** and **Trust** appear to have the weakest.
- Most variables show a **left skew**, with some countries scoring much lower than the rest.

---

## 🎯 Objectives

1. What is the relationship between **Generosity** and **Happiness Score**?
2. Which **regions** of the world have the highest/lowest happiness scores?
3. Do the relationships between variables and happiness change when splitting the dataset by **Happiness Rank**?

---

## 📈 Objective 1: Generosity vs. Happiness Score

We explore the relationship between Generosity and Happiness Score using:

- A **scatterplot** to visualize patterns.
- A **correlation heatmap** to quantify the relationship.

### 🔍 Conclusion

Generosity shows a **very weak positive correlation** (around 0.2) with Happiness Score. There is no strong visual pattern indicating a clear relationship.

---

## 🌍 Objective 2: Regional Happiness Trends

To identify regional differences in happiness:

- Grouped data by **Region** and computed the mean for each metric.
- Created a **bar plot** of Happiness Scores by region.

### 🔍 Conclusion

- **Australia and New Zealand** have the highest average happiness scores.
- **Sub-Saharan Africa** has the lowest.
- Regions with higher scores generally also have stronger metrics in Economy and Health.

---

## 🔄 Objective 3: Correlation Differences by Happiness Rank

We split the dataset in half based on Happiness Rank:
- Top 50% of countries (higher happiness)
- Bottom 50% of countries (lower happiness)

We then:
- Computed separate correlation matrices.
- Calculated the **difference** between the two.
- Visualized specific relationships (Trust and Generosity) using **scatterplots**.

### 🔍 Conclusion

- The **correlation of Trust and Generosity** with Happiness Score appears to change between the two halves.
- Scatterplots, however, do not show clear visual distinctions.
- More **rigorous statistical testing** (e.g., hypothesis testing) would be needed to confirm any differences.

---

## ⚠️ Potential Ethical Considerations

There may be **inaccuracies or biases** in how countries report data:

- Countries could **inflate metrics** like Trust or Generosity to improve public perception.
- Similar data manipulation occurred during the COVID-19 pandemic, highlighting the need to **critically evaluate** self-reported national statistics.

---

## 📁 Dataset Summary

- **Countries:** 157
- **Variables:** Happiness Score, GDP, Health, Freedom, Generosity, etc.
- **No missing values**
- **Numerical and visual exploration** completed using boxplots, scatterplots, heatmaps.

---

*This analysis was conducted using Python (Pandas, Seaborn, Matplotlib).*
