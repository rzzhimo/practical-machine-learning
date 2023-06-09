## 4.1 Model Metrics|模型评估
1. Loss measures how good the model in predicting the outcome in supervised learning
2. Other metrics to evaluate the model performance
3. We select models by multiple metrics
### Metrics for Binary Classification
1. Accuracy: #correct predictions / #examples
2. Precision: #True positive / #(True positive + False positive)
3. Recall: #True positive / #Positive examples
    - Be careful of division by 0
4. F1:the harmonic mean of precision and recall:2pr/(p+r)
    - One metric that balances precision and recall
### AUC-ROC
1. Measures how well the model can separate the two classes
2. Choose decision threshold θ, predict positive if o ≥ θ else neg
3. in the range[0.5,1]
### Case Study: Displaying Ads
Ads is one major revenue source for Internet companies
### Business Metrics for Displaying Ads
1. Optimize both revenue and customer experience:
    1. Latency:ads should be shown to users at the same time as others
    2. ASN:average #ads shown in a page
    3. CTR:actual user click through rate
    4. ACP:average price advertiser pay sper click
2. revenue = #pageviews × ASN × CTR × ACP
### Displaying Ads: Model → Business Metrics
1. The key model metric is AUC
2. A new model with increased AUC may harm business metrics, possible reasons:
   1. Lower estimated CTR → less ads displayed
   2. Lower real CTR because we trained and evaluated on past data
   3. Lower prices
3. Online experiment: deploy models to evaluate on real traffic data
### Summary
1. We evaluate models with multiple metrics
2. Model metrics evaluate model performance on examples
    - E.g.accuracy,precision,recall,F1,AUC for classification models
3. Business metrics measure how models impact the product

## 4.2 Underfiting & Overfitting|欠拟合、过拟合
1. Training error: model error on the training data
2. Generalization error: model error on new data

### Model Complexity
1. The capacity of a set of function to fit data points
2. In ML, model complexity usually refers to:
    1. The number of learnable parameters
    2. The value range for those parameters
3. It’s hard to compare between different types of ML models
    E.g. trees vs neural network
4. More precisely measure of complexity: VC dimension

### Data Complexity
1. Multiple factors matters 
2. Again, hard to compare among very different data
3. More precisely, Kolmogorov complexity

### Generalization error
- Generalization error also depends on the training algorithm
### Model Selection
1. Pick a model with a proper complexity for your data
2. Pick up a model family, then select proper hyper-parameters
### Summary
1. We care about generalization error
2. Model complexity: the ability to fit various functions
3. Data complexity: the richness of information
4. Model selection: match model and data complexities

## 4.3 Model Validation|模型验证
### Generalization Error
- Approximated by the error on a holdout test dataset, which has never been seen by the model and can be only used once
### Hold Out Validation
### Split non I.I.D. data
### K-fold Cross Validation
1. Useful when not sufficient data
2. Algorithm:
3. Popular choices: K = 5 or 10
### Common Mistakes
1. If your ML model performance is too good to be true, very likely there is a bug, and contaminated valid set is the #1 reason.
2. Valid set has duplicated examples from train set
    - Often happens when integrating multiple datasets
    - E.G. Scrape images from search engine to evaluate models trained on ImageNet
3. Information leaking from train set to valid set
    - Often happens for non I.I.D data
    - E.G. use future to predict past, see a person’s face before
4. Excessive use of valid set for hyper param tuning is cheating
### Summary 
1. The test data is used once to evaluate your model
2. One can hold out a validation set from the training data to estimate the test data
3. You can use validset multiple times for model selections and hyper param tuning
4. Validation data should be close to the test data
5. Improper validset is a common mistake that lead to over estimate of the model performance