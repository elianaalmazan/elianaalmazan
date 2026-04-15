## Regional Disparities in Cardiovascular & Cerebrovascular Mortality across New York State

This project examines regional disparities in cardiovascular and cerebrovascular mortality rates across 63 New York counties (2008–2012) using the NY Community Health Obesity and Diabetes Related Indicators dataset. Analyses include factorial MANOVA, post-hoc Tukey HSD tests, and multilinear regression with diet, exercise, and region as predictors. Results show significant regional variation in both outcomes, with region serving as a strong predictor of cerebrovascular mortality (R² = 0.67). Visualizations were built in R (ggplot2) and Python (matplotlib/seaborn).

---

# Executive Summary

This project investigates regional disparities in cardiovascular and cerebrovascular mortality rates across New York State's nine regions using the *Community Health Obesity and Diabetes Related Indicators: 2008–2012* dataset (63 counties). Two analyses were performed:

**Key Findings:**

-   **MANOVA** revealed highly significant differences in mortality rates across NY regions (Pillai's trace p = 8.52 × 10⁻⁹), rejecting the null hypothesis of equal means.
-   **Post-hoc Tukey tests** identified Western New York and Hudson Valley as the most significantly different pair for cardiovascular mortality (p = 0.030), and New York City vs. Finger Lakes, Northeastern NY, and Western NY as the most divergent for cerebrovascular mortality (p ≈ 0.0000001).
-   **Multilinear regression** found that region significantly predicted cerebrovascular mortality (R² = 0.671, p = 1.7 × 10⁻⁹), but not cardiovascular mortality (R² = 0.330, p = 0.014 at α = 0.01).

------------------------------------------------------------------------

# Introduction

Cardiovascular disease is the leading cause of death in the United States. Every year approximately 697,000 people die of heart disease (Centers for Disease Control and Prevention, 2022). Cardiovascular disease encompasses numerous conditions such as heart failure, coronary heart disease, or any other condition affecting the heart and blood vessels. Cerebrovascular disease, or stroke, occurs when the blood supply to the brain is interrupted.

Both of these diseases disproportionately affect low- and middle-income populations (Kelli et al., 2018). Key social determinants associated with both conditions include income level, education, employment status, and broader socioeconomic factors. The relationship between diet, exercise, and cardiovascular and cerebrovascular disease is crucial in maintaining a healthy cardiovascular system and reducing the risk of these conditions.

------------------------------------------------------------------------

# Dataset

For this project, the dataset *"Community Health Obesity and Diabetes Related Indicators: 2008–2012"* (Health.data.ny.gov, 2021) was used. It comprises 63 New York counties and their regional classifications, along with numerous health indicators including:

-   Diabetes and obesity hospitalizations for adults and children
-   Cirrhosis mortality rates
-   Diet and exercise habits
-   Cardiovascular and cerebrovascular mortality rates

The primary research questions were:

1.  Are there significant differences in the means of cardiovascular and cerebrovascular mortality rates per 100,000 people across the nine regions of New York?
2.  Is there a **linear** relationship between these mortality rates and diet (age-adjusted percentage of adults eating 5 or more fruits or vegetables per day), lack of exercise (age-adjusted percentage of adults who did not participate in leisure-time physical activity in the last 30 days), and region?

------------------------------------------------------------------------

# References

Bedre, R. (2021, October 1). *MANOVA using R (with examples and code)*. Data science blog. <https://www.reneshbedre.com/blog/manova.html>

Centers for Disease Control and Prevention. (2022, October 14). *Stroke facts*. <https://www.cdc.gov/stroke/facts.htm>

Health.data.ny.gov. (2021, February 25). *Community health obesity and diabetes related indicators: 2008–2012*. HealthData.gov. <https://healthdata.gov/State/Community-Health-Obesity-and-Diabetes-Related-Indi/95h9-42q2>

Kelli, H. M., et al. (2018). Socioeconomic status and cardiovascular outcomes. *Circulation*. <https://www.ahajournals.org/doi/10.1161/CIRCULATIONAHA.117.029652>

Navarro, D. (2019). *Learning statistics with R: A tutorial for psychology students and other beginners* (version 0.6.1). Chapter 16: Factorial ANOVA. <https://learningstatisticswithr.com/book/anova2.html#factorialanovasimple>

Zach. (2022, February 23). *How to plot multiple linear regression results in R*. Statology. <https://www.statology.org/plot-multiple-linear-regression-in-r/>
