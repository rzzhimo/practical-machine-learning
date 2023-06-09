## 9.1 Model Tuning|模型调参

### Manual Hyperparameter Tuning

### Automated Hyperparameter Tuning

### Automated Machine Learning (AutoML)
1. Automate every step in applying ML to solve real-world problems: data cleaning, feature extraction, model selection...
2. **Hyperparameter optimization (HPO)**: find a good set of hyperparameters through search algorithms
3. **Neural architecture search (NAS)**: construct a good neural network model

### Summary
1. Hyperparameter tuning aims to find a set of good values
2. It’s time consuming as data preprocessing
3. There is a trend to use algorithm for tuning

## 9.2 HPO algorithms|超参数优化 算法

### Search Space
1. Specify range for each hyperparameter
2. The search space can be exponentially large：
    - Need to carefully design the space to improve efficiency
### HPO algorithms: Black-box or Multi-fidelity

1. Black-box: treats a training job as a black-box in HPO
2. Multi-fidelity: modifies the training job to speed up the search

### Summary
1. Black-box HPO: grid/random search, bayesian optimization
2. Multi-fidelity HPO: Successive Halving, Hyperband
3. In practice, start with random search
4. Beware there are top performers：
    - You can find them by mining your training logs,or what common configurations used in paper/code

## 9.3 NAS algorithms|网络架构搜索 算法

### Neural Architecture Search (NAS)
1. A neural network has different types of hyperparameters
2. NAS automates the design of neural network

### NAS with Reinforcement Learning

### The One-shot Approach
1. Combines the learning of architecture and model params
2. Construct and train a single model presents a wide variety of architectures
3. Evaluate candidate architectures
4. Re-train the most promising candidate from scratch

### Differentiable Architecture Search

### Scaling CNNs

### Research directions|研究方向
1. Explainability of NAS result
2. Search architecture to fit into edge devices
3. To what extend can we automates the entire ML workflow?

### Summary
1. NAS searches a NN architecture for a customizable goal
    - Maximize accuracy or meet latency constraints on particular hardware
2. NAS is practical to use now:
    1. Compound depth,width,resolution scaling
    2. Differentiable one-hot neural network