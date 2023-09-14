# Stats Library in Python Cheat Sheet 📈📊

Made with :heart: by **Fardeen Ahmad Khan**

Welcome to the world of statistical analysis in Python! This cheat sheet is your comprehensive guide to using the Stats library for performing statistical calculations and analyses. Make sure to follow the author, [Fardeen Ahmad Khan](https://github.com/I-Fardeen), for more Python and Data Science insights! 🙌

📊 **1. Descriptive Statistics**:
   - Calculate basic statistics like mean, median, mode, and standard deviation.

   ```python
   import statistics as stats

   data = [1, 2, 2, 3, 3, 3, 4, 4, 5]
   mean = stats.mean(data)
   median = stats.median(data)
   mode = stats.mode(data)
   stdev = stats.stdev(data)
   ```

📈 **2. Probability Distributions**:
   - Work with probability distributions like normal, binomial, and Poisson.

   ```python
   from scipy.stats import norm, binom, poisson

   # Normal distribution
   normal_dist = norm(loc=0, scale=1)
   ```

📉 **3. Hypothesis Testing**:
   - Perform hypothesis tests such as t-tests and chi-squared tests.

   ```python
   from scipy.stats import ttest_ind, chisquare

   # Independent t-test
   t_stat, p_value = ttest_ind(group1_data, group2_data)
   ```

🔍 **4. Correlation and Regression**:
   - Calculate correlation coefficients and perform linear regression.

   ```python
   from scipy.stats import pearsonr, linregress

   # Pearson correlation coefficient
   corr_coeff, _ = pearsonr(x, y)
   ```

🌡️ **5. ANOVA**:
   - Analyze variance between groups using ANOVA.

   ```python
   from scipy.stats import f_oneway

   # One-way ANOVA
   f_stat, p_value = f_oneway(group1_data, group2_data, group3_data)
   ```

📚 **6. Probability and Random Variables**:
   - Generate random variables and calculate probabilities.

   ```python
   from scipy.stats import rv_discrete

   # Discrete random variable
   custom_dist = rv_discrete(name='custom', values=([1, 2, 3], [0.1, 0.4, 0.5]))
   ```

📊 **7. Confidence Intervals**:
   - Compute confidence intervals for sample statistics.

   ```python
   import statsmodels.stats.api as sms

   ci = sms.DescrStatsW(data).tconfint_mean()
   ```

📉 **8. Non-Parametric Tests**:
   - Perform non-parametric tests like the Wilcoxon signed-rank test.

   ```python
   from scipy.stats import wilcoxon

   # Wilcoxon signed-rank test
   stat, p_value = wilcoxon(data1, data2)
   ```

With the Stats library in Python, you can explore and analyze your data with confidence. Dive into statistical analysis and unlock valuable insights! 📈📊

Made with :heart: by **Fardeen Ahmad Khan**
