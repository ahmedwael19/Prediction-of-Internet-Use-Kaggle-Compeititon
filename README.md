# Prediction-of-Internet-Use-Kaggle-Compeititon (A3)
Project A3: Prediction of Internet Use
Here’s a **well-structured README** for your project repository on GitHub, ensuring clarity and engagement for readers.

---

# **Predicting Problematic Internet Usage in Children and Adolescents**
**Kaggle Competition | Severity Impairment Index (SII)**

---

## **Project Overview**
This project was conducted as part of the Intro to Data Science course at the University of Tartu, Institute of Computer Science. The goal is to analyze and predict the level of problematic internet usage among children and adolescents using physical, demographic, and behavioral data.

The target variable, **Severity Impairment Index (SII),** is derived from a 20-question survey that measures internet addiction severity.

This repository covers the full data science pipeline, from **Exploratory Data Analysis (EDA)** to advanced **Machine Learning modeling** with **AutoML** tools.



---

## **Dataset**
- **Source**: Kaggle competition: [Child Mind Institute - Problematic Internet Use](https://www.kaggle.com/competitions/child-mind-institute-problematic-internet-use/)
- **Records**: 3,960 samples
- **Features**: 82 columns, including:
  - **Demographics**: Age, sex, enrollment season  
  - **Internet Usage**: Daily hours spent online  
  - **Physical Measures**: BMI, endurance scores, heart rate  
  - **Behavioral Data**: SII derived from survey responses  

### Dataset Challenges
1. **Ambiguous zeros in SII**: Representing valid "no impairment" and missing values.  
2. **Inconsistent calculations**: Errors in survey-derived scores.  

### Fix:
- Recalculated **SII values** from raw survey responses.  
- Performed **informed imputation** for missing SII data.  

---

## **Project Goals**
1. **Understand Patterns**: Analyze relationships between physical activity, mental health, and internet addiction.  
2. **Build Predictive Models**: Train models to predict SII levels using behavioral and physical activity data.  
3. **Achieve Competitive Results**: Rank in the top 15% of the Kaggle competition leaderboard.  

---

## **Data Science Pipeline**
1. **Data Cleaning and Feature Engineering**  
   - Recalculated SII scores and fixed missing data.  
   - Corrected BMI errors using height and weight.  
   - Removed highly correlated features using **Hierarchical Clustering**.

2. **Exploratory Data Analysis (EDA)**  
   Key questions addressed:
   - Do older children exhibit higher addiction levels?
   - How do mental health scores vary with SII severity?
   - Do younger children exhibit addiction-like behaviors when restricted from internet use?  
   - Which features correlate most with SII and internet hours?

3. **Model Training**  
   - Built separate models for **Children (5–14 years)** and **Teens (15–22 years)**.  
   - Combined predictions for the final results.  
   - Automated Hyperparameter Tuning using:  
     - **Hyperopt**  
     - **TPOT**  
     - **H2O AutoML**  

   **Metric Used**: Quadratic Weighted Kappa (QWK)

4. **Evaluation**  
   - Achieved a QWK score of **0.347** on the public leaderboard.  
   - Positioned at **2312 out of 3180** (continuously improving).  


---

## **Key Results**
- Older adolescents (\textbf{14–17 years}) have the highest SII levels.  
- Teens spending **3+ hours/day** online exhibit severe problematic internet use.  
- **BMI** and internet usage hours are positively correlated with SII.  
- Mental health scores (\textbf{CGAS}) decline significantly with SII severity.

---

## **Tools and Libraries**
- **Python** (3.8+)
- **Pandas**, **NumPy**
- **Matplotlib**, **Seaborn**
- **Scikit-learn**  
- **TPOT**, **Hyperopt**, **H2O AutoML**  

## **Acknowledgments**
Special thanks to my ML project teammates **Anton Vykhovanets** and **Andres Sebastian** for their contributions and support.  
Data provided by the **Healthy Brain Network** in collaboration with the **Child Mind Institute** and Kaggle.
This project was completed as part of the **Intro to Data Science course** at the **University of Tartu**, **Institute of Computer Science**.

---

## **License**
This project is licensed under the MIT License.  
