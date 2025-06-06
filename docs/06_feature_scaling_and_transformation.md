## 📘 RIDE User Manual – Panel 6: **Feature Scaling & Transformation**

---
### 📊 **Purpose of the Panel**

This panel allows users to **normalize, standardize, or transform features** for better performance in machine learning models. Proper scaling and transformation:

- Makes algorithms converge faster.
- Prevents features with larger magnitudes from dominating the model.
- Handles skewness and non-normal distributions.

`Recommended Reading`

- Blog: <a href="https://www.atoti.io/articles/when-to-perform-a-feature-scaling/#:~:text=What%20is%20Feature%20Scaling%3F,during%20the%20data%20preprocessing%20step." target="_blank" rel="noopener noreferrer">When to perform scaling</a>
- Blog: <a href="https://sebastianraschka.com/Articles/2014_about_feature_scaling.html#:~:text=shouldn't%20hurt.-,About%20Min%2DMax%20scaling,range%20%2D%20usually%200%20to%201." target="_blank" rel="noopener noreferrer">About Feature Scaling and Normalization</a>
- Blog: <a href="https://www.analyticsvidhya.com/blog/2020/04/feature-scaling-machine-learning-normalization-standardization/" target="_blank" rel="noopener noreferrer">Feature Scaling: Engineering, Normalization, and Standardization</a>
- Blog: <a href="https://medium.com/@datasciencejourney100_83560/feature-transformation-part-of-feature-engineering-dff2deaf59a2" target="_blank" rel="noopener noreferrer">Feature Transformation- Part of Feature Engineering</a>
- Kaggle Notebook: <a href="https://www.kaggle.com/code/nargisbegum82/all-about-feature-transformation" target="_blank" rel="noopener noreferrer">All about Feature Transformation</a>


---
### 🧭 **User Workflow**

1. **Upload Dataset**  
    Choose from:
    - Initial DataFrame
    - After Missing Value Imputation
    - After Feature Encoding

2. **Select Scaling or Transformation Method**  
    Choose from 8 methods split into two categories:    
    - **Feature Scaling**
    - **Feature Transformation**

3. **Choose Features to Scale**  
    Select one or more numeric columns.

4. **View Results**  
    - Preview scaled data
    - See summary stats before and after scaling
    - Compare original vs transformed distributions

5. **Download Scaled Data**  
    Download the transformed dataset for modeling.

---
### 💻 Features Breakdown

| Feature                   | Description                                                        |
| ------------------------- | ------------------------------------------------------------------ |
| Source Selector           | Choose between raw, imputed, or encoded datasets.                  |
| Scaling Method Selector   | Includes both scaling and transformation strategies.               |
| Numeric Column Detection  | Uses utility to auto-select numeric features.                      |
| Before/After Summary      | Side-by-side stats before and after scaling.                       |
| Distribution Comparison   | Interactive histogram to compare original vs scaled distributions. |
| Download Transformed Data | Exports the result as a CSV.                                       |

---
## 🔧 Scaling & Transformation Methods

### 📏 Feature Scaling

| Method                        | Description                           | Best For                                                   |
| ----------------------------- | ------------------------------------- | ---------------------------------------------------------- |
| **Min-Max Scaling**           | Rescales values to [0, 1] range.      | When bounded input is required (e.g., image pixel values). |
| **Standardization (Z-score)** | Centers data with μ=0 and σ=1.        | When data needs normalization for gradient-based models.   |
| **Robust Scaler**             | Uses IQR (Q3 - Q1), ignores outliers. | When outliers are present and shouldn't dominate scaling.  |
| **Max AbsScaler**             | Scales by max absolute value.         | When dealing with **sparse** data (e.g., TF-IDF).          |

- Min-Max Scaling: <a href="https://medium.com/@iamkamleshrangi/how-min-max-scaler-works-9fbebb9347da" target="_blank" rel="noopener noreferrer">How Min-Max Scaler Works</a>
- Standardization(z-score): <a href="https://datatab.net/tutorial/z-score" target="_blank" rel="noopener noreferrer">z-Score</a>
- Robust Scaling: <a href="https://proclusacademy.com/blog/robust-scaler-outliers/" target="_blank" rel="noopener noreferrer">Robust Scaling: Why and How to Use It to Handle Outliers</a>
- Max AbsScaler: <a href="https://www.youtube.com/watch?v=RbFkTonj1lg" target="_blank" rel="noopener noreferrer">Using Max Abs Scaler for feature scaling | Machine Learning</a>

### 🔄 Feature Transformation

|Method|Description|Best For|
|---|---|---|
|**Quantile Transformer**|Converts feature to a uniform distribution.|When feature values are heavily skewed.|
|**Log Transformer**|Applies `log(1 + x)`.|Right-skewed distributions (e.g., income, prices).|
|**Power Transformer (Box-Cox)**|Normalizes data using λ parameter.|Positive-only data with non-normal shape.|
|**Power Transformer (Yeo-Johnson)**|Modified Box-Cox, supports negatives.|Mixed-sign numeric data needing normalization.|

- Quantile Transformer, Power Transformer and Log Transform: <a href="https://medium.com/data-science/5-data-transformers-to-know-from-scikit-learn-612bc48b8c89#:~:text=Quantile%20Transformer,Gaussian%20Distribution%20(Normal%20Distribution)" target="_blank" rel="noopener noreferrer">5 Data Transformers to know from Scikit-Learn</a> 

---
## 🧠 Why This Panel Matters

- Scaling ensures model **convergence** and **fair weight distribution**.
- Transformation can reduce **skewness** and make data more **Gaussian**, which is preferred by many statistical and ML models.

--- 

### Recommended Reading

- Blog: <a href="https://www.atoti.io/articles/when-to-perform-a-feature-scaling/#:~:text=What%20is%20Feature%20Scaling%3F,during%20the%20data%20preprocessing%20step." target="_blank" rel="noopener noreferrer">When to perform scaling</a>
- Blog: <a href="https://sebastianraschka.com/Articles/2014_about_feature_scaling.html#:~:text=shouldn't%20hurt.-,About%20Min%2DMax%20scaling,range%20%2D%20usually%200%20to%201." target="_blank" rel="noopener noreferrer">About Feature Scaling and Normalization</a>
- Blog: <a href="https://www.analyticsvidhya.com/blog/2020/04/feature-scaling-machine-learning-normalization-standardization/" target="_blank" rel="noopener noreferrer">Feature Scaling: Engineering, Normalization, and Standardization</a>
- Blog: <a href="https://medium.com/@datasciencejourney100_83560/feature-transformation-part-of-feature-engineering-dff2deaf59a2" target="_blank" rel="noopener noreferrer">Feature Transformation- Part of Feature Engineering</a>
- Kaggle Notebook: <a href="https://www.kaggle.com/code/nargisbegum82/all-about-feature-transformation" target="_blank" rel="noopener noreferrer">All about Feature Transformation</a>