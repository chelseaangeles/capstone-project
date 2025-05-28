# TEECE 2 Capstone Project

## Lifestyle and Learning – Predicting Student Performance

This project explores how student lifestyle habits and mental health status influence academic performance. Using a simulated dataset of 1,000 student records, it combines data analysis and machine learning to uncover patterns and build predictive models.

---

### Research Question

**How does mental health status influence the relationship between lifestyle habits and academic performance?**

---

### Project Overview

The dataset includes variables like:

- **Study Hours**
- **Atendance**
- **Sleep Patterns**
- **Part Time Job**
- **Screen Time**
- **Diet**
- **Exercise Frequency**
- **Mental Health**
- **Final Exam Score**

These features are analyzed to understand their individual and combined impact on student performance. The project includes data preprocessing, visualization, clustering, regression modeling, and optional classification.

---

### Objectives

- Explore the interaction between mental health, lifestyle, and academic results.
- Discover student groupings using clustering techniques.
- Build models to predict final exam scores based on lifestyle and mental health data.
- Optionally, classify students into performance levels.
- Derive practical insights and recommendations for students.

---

### Tools & Technologies

- **Python**
- **Jupyter Notebook**
- **Pandas, NumPy, Matplotlib, Seaborn**
- **Scikit-learn**
- **K-Means Clustering**
- **Linear, Decision Tree & Random Forest Regression**
- **Classification Models (Optional)**

## Key Methods

### 1. **Data Preprocessing**
- Handled missing values
- Encoded categorical variables
- Scaled numeric features
- Engineered new features (e.g., combined screen time)

### 2. **Exploratory Data Analysis**
- Visualized distributions, relationships, and correlations
- Compared mental health and lifestyle impacts on scores

### 3. **Clustering**
- Used K-Means on lifestyle and mental health features
- Identified distinct student profiles

### 4. **Regression**
- Trained Linear, Decision Tree, and Random Forest models
- Evaluated with MAE, RMSE, R², and cross-validation

### 5. **(Optional) Classification**
- Categorized scores into Low, Average, High
- Trained classification models and evaluated them

---

## Insights

Feature Importance:
- For tree-based models, plot and analyze feature importance
- For linear models, interpret coefficients
- Identify the top 3–5 features that most affect performance

### Tree-based models (Decision Tree and Random Forest Regressors)

Based on the Decision Tree and Random Forest regressors we trained earlier, the most significant lifestyle features affecting student performance were identified through the calculated feature importance scores. The analysis consistently highlights that:

- **Study Hours per Day** emerged as the most influential predictor, positively associated with higher exam scores.
- **Mental Health Rating** was another critical predictor, indicating that better mental health conditions strongly support improved academic performance.
- **Attendance Percentage** also appeared significant, reinforcing the importance of regular class attendance in achieving higher scores.
- **Sleep Hours** showed a notable impact, underscoring adequate rest as essential for optimal academic outcomes.
- **Total Screen Time** negatively correlated with academic performance, indicating that excessive screen usage detracts from academic success.

### Linear Regression Model

The coefficients derived from our Linear Regression model revealed similar insights. Positive coefficients confirmed that increases in Study Hours per Day, Attendance Percentage, and Mental Health Rating are directly associated with higher exam scores. Conversely, negative coefficients for features like Total Screen Time emphasized their detrimental effect on academic performance.

### Classification Task (Decision Tree Classifier and Logistic Regression)

The classification task further validated these findings. The trained Decision Tree Classifier indicated that Study Hours per Day, Mental Health Rating, and Attendance Percentage were primary factors distinguishing students in the "High," "Average," and "Low" performance categories. Similarly, Logistic Regression coefficients reinforced these findings, consistently identifying these features as major determinants of academic success.

### Summary

The cumulative analysis of regression and classification models consistently pinpointed the following as the most impactful lifestyle features:

- **Study Hours per Day**
- **Mental Health Rating**
- **Attendance Percentage**
- **Sleep Hours**
- **Total Screen Time**

---

Cluster Profiling
- For each cluster:
  - Describe common behaviors (e.g., “Cluster 1 sleeps less, studies more”)
  - Associate average exam scores with each group
  - Comment on trends you observe (e.g., does screen time correlate with lower scores?)

### Cluster Analysis Report – Student Lifestyle and Performance

**Objective**

To explore how lifestyle habits and mental health relate to academic performance using K-Means clustering. Two models were evaluated using **K = 3** and **K = 4** cluster groups based on features like study time, screen time, sleep, attendance, and mental health.

---

***Clustering Summary***

| K | Clusters | Purpose |
|---|----------|---------|
| 3 | Broader lifestyle groupings | Quick insights with minimal segmentation |
| 4 | Finer differentiation | Deeper behavioral profiling |

---

### K = 3 Cluster Analysis

***Cluster Descriptions***

| Cluster | Key Behaviors | Attendance (%) | Mental Health | Exam Score | Interpretation |
|--------|----------------|----------------|----------------|-------------|----------------|
| **0** | Moderate sleep, average screen time, low attendance | 71.6 | 5.55 | **67.67** | Possibly disengaged or inconsistent performers |
| **1** | High study hours, **highest attendance**, **highest screen time** | 95.3 | 5.48 | **71.55** | **Top performers** – strong academic discipline offsets distractions |
| **2** | Balanced habits, **least sleep**, low mental health | 83.7 | 5.36 | **69.39** | Healthy intentions, but **stress or fatigue may limit outcomes** |

***Trends Observed (K = 3)***

- **Attendance** is the most consistent predictor of academic success.
- **High screen time** doesn't always mean poor performance when paired with strong study habits.
- **Mental health** plays a moderating role, especially in Cluster 2.

---

### K = 4 Cluster Analysis

***Cluster Descriptions***

| Cluster | Key Behaviors | Attendance (%) | Mental Health | Exam Score | Interpretation |
|--------|----------------|----------------|----------------|-------------|----------------|
| **0** | Moderate habits, lowest mental health | 79.8 | **5.26** | **67.85** | Lower scores may be linked to emotional strain |
| **1** | **Highest study time and attendance**, highest screen time | **97.3** | 5.37 | **72.03** | **High achievers** – academically driven |
| **2** | Best sleep, best mental health, balanced habits | 88.0 | **5.60** | **70.70** | **Well-rounded performers** |
| **3** | Healthy lifestyle, **lowest attendance** | 69.1 | 5.59 | **68.10** | **High potential, underperforming** due to disengagement |

***Trends Observed (K = 4)***

- **Mental health** was highest in Cluster 2 and second highest in Cluster 3, both with good lifestyle habits.
- **Cluster 1 succeeded despite highest screen time** — showing that academic consistency matters more than screen habits.
- **Cluster 3 underperformed** mainly due to **poor class attendance**, not poor health or habits.

---

### Key Insights

- **Attendance is the strongest predictor of academic performance** across both models.
- **Good habits alone are not enough** — they must be paired with consistent engagement.
- **Mental health enhances** the benefits of good lifestyle habits, especially in well-balanced clusters.
- Screen time **is not inherently harmful** if the student has strong academic routines.

---

### Summary

Both K = 3 and K = 4 offer valuable behavioral insights:
- Use **K = 3** for a quick overview.
- Use **K = 4** for detailed profiling, especially in interventions or targeted support.

This clustering supports educators and advisors in identifying which student groups may benefit most from academic or mental health support.

---

Model Performance
- Which model performed best? Why?
- Are there trade-offs between interpretability and accuracy?

### Which model performed best? Why?
  - Linear Regression performed best because the relationship between lifestyle factors (like study hours, sleep, and screen time) and exam scores was mostly linear, which means changes in these habits led to consistent changes in performance. The model accurately captured these patterns without overfitting due to clean data preprocessing and well-chosen features. Its simplicity made it both effective and easy to interpret compared with other models.

### Are there trade-offs between interpretability and accuracy?
  - Linear regression is highly interpretable as it clearly shows how each lifestyle factor impacts exam scores, but more complex models like random forest or decision tree may offer slightly better accuracy by capturing non-linear relationships. However, these models are harder to interpret, especially when understanding the specific influence of each feature. Hence, while complex models may improve predictive performance, they sacrifice the transparency that linear regression provides.

---

Real-World Implications
- What advice could you give students based on your findings?
- Are there surprising or counterintuitive results?

### What advice could you give students based on your findings?
  - Based on the findings, those students with high study hours, and attends classes frequently performs well in exams. Therefore, spending more time in studying and attending classes regularly can affect exam scores positively.

### Are there surprising or counterintuitive results?
  - Based on the clustering, screen time doesn't have any affect on exam scores. It showed that some students with high screen time hours, also have high exam scores which is a surprise since it is expected that students who spend more time on their electronic gadgets to have low scores as it can be a distraction to studying. However, based on regression, it is negatively correlated with academic performance, indicating that excessive screen usage detracts from academic success.

---

## Presentation

Youtube Video Link: [TEECE 2 Capstone Project](https://www.youtube.com/)

A 10-minute recorded video includes:
- Overview of the research question and goals
- Key analysis steps and results
- Visualizations and modeling insights
- Final takeaways and practical advice

---

## License

This project is for academic and educational purposes only.

---

## Author/s

- **Name:** *Chelsea R. Angeles | Adelyn Joyce S. Soriano | Rychard Andrei Reyes*
- **University:** *Technological University of the Philippines*

---

## References

- Dataset Source: [Student Habits Dataset](https://docs.google.com/spreadsheets/d/1qXURK359eUjom2M7R8Zh2XALFt3EuS1s/edit?rtpof=true&gid=744158941#gid=744158941)


