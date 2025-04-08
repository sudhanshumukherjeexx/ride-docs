## 📘 RIDE User Manual – Panel 8: **Statistical Tests**

---
### 📊 **Purpose of the Panel**

The **Statistical Tests panel** allows users to run hypothesis tests on their data to determine:

- Differences between groups
- Associations between categorical variables
- Normality of distributions

Users can choose from **6 popular tests** depending on data type, assumptions, and goals.

`Recommended Reading`

- Blog: <a href="https://www.originlab.com/doc/Origin-Help/tTest-TwoSample" target="_blank" rel="noopener noreferrer">Two-Sample T-Test</a>
- Blog: <a href="https://www.jmp.com/en/statistics-knowledge-portal/t-test/two-sample-t-test" target="_blank" rel="noopener noreferrer">The Two-Sample t-Test</a>
- Blog: <a href="https://www.statology.org/two-sample-t-test/" target="_blank" rel="noopener noreferrer">Two Sample t-test: Definition, Formula, and Example</a>
- Blog: <a href="https://www.resonio.com/market-research/analysis-of-variance-anova/" target="_blank" rel="noopener noreferrer">Analysis of Variance (ANOVA) Guide with Examples</a>
- Blog: <a href="https://stattrek.com/tutorials/anova-tutorial" target="_blank" rel="noopener noreferrer">Analysis of Variance Tutorial</a>
- Blog: <a href="https://datatab.net/tutorial/chi-square-test" target="_blank" rel="noopener noreferrer">Chi-Square test</a>
- Blog: <a href="https://www.scribbr.com/statistics/chi-square-tests/" target="_blank" rel="noopener noreferrer">Chi-Square (Χ²) Tests | Types, Formula & Examples</a>
- Blog: <a href="https://www.scribbr.com/statistics/chi-square-test-of-independence/" target="_blank" rel="noopener noreferrer">Chi-Square Test of Independence | Formula, Guide & Examples</a>
- Blog: <a href="https://datatab.net/tutorial/mann-whitney-u-test" target="_blank" rel="noopener noreferrer">Mann-Whitney U-Test</a>
- Blog: <a href="https://www.statstutor.ac.uk/resources/uploaded/mannwhitney.pdf" target="_blank" rel="noopener noreferrer">The Mann-Whitney U Test</a>
- Blog: <a href="https://study.com/skill/learn/how-to-conduct-a-wilcoxon-signed-rank-test-explanation.html" target="_blank" rel="noopener noreferrer">How to Conduct a Wilcoxon Signed Rank Test</a>
- Blog: <a href="https://datatab.net/tutorial/wilcoxon-test" target="_blank" rel="noopener noreferrer">Wilcoxon signed-rank test</a>
- Blog: <a href="https://datatab.net/tutorial/kruskal-wallis-test" target="_blank" rel="noopener noreferrer">Kruskal-Wallis-Test</a>

---
### 🧭 **User Workflow**

1. **Upload Dataset**  
    Choose from:
    - Initial DataFrame
    - Imputed, Encoded, or Scaled DataFrame

2. **Choose a Statistical Test**  
    Options include:
    - 2-Sample T-Test
    - ANOVA
    - Chi-Square Test
    - Mann-Whitney U Test
    - Wilcoxon Signed-Rank Test
    - Kruskal-Wallis Test

3. **Select Group & Value Columns**  
    Based on the test chosen, select a categorical column (for grouping) and a numerical column (for values).
    
4. **Visualize Distributions** _(Optional)_  
    Choose to view histograms, box plots, or group distributions.
    
5. **Run the Test**  
    Get test statistics, p-values, interpretation, and AI-generated summaries if OpenAI API is enabled.

---
### 🧪 Statistical Test Explanations with Formulas & Use Cases

### **1. 2-Sample T-Test**

- **Purpose**: Compares means of two independent groups.
- **Assumptions**: Normal distribution, equal variances.
	- **Formula** $t = \frac{\bar{x}_1 - \bar{x}_2}{\sqrt{\frac{s_1^2}{n_1} + \frac{s_2^2}{n_2}}}$
	- $\bar{x}_1$ and $\bar{x}_2$ are the sample means
	- $s_1^2$ and $s_2^2$ are the sample variances
	- $n_1$ and $n_2$ are the sample sizes
- **Example**: Compare exam scores between two sections of students.

- <a href="https://www.originlab.com/doc/Origin-Help/tTest-TwoSample" target="_blank" rel="noopener noreferrer">Two-Sample T-Test</a>
- <a href="https://www.jmp.com/en/statistics-knowledge-portal/t-test/two-sample-t-test" target="_blank" rel="noopener noreferrer">The Two-Sample t-Test</a>
- <a href="https://www.statology.org/two-sample-t-test/" target="_blank" rel="noopener noreferrer">Two Sample t-test: Definition, Formula, and Example</a>

---
### **2. ANOVA (Analysis of Variance)**

- **Purpose**: Compares means of **3 or more** independent groups.
- **Assumptions**: Normal distribution, equal variances.
- **Formula**:
	- $$F = \frac{\text{Between-group variance}}{\text{Within-group variance}} = \frac{MS_{between}}{MS_{within}}$$
    - The $F$-statistic compares $MS_{between}$ to $MS_{within}$
	- $MS_{between}$ represents the between-group variance
	- $MS_{within}$ represents the within-group variance
- **Example**: Compare customer satisfaction across 4 product lines.

- <a href="https://www.resonio.com/market-research/analysis-of-variance-anova/" target="_blank" rel="noopener noreferrer">Analysis of Variance (ANOVA) Guide with Examples</a>
- <a href="https://stattrek.com/tutorials/anova-tutorial" target="_blank" rel="noopener noreferrer">Analysis of Variance Tutorial</a>
---
### **3. Chi-Square Test**

- **Purpose**: Tests for independence between two categorical variables.
- **Assumptions**: Expected frequencies ≥ 5.
	- **Formula**:
$\chi^2 = \sum \frac{(O - E)^2}{E}$
- where $O$ is observed frequency, $E$ is expected frequency.
- **Example**: Test if gender and preferred drink are related.


- <a href="https://datatab.net/tutorial/chi-square-test" target="_blank" rel="noopener noreferrer">Chi-Square test</a>
- <a href="https://www.scribbr.com/statistics/chi-square-tests/" target="_blank" rel="noopener noreferrer">Chi-Square (Χ²) Tests | Types, Formula & Examples</a>
- <a href="https://www.scribbr.com/statistics/chi-square-test-of-independence/" target="_blank" rel="noopener noreferrer">Chi-Square Test of Independence | Formula, Guide & Examples</a>
---
### **4. Mann-Whitney U Test**

- **Purpose**: Non-parametric alternative to T-test (for non-normal data).
- **Assumptions**: Independent samples, ordinal/numeric values.
- **Formula**:  
$U = n_1 n_2 + \frac{n_1(n_1+1)}{2} - R_1$  
	- where $R_1$ is the sum of ranks in group 1.
- **Example**: Compare ratings of two movies.

- <a href="https://datatab.net/tutorial/mann-whitney-u-test" target="_blank" rel="noopener noreferrer">Mann-Whitney U-Test</a>
- <a href="https://www.statstutor.ac.uk/resources/uploaded/mannwhitney.pdf" target="_blank" rel="noopener noreferrer">The Mann-Whitney U Test</a>
---
### **5. Wilcoxon Signed-Rank Test**

- **Purpose**: Non-parametric test for **paired** data.
- **Assumptions**: Symmetric distribution of differences.
- Formula **Wilcoxon Signed-Rank Test**
$W = \sum_{i=1}^{n} [sgn(x_{2,i} - x_{1,i}) \cdot R_i]$
	- where $R_i$ is the rank of the absolute difference, and $sgn()$ is the sign function.
- **Example**: Compare before/after treatment scores for same patients.

- <a href="https://study.com/skill/learn/how-to-conduct-a-wilcoxon-signed-rank-test-explanation.html" target="_blank" rel="noopener noreferrer">How to Conduct a Wilcoxon Signed Rank Test</a>
- <a href="https://datatab.net/tutorial/wilcoxon-test" target="_blank" rel="noopener noreferrer">Wilcoxon signed-rank test</a>

---
### **6. Kruskal-Wallis H Test**

- **Purpose**: Non-parametric ANOVA (3+ groups, not normally distributed).
- **Kruskal-Wallis H Test**
- **Formula**:
- $$H = \frac{12}{n(n+1)} \sum \frac{R_i^2}{n_i} - 3(n+1)$$
	- where $R_i$ is the sum of ranks in group $i$, $n_i$ is the sample size of group $i$, and $n$ is the total sample size.
- **Example**: Compare time spent on app across multiple age groups.

- <a href="https://datatab.net/tutorial/kruskal-wallis-test" target="_blank" rel="noopener noreferrer">Kruskal-Wallis-Test</a>

---
## 🔍 Summary Table

|Test|Parametric?|Groups|Data Type|Use When|
|---|---|---|---|---|
|**T-Test**|Yes|2|Numeric|Comparing two groups (normal)|
|**ANOVA**|Yes|≥3|Numeric|Comparing ≥3 groups (normal)|
|**Chi-Square**|No|≥2|Categorical|Check relationships|
|**Mann-Whitney U**|No|2|Numeric (Ordinal)|Two groups, not normal|
|**Wilcoxon**|No|Paired|Numeric (Ordinal)|Paired samples, not normal|
|**Kruskal-Wallis**|No|≥3|Numeric (Ordinal)|≥3 groups, not normal|

---

### Recommended Reading

- Blog: <a href="https://www.originlab.com/doc/Origin-Help/tTest-TwoSample" target="_blank" rel="noopener noreferrer">Two-Sample T-Test</a>
- Blog: <a href="https://www.jmp.com/en/statistics-knowledge-portal/t-test/two-sample-t-test" target="_blank" rel="noopener noreferrer">The Two-Sample t-Test</a>
- Blog: <a href="https://www.statology.org/two-sample-t-test/" target="_blank" rel="noopener noreferrer">Two Sample t-test: Definition, Formula, and Example</a>
- Blog: <a href="https://www.resonio.com/market-research/analysis-of-variance-anova/" target="_blank" rel="noopener noreferrer">Analysis of Variance (ANOVA) Guide with Examples</a>
- Blog: <a href="https://stattrek.com/tutorials/anova-tutorial" target="_blank" rel="noopener noreferrer">Analysis of Variance Tutorial</a>
- Blog: <a href="https://datatab.net/tutorial/chi-square-test" target="_blank" rel="noopener noreferrer">Chi-Square test</a>
- Blog: <a href="https://www.scribbr.com/statistics/chi-square-tests/" target="_blank" rel="noopener noreferrer">Chi-Square (Χ²) Tests | Types, Formula & Examples</a>
- Blog: <a href="https://www.scribbr.com/statistics/chi-square-test-of-independence/" target="_blank" rel="noopener noreferrer">Chi-Square Test of Independence | Formula, Guide & Examples</a>
- Blog: <a href="https://datatab.net/tutorial/mann-whitney-u-test" target="_blank" rel="noopener noreferrer">Mann-Whitney U-Test</a>
- Blog: <a href="https://www.statstutor.ac.uk/resources/uploaded/mannwhitney.pdf" target="_blank" rel="noopener noreferrer">The Mann-Whitney U Test</a>
- Blog: <a href="https://study.com/skill/learn/how-to-conduct-a-wilcoxon-signed-rank-test-explanation.html" target="_blank" rel="noopener noreferrer">How to Conduct a Wilcoxon Signed Rank Test</a>
- Blog: <a href="https://datatab.net/tutorial/wilcoxon-test" target="_blank" rel="noopener noreferrer">Wilcoxon signed-rank test</a>
- Blog: <a href="https://datatab.net/tutorial/kruskal-wallis-test" target="_blank" rel="noopener noreferrer">Kruskal-Wallis-Test</a>