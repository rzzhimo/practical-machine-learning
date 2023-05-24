## 2.1 探索性数据分析
### Summary
1. This notebook demonstrates the basic technologies for EDA, including：  
Understanding column data types, values, and distributions  
Understanding the interactions between columns  
2. We only explored a small aspect of the data. You are welcome to dive deep into more details.

## 2.2 数据清理
### Data Errors
### Types of Data Errors
### Outlier Detection
### Rule-based Detection 
### Pattern-based Detection
### Summary
1. Types of data errors: outliers, rule violations, pattern violations 
2. Multiple tools exist to help data cleaning：  
Graphic interface for interactive cleaning   
Automatically detect and fix  

## 2.3 Data Transformation|数据转换
### Normalization for Real Value Columns
### Image Transformations
### Video Transformations
### Text Transformations
### Summary
1. Transform data into formats preferred by ML algorithms
2. Need to balance storage, quality, and loading speed
Tabular:normalize real value features  
Images:cropping,downsampling,whitening   
Videos:clipping,sampling frames  
Text:stemming,lemmatization,tokenization  

## 2.4 Feature Engineering|特征工程
1. Before deep learning (DL), feature engineering (FE) was critical to using ML models
2. DL train deep neural networks to automatically extract features
### Tabular Data Features
### Text Features
### Image/Video Features
### Summary
1. Features are representations of raw data that are relevant to the target task
2. Feature engineering VS Feature learning：
The latter is preferred if available(images/videos/audio/text)  
Will cover more later in“transferlearning”  

## Data Part Summary|数据部分总结
### Collecting Data
1. Discover/ augment data
2. Generate data
### Data Labeling
1. Semi-supervised learning
2. Label via crowdsourcing
3. Weak supervision
### Data Preprocessing
1. Exploratory data analysis
2. Data cleaning
3. Data transformation
4. Feature engineering
