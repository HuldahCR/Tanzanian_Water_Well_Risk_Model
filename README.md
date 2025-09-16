\# 💧 Tanzanian Water Wells Functionality Prediction  



\## 📌 Project Overview  

Access to clean and safe water is critical for rural Tanzanian communities. Yet, many water wells fail or require frequent repairs, leaving thousands without reliable access.  



This project applies \*\*machine learning\*\* to predict the functionality of water wells, enabling NGOs, government agencies, and donors to \*\*prioritize repairs and allocate resources efficiently\*\*.  



The task is a \*\*multi-class classification problem\*\*:  

\- \*\*Functional\*\*  

\- \*\*Functional Needs Repair\*\*  

\- \*\*Non Functional\*\*



---



\## 🎯 Objectives  

\- ✅ Predict the functionality status of Tanzanian water wells.  

\- ✅ Identify geospatial and operational patterns of well failure.  

\- ✅ Provide interpretable feature importance to guide decision-making.  

\- ✅ Support proactive maintenance to \*\*reduce costs by ~20%\*\* and ensure reliable access.  



---



\## 📂 Dataset  

Data provided by \*\*Taarifa + Tanzanian Ministry of Water\*\*, covering ~59,400 wells.  



\- \*\*Features\*\*: geospatial (longitude, latitude, gps\_height), operational (funder, installer, management, payment), and technical details (pump type, water source).  

\- \*\*Target\*\*: `status\_group` (Functional / Needs Repair / Non Functional).  

\- Data split into:  

&nbsp; - \*\*Train set\*\* (with labels)  

&nbsp; - \*\*Test set\*\* (unlabeled, used for predictions)  



---



\## 🛠️ Methodology  



We used the \*\*CRISP-DM Framework\*\*:  



1\. \*\*Business Understanding\*\* – Address water scarcity \& infrastructure reliability.  

2\. \*\*Data Understanding\*\* – Explore geospatial and operational drivers of well failure.  

3\. \*\*Data Preparation\*\* – Cleaning, imputation, one-hot encoding, feature engineering (e.g., `population\_log`, `amount\_tsh\_log`, `age\_years`).  

4\. \*\*Modeling\*\* – Tested multiple models:  

&nbsp;  - Logistic Regression (baseline)  

&nbsp;  - Random Forest  

&nbsp;  - Gradient Boosting Classifier  

&nbsp;  - Support Vector Machine (SVM)  

&nbsp;  - \*\*XGBoost (final choice)\*\*  

5\. \*\*Evaluation\*\* – Accuracy, Precision, Recall, F1-score, and ROC-AUC.  

6\. \*\*Deployment Preparation\*\* – Predictions generated for the unlabeled test dataset.  



---



\## 📊 Results \& Insights  



\### ✅ Best Model: \*\*Tuned XGBoost with Threshold Adjustment\*\*  

\- \*\*Validation Accuracy\*\*: ~74%  

\- \*\*Macro F1-Score\*\*: 0.66  

\- \*\*ROC-AUC (macro)\*\*: 0.883  



\### 🔑 Key Findings  

\- \*\*Most Important Features\*\*:  

&nbsp; - Waterpoint type  

&nbsp; - Quantity group (enough / insufficient / seasonal)  

&nbsp; - Funder \& Installer (accountability effect)  

&nbsp; - Region zone \& basin (geospatial risks)  

&nbsp; - GPS height (elevation effects)  

\- \*\*Geospatial clustering\*\* shows high failure rates in regions like \*\*Dodoma, Tabora, and Singida\*\*.  

\- \*\*Threshold tuning\*\* reduced \*\*false positives\*\*, ensuring fewer failing wells are misclassified as functional.  



---



\## 💡 Business Recommendations  



1\. \*\*Preventive Maintenance\*\*  

&nbsp;  - Prioritize wells predicted as \*“Needs Repair”\* to avoid costly breakdowns.  



2\. \*\*Target High-Risk Regions\*\*  

&nbsp;  - Deploy regional maintenance teams where non-functionality is clustered.  



3\. \*\*Strengthen Management\*\*  

&nbsp;  - Support and monitor local funders/installers with higher failure rates.  



4\. \*\*Resource Allocation\*\*  

&nbsp;  - Drill new wells in \*\*overburdened areas\*\* where population per well is unsustainable.  



5\. \*\*Policy Integration\*\*  

&nbsp;  - Use predictions with \*\*GIS dashboards\*\* to guide donor investments and government planning.  



---



\## ⚠️ Limitations  

\- \*\*Data Imbalance\*\* → “Needs Repair” wells underrepresented.  

\- \*\*Data Quality\*\* → Some funder/installer names remain noisy.  

\- \*\*Temporal Drift\*\* → Future changes (climate, infrastructure) may reduce model reliability.  



---



\## 🔮 Next Steps  

\- 🎯 \*\*Hyperparameter Tuning\*\* → further refine model performance.  

\- 🎯 \*\*Cost-Sensitive Learning\*\* → penalize misclassification of non-functional wells.  

\- 🎯 \*\*Geospatial Visualization Dashboard\*\* → map high-risk wells for NGOs and governments.  

\- 🎯 \*\*Deployment\*\* → package the final model into an interactive tool.  



---



\## 📦 Repository Structure  



