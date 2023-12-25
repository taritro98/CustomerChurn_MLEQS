

---


# Customer Churn Prediction for B2B SaaS
**Notebook Author - Taritro Ghoshal**

## Task Introduction
In this data-driven project, I aim to address the pressing challenges faced by a B2B SaaS business: **predicting customer churn**. The goal is to develop predictive models that not only forecast churn with high accuracy but also unveil the underlying reasons behind customer attrition. This enables the business to intervene strategically and retain its customer base.

To tackle this multifaceted problem, I've orchestrated a structured approach segmented into 5 distinct Jupyter notebooks. Each notebook is created to address a specific aspect of the churn prediction task, ensuring a modular, organized, and reusable structure for easy understanding and efficient workflow.

The outline and summary of each of the notebooks are:

1. **EDA & Feature Engineering (1_EDA_FeatureEngineering.ipynb)** - Initial data exploration and transformation to prepare a robust dataset for predictive modeling. The preprocessed data is saved for future use.

2. **Modeling & Optimization (2_Modelling_Optimization.ipynb)** - Experimentation and evaluation of various classifiers, including tree-based bagging and boosting models, using stratified k-fold validation and hyperparameter tuning. The best models are saved alongside performance assessment on a holdout set.

3. **Ensemble Techniques (3_Ensembling_Models.ipynb)** - Development of stacked and voting classifiers to combine individual model predictions, enhancing model robustness, reliability and predictive strength. Ensemble models are saved for later analysis.

4. **Deep Learning Exploration (4_NeuralNetworks.ipynb)** - Implementation of a DenseNet neural network in PyTorch, offering a deep learning perspective on churn prediction. The focus is on network design, training, and validation.

5. **Interpretability, Risk Analysis & Validation (5_ModelExplainability_RiskAnalysis.ipynb)** - Interpretation of model predictions using SHAP, exploration of churn risk scores, and a detailed analysis of prediction errors. Calibration curves are employed to assess model reliability.

---
## Conclusion

From the beginning of this project, I endeavoured to predict customer churn based on the provided renewals dataset. Through rigorous data exploration, data preprocessing, feature engineering, modelling, optimization, ensembling and model explainability, I tackled this challenge systematically. 

In order to address the problem areas of the client:-
1. A robust model to predict customer churn was built
2. A customer churn model was built to predict churn to provide their team to action preventative measures. Additionally, potential cases of future churn were also identified for the team to be aware of and take appropriate measures.
3. A risk score was provided representing the churn propensity. Extensive explainability measures were employed to enable transparency and foster trust and reliance for the model predictions and enable customer success by effective conversations.
4. Model was rigorously validated and analyzed using techniques like stratified kfold cross validation, holdout set, monitoring multiple relevant validation metrics, explainability, calibration etc. This helps bolster trust and confidence in the client regarding the model performance and facilitates effective data-driven decision making
In order to Subsequent hyperparameter optimization fine-tuned the models to improve the predictive power even further.

In conclusion, I tackled the task of predicting customer churn and through meticulous and iterative efforts, achieved an insightful model that can predict churn with a notable degree of accuracy. This underscores the significance of methodical data analysis and advanced modeling in addressing real-world challenges.

##  Future Work
1. Advanced Feature Engineering: Explore more sophisticated feature interactions and time-series analyses to capture trends and patterns over time that may influence churn.
2. Improved Neural Networks : Experiment with different neural networks and improve the existing dense network using different architectures and introducing more regularization .
3. Unsupervised Learning for Customer Segmentation: Implement clustering techniques to identify distinct customer segments, which could lead to more tailored predictive models for each group.

----
## Authors

- [@taritro98](https://www.github.com/taritro98)

