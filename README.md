# **Predicting Problematic Internet Usage in Children and Adolescents**  
**University of Tartu | Intro to Data Science Course Project | A3**  

---

## **Project Overview**  
This project was conducted as part of the **Intro to Data Science** course at the **University of Tartu, Institute of Computer Science**.  

**Author**:  
- **Ahmed Wael**  

**Goal**: To analyze and predict problematic internet usage severity (measured by the **Severity Impairment Index (SII)**) among children and adolescents, using physical, demographic, and behavioral data.  

---

## **Motivation**  
Problematic internet use is a growing concern, particularly among children and adolescents, as it is linked to:  
- **Mental health issues**: depression, anxiety, and declining emotional well-being.  
- **Physical consequences**: reduced activity, poor posture, and unhealthy habits.  

This project aims to leverage **accessible physical activity and behavioral data** to:  
- Understand the behaviors associated with problematic internet use.  
- Predict SII severity for early intervention.  

---

## **Repository Contents**  
This repository is organized into the following structure:  

```plaintext
📁 Prediction-of-Internet-Use-Kaggle-Competition/
│-- data/
│   ├── train.csv                # Training dataset
│   ├── test.csv                 # Test dataset
│-- notebooks/
│   ├── HMS_Data_Visualization.ipynb       # Detailed data visualization
│   ├── complete-eda-ml-model.ipynb        # EDA and model training pipeline
│   ├── complete-eda-and-visualization-for-csv-files.ipynb   # EDA for CSV datasets
│-- results/
│   ├── plots/                   # All generated visualizations
│-- README.md                    # Project documentation (this file)
│-- requirements.txt             # Required Python libraries
│-- LICENSE                      # License information
```

---

## **How to Reproduce the Analysis**  

### 1. Clone the Repository  
```bash
git clone https://github.com/ahmedwael19/Prediction-of-Internet-Use-Kaggle-Compeititon.git
cd Prediction-of-Internet-Use-Kaggle-Competition
```

### 2. Set Up the Environment  
Install the necessary libraries using `requirements.txt`:  
```bash
pip install -r requirements.txt
```

### 3. Data Preparation  
Ensure the datasets (`train.csv` and `test.csv`) are placed in the `data/` folder.  

### 4. Run the Notebooks  
The analysis and modeling pipeline is split into three main notebooks:  
1. **`HMS_Data_Visualization.ipynb`**: Detailed exploration and visualization of the data.  
2. **`complete-eda-ml-model.ipynb`**: Full EDA, preprocessing, feature engineering, and machine learning pipeline.  
3. **`complete-eda-and-visualization-for-csv-files.ipynb`**: Focused EDA on raw CSV data.  

Execute each notebook in order to reproduce the results. Outputs (plots, results, etc.) will be saved in the `results/` folder.  

---

## **Project Highlights**  

- **Data Cleaning and Preprocessing**:  
  - Fixed **missing values** and recalculated ambiguous SII scores.  
  - Corrected errors in BMI and handled outliers using the **IQR method**.  
  - Removed highly correlated features (>90%) using **hierarchical clustering**.  

- **Key Insights from EDA**:  
  - Older adolescents (\textbf{14–17 years}) show the highest SII severity.  
  - Mental health scores (CGAS) decline with increasing SII severity.  
  - Younger children display addiction-like behaviors even when restricted from internet use.  
  - Internet preoccupation and frustration correlate strongly with SII levels.  

- **Modeling Approach**:  
  - Separate models were trained for **children** and **teens** to account for age-specific patterns.  
  - Combined predictions from both models to optimize performance.  
  - The best model achieved a **Quadratic Weighted Kappa (QWK)** score of 0.347  

- **Visualizations**:  
  - Correlation heatmaps for children and teens.  
  - Detailed plots illustrating age groups, internet usage hours, and SII severity.  

---

## **Results**  
- Final visualizations and analysis outputs are saved in the **`results/plots`** folder.  

---

## **Tools and Libraries**  
- **Python 3.8+**  
- **Pandas**, **NumPy**  
- **Matplotlib**, **Seaborn**  
- **Scikit-learn**  
- **TPOT**, **H2O**, **Hyperopt**  

---

## **Acknowledgments**
Thanks to my ML project teammates **Anton Vykhovanets** and **Andres Sebastian** @pinkfloydsito for their contributions and support.  
Data provided by the **Healthy Brain Network** in collaboration with the **Child Mind Institute** and Kaggle.
This project was completed as part of the **Intro to Data Science course** at the **University of Tartu**, **Institute of Computer Science**.

---

## **License**  
This project is licensed under the MIT License.  
