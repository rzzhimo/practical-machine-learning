## Deep Network Tuning|深度神经网络架构
1. DL is a programming language to extract information from data
2. Various design patterns, from layers to network architecture
3. Here we talk about some of them
### Batch Normalizations
1. Standardizing data makes the loss smother for linear methods
2. Batch Normalization (BN) standards inputs for internal layers
3. Reshape | Normalize | Recovery
### Layer Normalization
1. If apply to RNN, BN needs maintain separated moving statistics for each time step
2. Layer normalization reshapes input X ∈ Rn×p → X′ ∈ Rp×n or
X ∈ Rn×c×w×h → X′ ∈ Rcwh×n, rest is same with BN
### More Normalizations
1. Modify “reshape”
2. Modify “normalize”
3. Modify “recovery”
4. Apply to weights or gradients
### Summary
1. Normalizing inputs of internal layers makes deep NNs easier to train
2. A normalization layer performs three steps: reshape input, normalize data, recovery with learnable parameters
3. Notable examples include Batch Normalization for CNNs,Layer Normalization for Transformers