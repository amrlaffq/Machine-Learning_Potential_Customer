# Python-Machine-Learning_Potential_Customer
Design a predictive model to determine the potential customers for the next product's promotion for Ads Company

1. Create a feature name "Potential Customer" (for model training purposes) ‼️ \
  ➡️ Set the Potential Customer into 1 or 0\
  ➡️ Based on the requirements of the model (eg look into customers who ever purchased after received the ads in last 12 months)
  
2. Data cleaning 💨\
  ➡️ Make sure the features that supposed to be either int64 or object are assigned correctly (eg Cust_Last_Purchase, Cust_Ann_Income should be in int64)\
  ➡️ Check if there's duplications in the dataset & remove if any\
    ✨ Also look into the dataset, if got duplicates for the common key 🆔 ✨\
  ➡️ Check the data for missing values\
    ✨ For some numerical data, missing value can be simply means 0 (eg: Last_Cust_Purchase) ✨\
    ✨ There will be situation where 0 won't be the best option (eg: Cust_Age). Thus, we can replace it with the mean if it's not skewed or median if it's skewed ✨\
    ✨ For categorical, one of the choice is to remove the data if the count is small ✨
    
3. Exploratory Data Analysis (EDA) 💦\
  ➡️ Commonly there should be only 2 types of categories for the variables (Categorical & Numerical)\
  ➡️ Create insights to look at the relationship between the variables\
    ✨ We should remove variables that is highly correlated with the "Potential Customer" ✨\
      eg: Cust_Tenure (longer the tenure of the customers with the company, the higher change of them to purchase an item)\
    ✨However, not all the time the Cust_Tenure has higher correlation, it actually depending on the objective and requirements of the built model✨
    
4. Feature Engineering & Selection 👷 \
  ➡️ Imply high level features that reflect the interactions between multiple columns as new features to get better insight and feed more information to the predictive model\
    ✨ Eg instead of a numerical column, can use log of the column, square of the column, or any other transformation of the column✨\
  ➡️ We can manually remove the highly correlation features, or can let the PCA handles it during pre-processing
  
5. Data Preprocessing 🧰 \
  ➡️ Seperate X(features) and y(target) \
    ✨ y(target) = "Potential_Customer" ✨ \
  ➡️ Change categorical variables with numerical variables (One-hot encoding or Dummy encoding) \
  refer here : https://towardsdatascience.com/encoding-categorical-variables-one-hot-vs-dummy-encoding-6d5b9c46e2db \
    ✨ Can also try to look into the Label Encoding (not being used in the notebook) ✨\
  refer here : https://www.naukri.com/learning/articles/one-hot-encoding-vs-label-encoding/ \
  ➡️ Split data into train/test \
    ✨ Split the data into 75% train, 25% test ✨\
    ✨ If wanna go more, we can add Over-The-Time(OTT) validation (not being used in the notebook) ✨\
  ➡️ Feature scaling \
    ✨ Also can try OverSampling & Undersampling ✨\
  refer here : https://machinelearningmastery.com/random-oversampling-and-undersampling-for-imbalanced-classification/ \
    ✨ Make used of Standard Scaler, Min Max Scaler or Power Transformer ✨\
  refer here : https://towardsdatascience.com/all-about-feature-scaling-bcc0ad75cb35 \
  ➡️ PCA on Numerical Columns only \
    ✨ To check the highly correlated features ✨ \
  refer here : https://towardsdatascience.com/pca-clearly-explained-how-when-why-to-use-it-and-feature-importance-a-guide-in-python-7c274582c37e \
  
6. Machine Learning 💻 \
  ➡️ Logistic Regression \
  ➡️ K-Neighbour Network (KNN) \
  ➡️ Decision Tree \
    ✨ To check the best ML algorithm, the Precision, Recall, F1 and Accuracy were used ✨\
  refer here : https://towardsdatascience.com/accuracy-precision-recall-or-f1-331fb37c5cb9 \
    ✨ Confusion Matrix also crucial in the phase of algorithm selection ✨ \
  refer here : https://towardsdatascience.com/understanding-confusion-matrix-a9ad42dcfd62
