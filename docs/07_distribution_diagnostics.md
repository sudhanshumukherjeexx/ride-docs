## 📘 RIDE User Manual – Panel 7: **Statistical Data Exploration**

---
### 📊 **Purpose of the Panel**

The **Distribution Diagnostics Panel** allows users to:
- Understand data shape via **skewness** and **kurtosis**
- Test for **normality** with Q-Q plots and statistical tests
- **Detect outliers** using the IQR method

This is crucial for identifying data anomalies, choosing suitable transformations, and selecting proper machine learning models.

`Recommended Reading`

- Blog: <a href="https://www.datacamp.com/tutorial/qq-plot" target="_blank" rel="noopener noreferrer">The Q-Q Plot: What It Means and How to Interpret It</a>
- Blog: <a href="https://library.virginia.edu/data/articles/understanding-q-q-plots" target="_blank" rel="noopener noreferrer">Understanding QQ Plots</a>
- Blog: <a href="https://www.sciencedirect.com/topics/earth-and-planetary-sciences/kurtosis" target="_blank" rel="noopener noreferrer">Kurtosis</a>
- Blog: <a href="https://www.itl.nist.gov/div898/handbook/eda/section3/eda35b.htm#:~:text=Kurtosis%20is%20a%20measure%20of,would%20be%20the%20extreme%20case." target="_blank" rel="noopener noreferrer">Measures of Kurtosis and Skewness</a>
- Blog: <a href="https://www.investopedia.com/terms/s/skewness.asp#:~:text=a%20probability%20distribution.-,What%20Is%20Skewness%3F,the%20bell%20curve%20is%20skewed." target="_blank" rel="noopener noreferrer">Right Skewed vs. Left Skewed Distribution</a>
- Blog: <a href="https://www.simplilearn.com/tutorials/statistics-tutorial/skewness-and-kurtosis" target="_blank" rel="noopener noreferrer">The Complete Guide to Skewness and Kurtosis</a>
- Blog: <a href="https://careerfoundry.com/en/blog/data-analytics/what-is-an-outlier/" target="_blank" rel="noopener noreferrer">What Is an Outlier?</a>
- Blog: <a href="https://www.itl.nist.gov/div898/handbook/prc/section1/prc16.htm#:~:text=An%20outlier%20is%20an%20observation,what%20will%20be%20considered%20abnormal." target="_blank" rel="noopener noreferrer">What are outliers in the data?</a>
- Blog: <a href="https://www.coursera.org/articles/what-are-outliers" target="_blank" rel="noopener noreferrer">What Are Outliers in Data Sciences?</a>


---
### 🧭 **User Workflow**

1. **Upload Dataset**  
    Choose from:
    - Initial DataFrame
    - After Missing Value Imputation
    - After Feature Encoding
    - After Feature Scaling

2. **Navigate the Tabs**:
    - **📊 Distribution & Q-Q Plots**: Visualize histograms + Q-Q plots, run normality tests.
    - **🏔️ Kurtosis**: Check how “peaked” or “flat” distributions are.
    - **↗️ Skewness**: Explore asymmetry in distributions.
    - **🔍 Outliers**: Detect extreme values using IQR logic.

3. **Interactive Visuals**:
    - Select numeric features.
    - Compare histograms and Q-Q plots.
    - Get metric summaries and AI insights.

---
### 💻 Features Breakdown

|Feature|Description|
|---|---|
|Data Source Selection|Choose which version of dataset to analyze.|
|Distribution Analysis|Histogram + KDE + Q-Q Plot.|
|Statistical Tests|Shapiro-Wilk, Kolmogorov-Smirnov, Anderson-Darling.|
|Skewness Panel|Visual and numeric skewness for all columns.|
|Kurtosis Panel|Measures tailedness; interprets platykurtic vs leptokurtic.|
|Outlier Detection|Uses IQR method; gives upper/lower bounds, values, and percentage.|
|AI Explanation|GPT-generated summaries for kurtosis and skewness.|

---
## 🔍 What Each Technique Tells You

### 🟩 Skewness

| Type    | Interpretation                  | When It Matters                   |
| ------- | ------------------------------- | --------------------------------- |
| **= 0** | Symmetric distribution (Normal) | Good baseline for modeling        |
| **> 0** | Right-skewed (long right tail)  | Log transformation may help       |
| **< 0** | Left-skewed (long left tail)    | Square-root or Box-Cox might help |

---
### 🟪 Kurtosis

| Type    | Interpretation             | When It Matters                      |
| ------- | -------------------------- | ------------------------------------ |
| **≈ 0** | Normal-tailed (mesokurtic) | Safe for most parametric tests       |
| **> 0** | Heavy-tailed (leptokurtic) | Higher chance of outliers            |
| **< 0** | Light-tailed (platykurtic) | More uniform, less prone to extremes |

---
### 🟥 Q-Q Plot

- **Compares quantiles** of sample distribution to a normal distribution.
- **S-shaped curve**: Skewed data.
- **Straight line**: Normal distribution.

---
### 🟨 Statistical Tests for Normality

| Test                   | Description                                                        | When It’s Used                   |
| ---------------------- | ------------------------------------------------------------------ | -------------------------------- |
| **Shapiro-Wilk**       | Most powerful for n < 5000                                         | Small to medium datasets         |
| **Kolmogorov-Smirnov** | Compares empirical vs normal distribution (uses μ and σ from data) | For larger datasets              |
| **Anderson-Darling**   | Strong test across all sizes                                       | Offers critical value comparison |


- Shapiro-Wilk Test: <a href="https://en.wikipedia.org/wiki/Shapiro%E2%80%93Wilk_test" target="_blank" rel="noopener noreferrer">Wikipedia</a>
- Shapiro-Wilk Test: <a href="https://builtin.com/data-science/shapiro-wilk-test" target="_blank" rel="noopener noreferrer">An Introduction to the Shapiro-Wilk Test for Normality</a>
- Kolmogorov-Smirnov: <a href="https://en.wikipedia.org/wiki/Kolmogorov%E2%80%93Smirnov_test" target="_blank" rel="noopener noreferrer">Wikipedia</a>
- Kolmogorov-Smirnov: <a href="https://www.graphpad.com/guides/prism/latest/statistics/interpreting_results_kolmogorov-smirnov_test.htm" target="_blank" rel="noopener noreferrer">Interpreting results: Kolmogorov-Smirnov test</a>
- Anderson-Darling Test: <a href="https://en.wikipedia.org/wiki/Anderson%E2%80%93Darling_test" target="_blank" rel="noopener noreferrer">Wikipedia</a>
- Anderson-Darling Test: <a href="https://www.6sigma.us/six-sigma-in-focus/anderson-darling-normality-test/" target="_blank" rel="noopener noreferrer">A Complete Guide to the Anderson-Darling Normality Test</a>

---
### 🧮 Outlier Detection (IQR Method)

- **IQR = Q3 - Q1**
- **Outliers**:
    - Below: Q1 − 1.5 × IQR
    - Above: Q3 + 1.5 × IQR
- Users can **tune k (IQR multiplier)** to make detection more or less sensitive.

---

### Recommended Reading

- Blog: <a href="https://www.datacamp.com/tutorial/qq-plot" target="_blank" rel="noopener noreferrer">The Q-Q Plot: What It Means and How to Interpret It</a>
- Blog: <a href="https://library.virginia.edu/data/articles/understanding-q-q-plots" target="_blank" rel="noopener noreferrer">Understanding QQ Plots</a>
- Blog: <a href="https://www.sciencedirect.com/topics/earth-and-planetary-sciences/kurtosis" target="_blank" rel="noopener noreferrer">Kurtosis</a>
- Blog: <a href="https://www.itl.nist.gov/div898/handbook/eda/section3/eda35b.htm#:~:text=Kurtosis%20is%20a%20measure%20of,would%20be%20the%20extreme%20case." target="_blank" rel="noopener noreferrer">Measures of Kurtosis and Skewness</a>
- Blog: <a href="https://www.investopedia.com/terms/s/skewness.asp#:~:text=a%20probability%20distribution.-,What%20Is%20Skewness%3F,the%20bell%20curve%20is%20skewed." target="_blank" rel="noopener noreferrer">Right Skewed vs. Left Skewed Distribution</a>
- Blog: <a href="https://www.simplilearn.com/tutorials/statistics-tutorial/skewness-and-kurtosis" target="_blank" rel="noopener noreferrer">The Complete Guide to Skewness and Kurtosis</a>
- Blog: <a href="https://careerfoundry.com/en/blog/data-analytics/what-is-an-outlier/" target="_blank" rel="noopener noreferrer">What Is an Outlier?</a>
- Blog: <a href="https://www.itl.nist.gov/div898/handbook/prc/section1/prc16.htm#:~:text=An%20outlier%20is%20an%20observation,what%20will%20be%20considered%20abnormal." target="_blank" rel="noopener noreferrer">What are outliers in the data?</a>
- Blog: <a href="https://www.coursera.org/articles/what-are-outliers" target="_blank" rel="noopener noreferrer">What Are Outliers in Data Sciences?</a>