---

#### Dataset
- This dataset is obtained from Kaggle: [Heart Failure Prediction Dataset](https://www.kaggle.com/datasets/fedesoriano/heart-failure-prediction)

#### Context
- The dataset contains 11 features that can be used to predict the presence of heart disease.
- A machine learning model was trained to assist with diagnosing this disease.

#### Results

| Model            | Train Accuracy | Test Accuracy |
|------------------|----------------|---------------|
| KNN              | 88.5%          | 87.2%         |
| Decision Tree    | 85.42%         | 84.24%        |
| Random Forest    | 92.92%         | 89.13%        |
| XGBoost          | 96.73%         | 85.33%        |
| Neural Network   | 87.46%         | 85.3%         |

#### Work Done
- This project builds on the course material from Andrew Ng’s ML Specialization, where he compares Decision Trees, Random Forest, and XGBoost. I extended the comparison by experimenting with Neural Networks and the KNN algorithm to try and outperform the Random forest model. Interestingly, KNN achieved the second-highest test accuracy, showing that even simple distance-based models can be competitive on well-preprocessed datasets.

> **Note:** All models performed quite similarly, with only a 3–4% difference in test accuracy. The reasons below are based on my own understanding of why a particular model may have performed better than others in this context.

- **Reasons for Random Forest outperforming others:**
  1. **XGBoost**: Although it achieved the highest training accuracy, its lower test accuracy suggests overfitting — likely due to the small dataset (around 700 training samples).
  2. **Decision Tree**: A single tree tends to overfit or underfit and generally performs worse than ensemble methods like Random Forest or XGBoost.
  3. **KNN**: Performed surprisingly well, achieving the second-best test accuracy (87.2%). This suggests that the feature space was well-scaled and structured in a way that favored proximity-based learning.
  4. **Neural Networks**: They require larger datasets to perform optimally. With only 700 training samples, it's hard to avoid overfitting or underfitting despite tuning.

#### Attribute Information
- **Age**: Age of the patient [years]  
- **Sex**: Sex of the patient [M: Male, F: Female]  
- **ChestPainType**: Chest pain type [TA: Typical Angina, ATA: Atypical Angina, NAP: Non-Anginal Pain, ASY: Asymptomatic]  
- **RestingBP**: Resting blood pressure [mm Hg]  
- **Cholesterol**: Serum cholesterol [mm/dl]  
- **FastingBS**: Fasting blood sugar [1: if FastingBS > 120 mg/dl, 0: otherwise]  
- **RestingECG**: Resting electrocardiogram results [Normal, ST, LVH]  
- **MaxHR**: Maximum heart rate achieved [60–202]  
- **ExerciseAngina**: Exercise-induced angina [Y: Yes, N: No]  
- **Oldpeak**: ST depression induced by exercise  
- **ST_Slope**: Slope of the peak exercise ST segment [Up, Flat, Down]  
- **HeartDisease**: Target variable [1: Heart disease, 0: Normal]
