# 💧 Tanzanian Water Well Functionality Prediction - Phase Three Data Science Project

## 📁 1. Project Overview

This project focuses on analyzing and modeling the functionality of water wells in **Tanzania**. 
The dataset captures key features related to the **condition, installation, management, and 
geographical attributes** of wells. The goal is to create predictive models that help identify 
non-functional or at-risk wells, supporting **government agencies, NGOs, and water resource managers** 
in better targeting interventions.

The project follows the **CRISP-DM methodology** and leverages **predictive analytics** to 
generate actionable insights that can enhance water accessibility and sustainability across communities.

---

## 🧠 2. Business Understanding

- **Client/Context**: Tanzanian government agencies, NGOs, and water sustainability programs
- **Objective**: Predict the operational status of water wells to improve maintenance planning, 
  reduce downtime, and allocate resources effectively
- **Problem Statement**: A large percentage of wells in Tanzania are non-functional, leading to 
  wasted investments and water scarcity for communities
- **Metrics of Success**:
  - Achieve high **accuracy, recall, and F1-score** in predicting well functionality
  - Identify the **top contributing factors** affecting well sustainability
  - Provide clear **recommendations** for prioritizing repairs and installations

---

## 📊 3. Data Understanding

- **Source**: [Tanzania Water Wells Dataset (Taarifa / DrivenData)](https://www.drivendata.org/competitions/7/pump-it-up-data-mining-the-water-table/)
- **Description**:
  - The dataset contains ~59,000 records of water wells across Tanzania
  - Features include `funder`, `installer`, `gps_height`, `population`, `construction_year`, 
    `water_quality`, `quantity`, `source_type`, `management`, `payment`, `region`, and more
  - Target variable: `status_group` (functional, non-functional, functional needs repair)

---

## 🧹 4. Data Cleaning and Preparation

- Imputed missing values for key categorical and numerical columns
- Bucketed funders and installers to reduce high cardinality issues
- Converted date fields to appropriate datetime formats
- Engineered new features such as:
  - `age_years` = Current year – `construction_year`
  - Log transformations on skewed variables (`amount_tsh`, `population`)
- Removed duplicates and obvious data entry errors
- Encoded categorical variables using one-hot encoding

**Key Fields Used**:  
`funder`, `installer`, `gps_height`, `population`, `amount_tsh`, `age_years`, `region`, 
`water_quality`, `extraction_type`, `management`, `payment`, `source_type`, `status_group`

---

## 🧪 5. Methodology: CRISP-DM

1. **Business Understanding**: Define objectives (predict well functionality, allocate resources)
2. **Data Understanding**: Explore data distribution, missing values, and correlations
3. **Data Preparation**: Cleaning, feature engineering, encoding
4. **EDA**:
   - Univariate, bivariate, and multivariate analysis
   - Geographic distribution of well functionality
   - Relationships between funder/installer and failure rates
5. **Modeling**:
   - Logistic Regression, Random Forest, XGBoost
   - Hyperparameter tuning with GridSearchCV
6. **Evaluation**:
   - Performance measured with Accuracy, Precision, Recall, F1-score, ROC-AUC
   - Confusion matrices to evaluate misclassifications

---

## 📈 6. Visualizations

- Distribution of well status across regions
- Population served vs. functionality
- Top funders/installers and their respective failure rates
- Feature importance plots from Random Forest / XGBoost
- Geospatial heatmaps of non-functional wells

> Visuals are included in the Jupyter Notebook and Presentation Deck.

---

## 📊 7. Key Findings

- **High failure rates** are associated with wells installed by lesser-known funders/contractors
- **Population and gps_height** significantly influence well sustainability
- Wells with **unreliable water quality and low quantity** are more likely to be non-functional
- **Payment and management structures** strongly correlate with operational success
- **Older wells** (constructed >20 years ago) have higher non-functionality rates

---

## 💡 8. Prescriptive Recommendations

1. **Prioritize repairs** for wells in high-population areas to maximize impact
2. **Focus on funder/installer quality control** by investing in top-performing organizations
3. **Promote sustainable management models** with community contributions for maintenance
4. Use predictive modeling to **pre-emptively flag at-risk wells** before breakdown
5. Encourage replacement/rehabilitation of **aging infrastructure**

---

## 📦 9. Deliverables

- ✅ **Jupyter Notebook** with EDA, feature engineering, and model building
- ✅ **Cleaned dataset** for analysis
- ✅ **Presentation slides** for stakeholders
- ✅ **README.md** (this file)

---

## 📎 10. Repository Structure

```bash
tanzania-water-well-analysis/
│
├── data/
│   ├── raw/                  # Original dataset
│   └── processed/            # Cleaned and engineered dataset
│
├── notebooks/
│   └── Tanzanian_Water_Well_Modeling.ipynb # Main notebook
│
├── presentation/
│   └── presentation.pdf      # Stakeholder presentation
│
├── models/
│   └── best_model.pkl        # Saved trained model
│
├── README.md
├── .gitignore
```

---

## 🛠 11. Tools & Technologies

- Python (Pandas, NumPy, Matplotlib, Seaborn)
- Scikit-learn, XGBoost
- Jupyter Notebook
- CRISP-DM methodology

---

## 👤 12. Author

**Huldah Chepkoech Rotich**  
Data Science Student | Moringa School  
*This project is part of Phase 3 Presentation for Moringa’s Data Science Program.*

---

## 📬 Contact

For feedback or questions, please email: rotichhuldah@gmail.com  
Or connect via [LinkedIn](https://www.linkedin.com/in/huldah-rotich-339797181/)

---

## 📝 License

This project is for educational purposes and not intended for production-grade use or regulatory decision-making.
