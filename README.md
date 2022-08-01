# Credit_Risk_Analysis

---

## 1. Overview of the analysis:

In 2019, more than 19 million Americans had at least one unsecured personal loan. Personal lending is growing faster than credit card, auto, mortgage, and even student debt. With such growth, FinTech firms are storming ahead of traditional loan processes. By using the latest machine learning techniques, these FinTech firms can continuously analyze large amounts of data and predict trends to optimize lending.

Being able to predict credit risk with machine learning algorithms can help banks and financial institutions predict anomalies, reduce risk cases, monitor portfolios, and provide recommendations on what to do in cases of fraud.

Credit risk is an inherently unbalanced classification problem, as good loans easily outnumber risky loans. Therefore, through the use of Python, imbalanced-learn and scikit-learn libraries we implemented machine learning to train and evaluate models. We used the credit card credit dataset from LendingClub, a peer-to-peer lending services company. The models we used oversample the data using the RandomOverSampler and SMOTE algorithms, and undersample the data using the ClusterCentroids algorithm. Then, we used combinatorial approach of over- and undersampling using the SMOTEENN algorithm. Finally we compare two new machine learning models that reduce bias, BalancedRandomForestClassifier and EasyEnsembleClassifier, to predict credit risk. Now we will evaluate the performance of these models.

---

## 2. Results

Descrption of the balanced accuracy scores, the precision and recall scores of all six machine learning models:

### OVERSAMPLING

#### 1.Naive Random Oversampling

*Main Indicators:

- Balanced Accuracy Score: 66.27%
- Avg/Total Precision:0.99
- Avg/Total Recall:0.64

![NRO](/Format%20Date.png)

#### 2.SMOTE Oversampling

- Balanced Accuracy Score: 65.83%
- Avg/Total Precision:0.99
- Avg/Total Recall:0.68

![SMOTE](/Format%20Date.png)

### UNDERSAMPLING

### 3.ClusterCentroids resampler

- Balanced Accuracy Score: 54.47%
- Avg/Total Precision:0.99
- Avg/Total Recall:0.40

![CCR](/Format%20Date.png)

### Combination (Over and Under) Sampling

### 4.SMOTEENN

- Balanced Accuracy Score: 64.27%
- Avg/Total Precision:0.99
- Avg/Total Recall:0.58

![SMO](/Format%20Date.png)

### Ensemble Learners

### 5.Balanced Random Forest Classifier

- Balanced Accuracy Score: 78.85%
- Avg/Total Precision:0.99
- Avg/Total Recall:0.87

![nro](/Format%20Date.png)

### 6.Easy Ensemble AdaBoost Classifier

- Balanced Accuracy Score: 93.16%
- Avg/Total Precision:0.99
- Avg/Total Recall:0.94

![EEC](/Format%20Date.png)

---

## 3. Summary

### Results of the machine learning models

1.Naive Random Oversampling: Balanced Accuracy Score: 66.27% / Avg/Total Precision:0.99 / Avg/Total Recall:0.64
2.SMOTE Oversampling: Balanced Accuracy Score: 65.83% / Avg/Total Precision:0.99 / Avg/Total Recall:0.68
3.ClusterCentroids resampler: Balanced Accuracy Score: 54.47% / Avg/Total Precision:0.99 / Avg/Total Recall:0.40
4.SMOTEENN: Balanced Accuracy Score: 64.27% / Avg/Total Precision:0.99 / Avg/Total Recall:0.58
5.Bal. Random Forest Classif: Balanced Accuracy Score: 78.85% / Avg/Total Precision:0.99 / Avg/Total Recall:0.87
**6.E.E. AdaBoost Classif.:Balanced Accuracy Score: 93.16% / Avg/Total Precision:0.99 / Avg/Total Recall:0.94

![EEC](/Format%20Date.png)

### Recommendation on the model to use:

I would recomend the usage of the Ensamble Learner model Easy Ensemble AdaBoost Classifier. Te reason is beacause it's Balanced Accuracy Score is over 90, letting us know that it has a good chance to have good predictions, in the other hand Recall is the highest across models and very near to 1. Also i would recomend to make credit risk evaluation to individuals using more than one model, for example using EE Adaboost and Baalanced Random Fores (wich also has high rating across the models we used) and if both models point in the same direction then move forward. Pros: Being extra carefull on desition making. Cons: Maybe lose some desitions for being extra carefull.
