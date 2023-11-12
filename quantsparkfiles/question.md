
# Instructions

Below are a set of questions in relation to the churn prediction task. Please do your best to answer them and don't be afraid to add detail to your responses.

# Questions

1. The client uses Snowflake for storing a majority of their customer data. They wish to use the churn predictive model to make daily predictions on their customers and use derived output tables in Snowflake to build dashboards in Tableau for end-user interaction and wider stakeholder reporting. What would you recommend for deploying the model you have built / will build?

a. I would recommend deploying the model as a batch prediction service on a cloud platform such as Azure Machine Learning or AWS Sagemaker which can run on a daily prediction schedule. On AWS, we can use AWS Sagemaker studio and add Snowflake as a data source to access Snowflake data, create a data flow using data wrangler service to perform analysis and data transformations, train and experiment with the model, and deploy the data flow using AWS Sagemaker pipelines as a batch prediction service. The prediction data can be written back into another snowflake table which can be connected to Tableau for visualizations.

2. The client is cautious of needing to maintain the model after project completion. In particular, they are worried the model will gradually lose predictive capability due to changes in data over time. What systems and processes do you recommend implementing to support model maintenance? How can the client retain their confidence in the model and its outputs?

a. To support model maintenance, model monitoring systems need to be incorporated. In an overall level, the client can benefit from streamlining their churn prediction system using an MLOps pipeline.  MLFlow is a great open-source tool that can not only enable effective model tracking and versioning but also enable model monitoring. Evidently AI is another open source tool that can be integrated into the pipeline which helps monitor model, data and concept drift. Evidently supports deployment of live monitoring dashboards which we can deploy on the relevant cloud platform and monitor these drifts. Alerts can be set up to notify in case drifts are detected. To handle data and concept drift, data quality assessment processes need to be incorporated and regular data quality reviews should take place. Model drift can be handle by having automated retraining pipelines in the MLOps process.
To ensure client retains their confidence, we need to ensure a model retraining pipeline is in place to maintain model accuracy in cases of model drift. Model retraining pipelines can be set up using tools like Airflow where retraining can be triggered when validation metrics drop below a certain threshold.


3. During the delivery of the churn prediction project you will need to provide progress updates on model development. How would you seek to validate the model performance from a development perspective, and how would you use these results to inform wider non-technical stakeholders?

a. From a development perspective, I'll use extensive stratified cross-validation techniques and further validate on a separate holdout set to test the model's ability to generalize on unseen data. I'll use a range of validation metrics depending on the use case - F1 Score, ROC-AUC, precision-recall, weighted and macro averages in this use case due to high imbalance in the dataset. Monitoring a range of validation metrics will ensure a multifaceted approach to validation where the performance of the model over different classes and data subsets are monitored to ensure the model is robust and help bolster client confidence in the model predictions. I've implemented these techniques in my assessment as well. 
To present the results to non-technical stakeholders:-
1.  I'll use clear visualizations such as confusion matrix, ROC curves and ensure suitable comparisons with benchmarks so that the audience has clear references of comparison. 
2. I'll showcase model explainability graphs and prediction analysis of the model on a case-by-case basis. For example, I'll take some samples of the model predictions and showcase the business features along with their impact using SHAP explainability that led to the predictions
3. I'll underscore all of my presentations with the relevant business impact and examples. For instance, I'll communicate what business features can be targeted in order to improve customer retention strategies. 

Regular progress updates should be delivered in an accessible format, highlighting both the technical and business performance of the model.

4. The client is investing in capturing more data points on their customers with the intention of using this new data in the model at some point in the near future. What recommendations would you make to the client in regards to including these new features? For context, they have limited expertise in machine learning, but do have resource in business analytics and analytics engineering.

a. A thorough validation system should be in place before incorporating new features into the existing dataset. I would recommend a process with the following stages to be included in the system:-
1. Conduct an exploratory data analysis to understand the data distributions, data quality, correlations etc. to pave way for effective treatment of the data and effectively engineer new features
2. Perform relevant feature engineering using the new features to capture their interactions amongst themselves and with existing features.
3. Assess feature importance analysis using different prediction models to assess whether the new features have any impact on churn. Conduct thorough validation using relevant validation metrics and compare model performance without and with adding new features.
4. Perform error analysis and explainability using libraries like SHAP to understand the relevance of these features in the predictions.
5. Integrate these new features into the model iteratively and validate their impact on performance each time. 

The system should be implemented as a robust pipeline that can perform all the above steps as new data comes in. This process should be well-documented so that the client's business analytics team, with their existing skill set, can understand and manage the updated model with minimal additional training. Productizing the entire feature incorporation process into a low-code or no-code platform or custom-built API can help the client business analytics teams can manage these processes using the existing skill-sets.
