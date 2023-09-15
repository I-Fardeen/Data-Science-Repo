# ANOVA in Python Cheat Sheet 📊🔬

Made with :heart: by **Fardeen Ahmad Khan**

Welcome to the world of Analysis of Variance (ANOVA) in Python! This cheat sheet provides both theory and practical implementation to help you understand and perform ANOVA tests effectively. Don't forget to follow the author, [Fardeen Ahmad Khan](https://github.com/I-Fardeen), for more Python and Data Science insights! 🙌

🔍 **1. What is ANOVA?**:
   - ANOVA is a statistical method used to analyze the differences among group means in a sample.
   - It's used when you have more than two groups to compare.

📈 **2. Types of ANOVA**:
   - One-Way ANOVA: Compares means of three or more independent (unrelated) groups.
   - Two-Way ANOVA: Analyzes the influence of two different categorical independent variables on one dependent variable.
   - Repeated Measures ANOVA: Analyzes the differences with related groups (e.g., repeated measurements over time).

📚 **3. Assumptions of ANOVA**:
   - Independence of Observations.
   - Homogeneity of Variance.
   - Normality of Residuals.

📊 **4. Implementation with Python**:
   - Import the necessary libraries.

   ```python
   import scipy.stats as stats
   ```

🔬 **5. One-Way ANOVA**:
   - Calculate F-statistic and p-value.

   ```python
   f_statistic, p_value = stats.f_oneway(group1_data, group2_data, group3_data)
   ```

📈 **6. Two-Way ANOVA**:
   - Use `ols` from `statsmodels` for two-way ANOVA.

   ```python
   import statsmodels.api as sm
   from statsmodels.formula.api import ols

   model = ols('dependent_var ~ C(factor_var1) * C(factor_var2)', data=df).fit()
   anova_table = sm.stats.anova_lm(model, typ=2)
   ```

📊 **7. Repeated Measures ANOVA**:
   - Use `rm_anova` from `pingouin` library for repeated measures ANOVA.

   ```python
   import pingouin as pg

   anova = pg.rm_anova(data=df, dv='dependent_var', within='time_var', subject='subject_id')
   ```

📉 **8. Post Hoc Tests**:
   - If ANOVA indicates significant differences, perform post hoc tests (e.g., Tukey's HSD).

   ```python
   from statsmodels.stats.multicomp import pairwise_tukeyhsd

   tukey_results = pairwise_tukeyhsd(endog=df['dependent_var'], groups=df['group_var'])
   ```

🔑 **9. Interpretation**:
   - Evaluate p-values to determine whether group means are significantly different.
   - Post hoc tests help identify which groups differ from each other.

With this ANOVA cheat sheet, you're well-equipped to analyze and compare group means effectively in Python. Dive into the world of statistical analysis! 📊🔬

Made with :heart: by **Fardeen Ahmad Khan**
