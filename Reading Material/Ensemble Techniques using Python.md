# Ensemble Techniques in Python Cheat Sheet 📊🚀

Made with :heart: by **Fardeen Ahmad Khan**

Welcome to the exciting world of Ensemble Techniques in Python! This cheat sheet is your comprehensive guide to understanding and implementing ensemble learning methods for improved machine learning models. Don't forget to follow the author, [Fardeen Ahmad Khan](https://github.com/I-Fardeen), for more Python and Data Science insights! 🙌

## 🔑 **1. What are Ensemble Techniques?**:
   - Ensemble methods combine multiple machine learning models to create a more robust and accurate model.
   - They are used to reduce overfitting and improve predictive performance.

## 📊 **2. Types of Ensemble Techniques**:
   - **Bagging**:
     - Bootstrap Aggregating (Bagging) combines multiple models trained on different subsets of data.
     - Example: Random Forest.

   - **Boosting**:
     - Boosting sequentially trains models, giving more weight to misclassified samples.
     - Example: AdaBoost, Gradient Boosting.

   - **Stacking**:
     - Stacking combines the predictions of multiple models as input to another model.
     - Example: StackingClassifier.

   - **Voting**:
     - Voting combines the predictions of multiple models and selects the majority vote.
     - Example: VotingClassifier.

## 🔍 **3. Bagging with Random Forest**:
   - Import the necessary library.

   ```python
   from sklearn.ensemble import RandomForestClassifier

   rf = RandomForestClassifier(n_estimators=100, random_state=0)
   ```

## 🚀 **4. Boosting with AdaBoost**:
   - Use AdaBoost to improve weak classifiers.

   ```python
   from sklearn.ensemble import AdaBoostClassifier

   ada = AdaBoostClassifier(base_estimator=DecisionTreeClassifier(), n_estimators=50)
   ```

## 🌐 **5. Stacking with StackingClassifier**:
   - Stack models to enhance prediction accuracy.

   ```python
   from sklearn.ensemble import StackingClassifier
   from sklearn.linear_model import LogisticRegression

   estimators = [('rf', rf), ('ada', ada)]
   stack = StackingClassifier(estimators=estimators, final_estimator=LogisticRegression())
   ```

## 📉 **6. Voting with VotingClassifier**:
   - Combine the predictions of multiple classifiers.

   ```python
   from sklearn.ensemble import VotingClassifier

   estimators = [('rf', rf), ('ada', ada)]
   vote = VotingClassifier(estimators=estimators)
   ```

## 🔑 **7. Parameters Tuning**:
   - Tune hyperparameters for better model performance.

   ```python
   from sklearn.model_selection import GridSearchCV

   param_grid = {'n_estimators': [50, 100, 200]}
   grid_search = GridSearchCV(estimator=rf, param_grid=param_grid, cv=5)
   ```

## 🌟 **8. Evaluation**:
   - Evaluate ensemble models using metrics like accuracy, precision, recall, and F1-score.

   ```python
   from sklearn.metrics import accuracy_score, classification_report

   y_pred = vote.predict(X_test)
   accuracy = accuracy_score(y_test, y_pred)
   report = classification_report(y_test, y_pred)
   ```

With Ensemble Techniques, you can boost the performance of your machine learning models and make more accurate predictions. Dive into ensemble learning and take your data science skills to the next level! 📊🚀

Made with :heart: by **Fardeen Ahmad Khan**
