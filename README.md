

# GuardianPay - Protecting Against Lost Card and Copied Card Transactions

_비정상적인 거래 패턴 식별 및 복제 카드 결제 방지 프로그램_ <br>

<p align="right">
  <a href="https://blog.naver.com/pixelwizard/223313104718">
    <img src="https://img.shields.io/badge/한국어%20번역본-03C75A?style=flat-square&logo=Naver&logoColor=white" alt="네이버 블로그">
  </a>
</p>

![경고사진](https://github.com/pixelwizard2/Project.AI--GuardianPay---Protecting-Against-Lost-Card-and-Copied-Card-Transactions/assets/138272416/b63a944b-a865-45a2-bd76-2095e544f6d4) 
## Project Introduction (프로젝트 소개)

Credit card payments are one of the indispensable convenient payment methods in modern society. However, issues such as card information leakage, duplication, and unauthorized usage continue to rise. This threatens the financial security of individuals and businesses. To address these issues, the "GuardianPay" project was initiated. <br> <br> <br>


## Project Goals (프로젝트 목표)

The main goals of the "GuardianPay" project are as follows:
- Establish a system to detect abnormal card payment behavior and issue warnings.
- Block transactions that appear suspicious during payment attempts and notify cardholders.
- Utilize real-time data analysis and machine learning algorithms for more accurate detection of fraudulent behavior. <br> <br>
![경고사진1](https://github.com/pixelwizard2/Project.AI--GuardianPay---Protecting-Against-Lost-Card-and-Copied-Card-Transactions/assets/138272416/db256c05-cf23-4298-9f86-b039bcf1b905)

## Project Technology Stack (프로젝트 기술 스택)

The "GuardianPay" project uses the following technology stack:
- **Language :** Python
- **Data Analysis and Visualization :** Pandas, Matplotlib, Seaborn, Numpy
- **Machine Learning and Modeling :** Scikit-learn (train_test_split, confusion_matrix, classification_report)
- **Ensemble Learning Models :** RandomForestClassifier, GradientBoostingClassifier
- **Algorithm-related Models :** XGBoost, SVC (Support Vector Classifier)
- **Model Selection and Optimization :** GridSearchCV
- **Data Preprocessing :** OneHotEncoder, Pipeline, ColumnTransformer
- **Solving Data Imbalance :** SMOTE (Synthetic Minority Over-sampling Technique)
- **Statistical Analysis :** chi2_contingency (Chi-square test for independence)
- **Additional Tools and Libraries :** Google Colab(drive), Shutil
- **Web Application Development (Optional) :** Flask, HTML, CSS <br> <br>

## Project Workflow (프로젝트 진행 방식)

The project was conducted in the following steps:
1. **Data Collection :** Collect card payment data from sources from Kaggle.
2. **Data File Integration & Dataset Preprocessing.**
3. **Model Development :** Developing and training models based on machine learning algorithms.
4. **Model Evaluation and Feature Implementation.**
5. **System Construction (Optional):** Building a system to detect card payment anomalies in real-time.
6. **Web Application (Optional):** Developing a web application for card owners to monitor their payment activities. <br> <br>
![카글 페이지](https://github.com/pixelwizard2/Project.AI--GuardianPay---Protecting-Against-Lost-Card-and-Copied-Card-Transactions/assets/138272416/09c2dcb3-85df-4903-a01b-fda931f73ae4)
<br> <br>

## Project Execution Process (프로젝트 수행 과정)

The project was carried out as follows: <br> <br> <br>
![1  데이터셋 출력 사진](https://github.com/pixelwizard2/Project.AI--GuardianPay---Protecting-Against-Lost-Card-and-Copied-Card-Transactions/assets/138272416/e5b5d00d-a73b-4127-b3a5-65ee23249441)  
Collected payment card information, user information, and fraud data files from Kaggle. <br> <br> <br>

![3  전처리완료](https://github.com/pixelwizard2/Project.AI--GuardianPay---Protecting-Against-Lost-Card-and-Copied-Card-Transactions/assets/138272416/46130330-9e01-4df8-8975-1a1eb4dcd67d)  
Integrated and preprocessed datasets to form a consolidated file for model configuration. <br> <br> <br>

![4  히트맵 분석](https://github.com/pixelwizard2/Project.AI--GuardianPay---Protecting-Against-Lost-Card-and-Copied-Card-Transactions/assets/138272416/bf831dad-32ee-40a3-abf3-38a4cad15a60)  
Analyzed the correlation between the transaction amount ('Amount') and fraud status ('Is Fraud?') using a heatmap.  
Although the correlation was very low at 0.6%, indicating almost no linear relationship, a more detailed analysis was conducted as a close relationship between the amount and fraud status was suspected. <br> <br> <br>

![5  세부분석](https://github.com/pixelwizard2/Project.AI--GuardianPay---Protecting-Against-Lost-Card-and-Copied-Card-Transactions/assets/138272416/f1c0ed96-f7d3-47e2-a4fa-6496eef3bc17)  
Analyzed the relationship between categorized amounts and fraud using graphs, recognizing that high-amount transactions relatively have a higher risk of fraud, but most fraud transactions occur in lower amount categories.  
Conducted a chi-square test to derive the p-value, confirming a strong correlation between the two variables despite the small dataset, and decided to include these columns in the model. <br> <br> <br>  

![6  세부 데이터](https://github.com/pixelwizard2/Project.AI--GuardianPay---Protecting-Against-Lost-Card-and-Copied-Card-Transactions/assets/138272416/ed70e192-c2af-4719-96fe-07b1917328d9)  
Attempted to analyze 'normal payment' and 'fraudulent payment' patterns based on the 'Amount', 'Time', and 'Merchant City' columns, and visualized the time and amount of fraud transactions in major regions to analyze elements necessary for model configuration. <br> <br> <br>

![7  혼동행렬 체크](https://github.com/pixelwizard2/Project.AI--GuardianPay---Protecting-Against-Lost-Card-and-Copied-Card-Transactions/assets/138272416/984d631f-d925-4067-a4e2-9162f28b5355)  
Conducted oversampling & trained the Random Forest model, generating a report and constructing a Confusion Matrix. Attempted to address data imbalance and improve precision, recall, and f1-score values to enhance fraud detection.  <br> <br> <br>

![8  모델 분석](https://github.com/pixelwizard2/Project.AI--GuardianPay---Protecting-Against-Lost-Card-and-Copied-Card-Transactions/assets/138272416/4df32037-4845-40de-af12-f087da5b5d84)  
Tuned model parameters using GridSearchCV and tested models including Support Vector Machine (SVM), Gradient Boosting, and XGBoost. XGBoost was identified as the main ML model for this project due to its high accuracy in predicting actual fraudulent transactions. <br> <br> <br>

![9  그래프 분석](https://github.com/pixelwizard2/Project.AI--GuardianPay---Protecting-Against-Lost-Card-and-Copied-Card-Transactions/assets/138272416/1cd457c4-94b9-4f5a-8b2a-ea272c51defc)  
Constructed ROC Curve Comparison and Precision-Recall Curve Comparison to additionally compare the performance with other models.  
XGBoost demonstrated higher precision but slightly lower recall compared to Gradient Boosting, indicating a higher likelihood of correct fraud prediction.  <br> <br> <br>  

![2  결과 출력](https://github.com/pixelwizard2/Project.AI--GuardianPay---Protecting-Against-Lost-Card-and-Copied-Card-Transactions/assets/138272416/ebe8a0d2-7a91-46bb-a72a-4a8fb48ebab7)  
Mounted Google Drive, loaded the XGBoost model, retrieved the list of all cities from the training dataset, performed one-hot encoding, and prepared model input data for prediction.  
Project Challenges <br> <br> <br>

## Challenges encountered during the project were analyzed

Organized and analyzed errors that occurred during the project progress: <br> <br>

**Data Preprocessing Issue:**  

**Problem:** During data file integration, fraud determination data values were transformed into NaN.  
**Solution:** Unified data values to YES and NO, converted to 0 and 1, to resolve the issue caused by conflicts in NaN data values during file integration. <br> <br>

**Model Implementation Issue:**  

**Problem:** Encountered a mismatch in feature counts between training and user input data when implementing the developed XGBoost model.  
**Solution:** Despite reconfiguring the model after investigating issues in hyperparameter adjustment and data preprocessing, the same error persisted. Further study on model design features is needed for resolution. I will definitely solve it.  <br> 

![결과 출력 오류](https://github.com/pixelwizard2/Project.AI--GuardianPay---Protecting-Against-Lost-Card-and-Copied-Card-Transactions/assets/138272416/8f8bf370-9b34-4945-90c3-0583cfaf6343)




