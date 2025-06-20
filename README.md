---

## 📊 Dataset
- This dataset is obtained from Kaggle: [Heart Failure Prediction Dataset](https://www.kaggle.com/datasets/fedesoriano/heart-failure-prediction)

## 🧠 Context
- The dataset contains 11 features that can be used to predict the presence of heart disease.  
- A machine learning model was trained to assist with diagnosing this disease.

## 📈 Results
- Random Forest has highest accuracy

| 🧪 Model          | 🏋️ Train Accuracy | 🧾 Test Accuracy |
|-------------------|-------------------|------------------|
| 🔹 KNN             | 88.5%             | 87.2%            |
| 🌳 Decision Tree   | 85.42%            | 84.24%           |
| 🌲 Random Forest   | 92.92%            | 89.13%           |
| ⚡ XGBoost          | 96.73%            | 85.33%           |
| 🧠 Neural Network  | 87.46%            | 85.3%            |

## 🛠️ Work Done
- Built on Andrew Ng’s ML Specialization course, which compares Decision Trees, Random Forest, and XGBoost.  
- Extended the comparison by adding Neural Networks and KNN and tried to outperfrome Random Forest.  
- Notably, **KNN** achieved the **second-highest test accuracy**, highlighting the power of simple, well-preprocessed models.

> #### ⚠️ Note  
> All models performed similarly (only a **3–4%** test accuracy spread). The reasons below reflect my interpretation of each model's strengths in this context.

### 🔍 Reasons for Random Forest outperforming others:
1. **⚡ XGBoost**  
   - Highest training accuracy but lower test accuracy → suggests **overfitting** on ~700 samples. As data is small we no need this big model
2. **🌳 Decision Tree**  
   - Single-tree models often **overfit** or **underfit**, compared to ensemble methods like XGBoost or Random forest.  
3. **🔹 KNN**  
   - Achieved **87.2%** test accuracy (2nd best), indicating a well-scaled feature space favorable for proximity-based learning.  
4. **🧠 Neural Networks**  
   - Typically need **larger datasets**; with only ~700 samples, they risk **overfitting** or **underfitting** despite tuning.

## 🧾 Attribute Information
- **🧓 Age**: Age of the patient [years]  
- **🚻 Sex**: Sex of the patient [M: Male, F: Female]  
- **❤️ ChestPainType**: Chest pain type [TA, ATA, NAP, ASY]  
- **🩺 RestingBP**: Resting blood pressure [mm Hg]  
- **🧪 Cholesterol**: Serum cholesterol [mm/dl]  
- **🍬 FastingBS**: Fasting blood sugar [1 if > 120 mg/dl, else 0]  
- **📉 RestingECG**: Resting ECG results [Normal, ST, LVH]  
- **🏃 MaxHR**: Maximum heart rate achieved [60–202]  
- **💔 ExerciseAngina**: Exercise-induced angina [Y: Yes, N: No]  
- **📉 Oldpeak**: ST depression induced by exercise  
- **📈 ST_Slope**: Slope of peak exercise ST segment [Up, Flat, Down]  
- **🩺 HeartDisease**: Target variable [1: Heart disease, 0: Normal]  
