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