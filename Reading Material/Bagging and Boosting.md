# Bagging and Boosting using Python Cheat Sheet 🎯🚀

Made with :heart: **Fardeen Ahmad Khan**

Welcome to the exciting world of Bagging and Boosting techniques in Python! This cheat sheet is your comprehensive guide to understanding and implementing Bagging and Boosting algorithms for enhanced machine learning models. Be sure to follow the author, [Fardeen Ahmad Khan](https://github.com/I-Fardeen), for more Python and Data Science insights! 🙌

## 👜 **1. Bagging (Bootstrap Aggregating)**:
   - **Purpose**: Reduce variance and improve model stability.
   - **Key Algorithm**: Random Forest.
   - **Implementation**:

   ```python
   from sklearn.ensemble import RandomForestClassifier

   model = RandomForestClassifier(n_estimators=100)
   model.fit(X_train, y_train)
   ```

## 🚀 **2. Boosting**:
   - **Purpose**: Increase model accuracy by focusing on hard-to-classify data.
   - **Key Algorithms**: AdaBoost, Gradient Boosting, XGBoost.
   - **Implementation**:

   ```python
   from sklearn.ensemble import AdaBoostClassifier

   model = AdaBoostClassifier(n_estimators=50, learning_rate=1.0)
   model.fit(X_train, y_train)
   ```

## 🔗 **3. AdaBoost (Adaptive Boosting)**:
   - **Highlights**: Weighted training data to emphasize misclassified samples.
   - **Implementation**:

   ```python
   from sklearn.ensemble import AdaBoostClassifier

   model = AdaBoostClassifier(n_estimators=50, learning_rate=1.0)
   model.fit(X_train, y_train)
   ```

## 📊 **4. Gradient Boosting**:
   - **Highlights**: Builds models sequentially, correcting errors.
   - **Implementation**:

   ```python
   from sklearn.ensemble import GradientBoostingClassifier

   model = GradientBoostingClassifier(n_estimators=100, learning_rate=0.1)
   model.fit(X_train, y_train)
   ```

## 🚀 **5. XGBoost (Extreme Gradient Boosting)**:
   - **Highlights**: Highly efficient and scalable boosting algorithm.
   - **Implementation**:

   ```python
   import xgboost as xgb

   model = xgb.XGBClassifier(n_estimators=100, learning_rate=0.1)
   model.fit(X_train, y_train)
   ```

## 🔄 **6. Stacking**:
   - **Purpose**: Combine multiple models to improve prediction accuracy.
   - **Implementation**:

   ```python
   from sklearn.ensemble import StackingClassifier
   from sklearn.linear_model import LogisticRegression

   estimators = [('model1', model1), ('model2', model2), ('model3', model3)]
   model = StackingClassifier(estimators=estimators, final_estimator=LogisticRegression())
   model.fit(X_train, y_train)
   ```

Now that you're equipped with Bagging, Boosting, and Stacking techniques, you can elevate your machine learning models to new heights! Happy boosting! 🎯🚀

Made with :heart: by **Fardeen Ahmad Khan**
